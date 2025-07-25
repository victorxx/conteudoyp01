let indexe = 0;
const limiteporvez = 1;
const resultado = document.getElementById('video');
const botao = document.getElementById('btn');
let contador = 0;
const videos = [
  // seus links de vídeos aqui
                     'https://www.youtube.com/embed/5H4-NStHs7A',
'https://www.youtube.com/embed/6NREQi8Nvgc',
'https://www.youtube.com/embed/esibk_2OXak',
'https://www.youtube.com/embed/GNqSIyNXFM4',
'https://www.youtube.com/embed/WHGPYxV28eA',
'https://www.youtube.com/embed/mrODfbZ1Iy4',
'https://www.youtube.com/embed/VEYAs7OlSvQ',
'https://www.youtube.com/embed/6VhMKBonOeY',
'https://www.youtube.com/embed/GNqSIyNXFM4',
'https://www.youtube.com/embed/oqYl88iI6MM',
'https://www.youtube.com/embed/KhiHtohPP3U',
'https://www.youtube.com/embed/kowX7PdHFTw',
'https://www.youtube.com/embed/-6UtDa9OHrA',
'https://www.youtube.com/embed/ufbWBUWhMZs',
'https://www.youtube.com/embed/siemyLr8Ke0',
'https://www.youtube.com/embed/jgbxxxU0EVM',
'https://www.youtube.com/embed/dYuq6wR-p98',
'https://www.youtube.com/embed/iqJDpOYuiMU',
'https://www.youtube.com/embed/0lwdM3aslG0',
'https://www.youtube.com/embed/aLiCrfdJxJE',
'https://www.youtube.com/embed/CJPxH_0QiM0',
'https://www.youtube.com/embed/0XMVNmbWx1I',
'https://www.youtube.com/embed/5t_25JJyO7s',
'https://www.youtube.com/embed/aGowv-jMIZ0',
'https://www.youtube.com/embed/GlDtQdtbyk8',
'https://www.youtube.com/embed/6NREQi8Nvgc',
'https://www.youtube.com/embed/UK2La26ODnY',
'https://www.youtube.com/embed/R4AIHaCLPP8',
'https://www.youtube.com/embed/yZ7HwYSOTDc',
'https://www.youtube.com/embed/K3Hhr4mYkz4',
'https://www.youtube.com/embed/KwAJVIlILvM',
'https://www.youtube.com/embed/8709AFvpYfc',
'https://www.youtube.com/embed/6knnv_rjOr4',
'https://www.youtube.com/embed/Mju8aEKrIlk',
'https://www.youtube.com/embed/zMbnJV-6YgY',
'https://www.youtube.com/embed/Gw66r1AsMLk',
'https://www.youtube.com/embed/lgIIL2ll9Io',
'https://www.youtube.com/embed/6DYkq6FMQR8',
'https://www.youtube.com/embed/kqTtlwG_Eb4',
'https://www.youtube.com/embed/0EEUJ6Tyqdk',
'https://www.youtube.com/embed/WHGPYxV28eA',
'https://www.youtube.com/embed/wr_-DCRLg9w',
'https://www.youtube.com/embed/sMA-wrn10aI',
'https://www.youtube.com/embed/cnYNGO7xdkQ',
'https://www.youtube.com/embed/nZSp9AzJius',
'https://www.youtube.com/embed/6sXRf6m_5bI',
'https://www.youtube.com/embed/3OIsxJf-Z2U',
'https://www.youtube.com/embed/0xgcUSUdv84',
'https://www.youtube.com/embed/UyYV7TvKrL4',
'https://www.youtube.com/embed/Q2rDHh4_4mU',
'https://www.youtube.com/embed/FEIIVPRoBMY',
'https://www.youtube.com/embed/KTtzIFOOP9g',
'https://www.youtube.com/embed/JK9FuWvaISE',
'https://www.youtube.com/embed/fge7NcZtG8M',
'https://www.youtube.com/embed/fOIeVVFNn3w',
'https://www.youtube.com/embed/I2oROAyhgyo',
'https://www.youtube.com/embed/dWUYkkkLpfA',
'https://www.youtube.com/embed/mrODfbZ1Iy4',
'https://www.youtube.com/embed/ek5XCBAphSc',
'https://www.youtube.com/embed/rdDeOtpCG6A',
'https://www.youtube.com/embed/6pLzTtINz7Q',
'https://www.youtube.com/embed/o1Q2A2CAFN8',
'https://www.youtube.com/embed/xdzyj0_BLeM',
'https://www.youtube.com/embed/yKX0VIb1NMc',
'https://www.youtube.com/embed/hKownpGXyTk',
'https://www.youtube.com/embed/EHdvIOnf3Sc',
'https://www.youtube.com/embed/EMU_Ulv6CFA',
'https://www.youtube.com/embed/Fuwmnpt7RQc',
'https://www.youtube.com/embed/VI1aOs1H_LE',
'https://www.youtube.com/embed/yC_q2LnEGX0',
'https://www.youtube.com/embed/ktVUwEkiZ7E',
'https://www.youtube.com/embed/uSXYUWfYosE',
'https://www.youtube.com/embed/AlQqUOxpOtw',
'https://www.youtube.com/embed/361CYsjZjnI',
'https://www.youtube.com/embed/QnSLOJyBxhE',
'https://www.youtube.com/embed/1yG_4_gfHSw',
'https://www.youtube.com/embed/pKDBs68LZKA',
'https://www.youtube.com/embed/NUdK9OSEBmk',
'https://www.youtube.com/embed/5wN8aRc37uQ',
'https://www.youtube.com/embed/jbFmQY7qPAo',
'https://www.youtube.com/embed/7ULSR8IJ590',
'https://www.youtube.com/embed/QiWy7lqDsfA',
'https://www.youtube.com/embed/YUWpG3fADNA',
'https://www.youtube.com/embed/y9SwyBSo14I',
'https://www.youtube.com/embed/0t2x31P2RlI',
'https://www.youtube.com/embed/KRdUg3vVBSA',
'https://www.youtube.com/embed/UcoqpN0XWmE',
'https://www.youtube.com/embed/jy1BjuqtxRY',
'https://www.youtube.com/embed/KJLDbG-QlCA',
'https://www.youtube.com/embed/tHVkY-wBi_A',
'https://www.youtube.com/embed/f_JEB7OwsNI',
'https://www.youtube.com/embed/mCfEUZcpYpg',
'https://www.youtube.com/embed/AcnzaSDzvJ4',
'https://www.youtube.com/embed/bWGNieFtduY',
'https://www.youtube.com/embed/RWXwrzTLfa4',
'https://www.youtube.com/embed/MmXUp4JGrpQ',
'https://www.youtube.com/embed/5ng3JDt8qHA',
'https://www.youtube.com/embed/VY57XiCMPEs',
'https://www.youtube.com/embed/10e8sKzHbJY',
'https://www.youtube.com/embed/gbhmzPxjXw4',
'https://www.youtube.com/embed/IzhoryfEe5k',
'https://www.youtube.com/embed/DYmXZWj-EA8',
'https://www.youtube.com/embed/NLSjTmPr2aU',
'https://www.youtube.com/embed/tthbZrGgwCg',
'https://www.youtube.com/embed/-Z_ajai09cY',
'https://www.youtube.com/embed/S-9xdF_mXHA',
'https://www.youtube.com/embed/0nwOomSvA4M',
'https://www.youtube.com/embed/fylzPAsxkws',
'https://www.youtube.com/embed/mIbC3hNIK5c',
'https://www.youtube.com/embed/NeYXss6S0VM',
'https://www.youtube.com/embed/BjVxkyyUGSY',
'https://www.youtube.com/embed/Y734WSfGB7E',
'https://www.youtube.com/embed/MtaCFYIDPzk',
'https://www.youtube.com/embed/OBHBENKzQWU',
'https://www.youtube.com/embed/35tdu3OZqZg',
'https://www.youtube.com/embed/erOe8JzRdC8',
'https://www.youtube.com/embed/sA2ezgdNMcM',
'https://www.youtube.com/embed/ZxUhCy41Phw',
'https://www.youtube.com/embed/Zl_1rQ4JR6c',
'https://www.youtube.com/embed/9s00HMnDCVc',
'https://www.youtube.com/embed/tsltmFn0a0k'


];

function criaIframe(src, width = 300, height = 300) {
  const iframe = document.createElement('iframe');
  iframe.src = src;
  iframe.width = width;
  iframe.height = height;
  iframe.setAttribute('frameborder', '0');
  iframe.setAttribute('allowfullscreen', '');
  return iframe;
}

botao.onclick = function () {
  let final = indexe + limiteporvez;

  for (; indexe < final && indexe < videos.length; indexe++) {
    contador++;

    // cria e adiciona o vídeo
    let iframe = criaIframe(videos[indexe]);
    resultado.appendChild(iframe);

    if (contador === 4) {
      // Anúncio para contador 1
      const div = document.createElement('div');
      div.innerHTML = `
        <iframe src="https://sistema01.pages.dev/" width="350" height="250" frameborder="0" allowfullscreen></iframe>
          <a href="https://sistema01.pages.dev/" 
          style="display: inline-block; background-color: blue; color: white; padding: 10px 20px; border-radius: 5px; text-decoration: none; font-weight: bold; font-family: sans-serif;">
          ABRIR TELA CHEIA
        </a> 
      `;
      resultado.appendChild(div);
      
    } 

    if (contador === 5) {
      // Anúncio para contador 1
      const div = document.createElement('div');
      div.innerHTML = `
        <iframe src="https://conteudo01.pages.dev/" width="350" height="250" frameborder="0" allowfullscreen></iframe>
          <a href="https://conteudo01.pages.dev/" 
          style="display: inline-block; background-color: blue; color: white; padding: 10px 20px; border-radius: 5px; text-decoration: none; font-weight: bold; font-family: sans-serif;">
          ABRIR TELA CHEIA
        </a> 
      `;
      resultado.appendChild(div);
      contador=0;
    } 

    if (contador === 1) {
      // Anúncio para contador 1
      const div = document.createElement('div');
      div.innerHTML = `
        <iframe src="https://uteis01.pages.dev/servicobancario" width="350" height="250" frameborder="0" allowfullscreen></iframe>
        <a href="https://uteis01.pages.dev/servicobancario" 
          style="display: inline-block; background-color: blue; color: white; padding: 10px 20px; border-radius: 5px; text-decoration: none; font-weight: bold; font-family: sans-serif;">
          ABRIR TELA CHEIA
        </a> 
      `;
      resultado.appendChild(div);
    
    } 
    
    else if (contador === 2) {
      // Anúncio para contador 2 (diferente do 1)
      const div = document.createElement('div');
      div.innerHTML = `
        <iframe src="https://encurtadorko.pages.dev/" width="350" height="500" frameborder="0" allowfullscreen></iframe>
        <a href="http://www.espiritosanto-es.com.br/cloudflare" 
          style="display: inline-block; background-color: blue; color: white; padding: 10px 20px; border-radius: 5px; text-decoration: none; font-weight: bold; font-family: sans-serif;">
          CONFERIR 2
        </a>

      `;
      resultado.appendChild(div);
       // reseta contador depois do 2
    }
  }

  if (indexe >= videos.length) {
    botao.disabled = true;
    botao.textContent = 'Chegamos no limite já';
  }
};
