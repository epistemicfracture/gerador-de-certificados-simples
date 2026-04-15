<h1>🎓 Gerador de Certificados Simples (Google Colab)</h1>

<p>
Gere certificados automaticamente em <strong>PDF</strong> a partir de uma lista de participantes em Excel,
diretamente no <strong>Google Colab</strong>, sem instalar Python no computador.
</p>

<p>
✅ Simples de usar &nbsp;|&nbsp;
✅ Funciona no navegador &nbsp;|&nbsp;
✅ Gera certificados e lista de e-mails
</p>

<hr>

<h2>🚀 Comece aqui</h2>

<p>
Este repositório foi criado para facilitar a geração automática de certificados a partir de uma planilha
com os nomes e e-mails dos participantes.
</p>

<p>
O processo é executado inteiramente no <strong>Google Colab</strong>, de forma prática e rápida.
</p>

<p>
<a href="https://colab.research.google.com/" target="_blank">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Abrir no Colab"/>
</a>
</p>

<p>
Depois de abrir o Colab, carregue o arquivo <strong>Gerador_de_certificados_simples.ipynb</strong>.
</p>

<hr>

<h2>📁 Arquivos do repositório</h2>

<ul>
  <li>
    <strong>Gerador_de_certificados_simples.ipynb</strong><br>
    Notebook principal que executa todo o processo.
  </li>
  <br>
  <li>
    <strong>Lista.xlsx</strong><br>
    Planilha modelo com os nomes e e-mails dos participantes.
  </li>
  <br>
  <li>
    <strong>Modelo certificado.pdf</strong><br>
    Modelo de exemplo em PDF para testes. Utilize um único arquivo modelo (template) do certificado,
    que será enviado quando solicitado durante a execução do notebook no Google Colab.
  </li>
  <br>
  <li>
  <strong>Modelo certificado (editável).pptx</strong><br>
  Modelo editável em PowerPoint (.pptx), que pode ser modificado livremente para criar o seu próprio
  layout de certificado antes de exportá-lo como PDF.
  <br><br>
🎨 Alternativamente, você pode criar o certificado diretamente no
<a href="https://www.canva.com/" target="_blank">Canva</a>,
 ajustando livremente o layout antes de exportá-lo em <strong>PDF</strong> para uso como modelo no gerador.
  </li>
</ul>

<hr>

<h2>⚙️ O que o script faz</h2>

<ol>
  <li>📄 Lê os nomes da planilha Excel</li>
  <li>🖋️ Insere o texto no certificado</li>
  <li>📚 Gera um PDF final com todos os certificados</li>
  <li>📧 Cria um arquivo com os e-mails dos participantes</li>
</ol>

<hr>

<h2>🧭 Como usar no Google Colab</h2>

<h3>1. Abra o notebook</h3>

<p>
Clique no botão do Google Colab acima e carregue o arquivo
<strong>Gerador_de_certificados_simples.ipynb</strong>.
</p>

<h3>2. Execute o notebook</h3>

<p>
No menu do Colab, clique em <strong>Executar tudo</strong> ou use <strong>Ctrl + F9</strong>.
As bibliotecas necessárias serão instaladas automaticamente.
</p>

<h3>3. Envie a planilha</h3>

<p>
Quando o Colab solicitar a planilha, envie o arquivo:
</p>

<pre><code>Lista.xlsx</code></pre>

<p>
A planilha deve conter <strong>exatamente</strong> estas colunas:
</p>

<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>E-mail</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>João da Silva</td>
      <td>joao@email.com</td>
    </tr>
  </tbody>
</table>

<h3>💡 Dica prática: como coletar os nomes dos participantes rapidamente</h3>

<p>
Se você ainda não possui a lista de participantes, pode gerá-la facilmente usando
o <strong>Google Forms</strong>.
</p>

<ol>
  <li>
    Acesse:
    <a href="https://forms.google.com" target="_blank">Google Forms</a>
  </li>
  <li>
    Crie um formulário com exatamente dois campos:
    <strong>Nome</strong> e <strong>E-mail</strong>
  </li>
  <li>
    Compartilhe o formulário com os participantes durante o evento
  </li>
  <li>
    Exporte as respostas em Excel e salve o arquivo como <strong>Lista.xlsx</strong>
  </li>
</ol>

<p>
📌 Uma forma prática de divulgar o formulário é gerar um QR Code e colocá-lo na porta da sala
ou projetá-lo na tela durante o evento.
</p>

<p>
Você pode gerar o QR Code aqui:
<a href="https://www.canva.com/qr-code-generator/" target="_blank">
Canva QR Code Generator
</a>
</p>

<p>
⚠️ Ao exportar a planilha, mantenha exatamente as colunas
<strong>Nome</strong> e <strong>E-mail</strong>.
</p>

<h3>4. Envie o PDF modelo do certificado</h3>

<p>
Depois, o Colab solicitará o arquivo PDF que será usado como modelo de fundo do certificado.
Envie esse arquivo normalmente.
</p>

<h3>5. Baixe os arquivos gerados</h3>

<p>
Ao final da execução, serão gerados automaticamente:
</p>

<ul>
  <li><strong>certificados_ouvintes.pdf</strong></li>
  <li><strong>emails_ouvintes.txt</strong></li>
</ul>

<hr>

<h2>✏️ Como editar o texto do certificado</h2>

<p>
O texto exibido no certificado é definido dentro da função
<strong>montar_texto_certificado(nome)</strong> no notebook.
</p>

<p>Localize este trecho:</p>

<pre><code>
return (
    f'CERTIFICAMOS QUE &lt;b&gt;{nome}&lt;/b&gt; '
    f'PARTICIPOU COMO OUVINTE NO ENCONTRO DE &lt;b&gt;SEMINÁRIOS DE PESQUISA DO PPGE&lt;/b&gt;, '
    f'REALIZADO EM &lt;b&gt;14 DE ABRIL DE 2026&lt;/b&gt;, '
    f'NA FACULDADE DE CIÊNCIAS E LETRAS DE ARARAQUARA, '
    f'CARACTERIZANDO &lt;b&gt;1 HORA&lt;/b&gt; DE ATIVIDADE.&lt;br/&gt;&lt;br/&gt;'
    f'ARARAQUARA, &lt;b&gt;{data_extenso}&lt;/b&gt;.'
)
</code></pre>

<p>Você pode alterar:</p>

<ul>
  <li>📌 Nome do evento</li>
  <li>📅 Data do evento</li>
  <li>🏛️ Instituição</li>
  <li>📍 Cidade</li>
  <li>⏱️ Carga horária</li>
</ul>

<p>Exemplo modificado:</p>

<pre><code>
return (
    f'CERTIFICAMOS QUE &lt;b&gt;{nome}&lt;/b&gt; '
    f'PARTICIPOU DO &lt;b&gt;WORKSHOP DE EXEMPLO&lt;/b&gt;, '
    f'REALIZADO EM &lt;b&gt;10 DE MAIO DE 2026&lt;/b&gt;, '
    f'NA UNIVERSIDADE DE EXEMPLO, '
    f'COM CARGA HORÁRIA DE &lt;b&gt;4 HORAS&lt;/b&gt;.&lt;br/&gt;&lt;br/&gt;'
    f'CIDADE (UF), &lt;b&gt;{data_extenso}&lt;/b&gt;.'
)
</code></pre>

<p>
⚠️ Não remova <strong>{nome}</strong> nem <strong>{data_extenso}</strong>,
pois esses campos são preenchidos automaticamente pelo sistema.
</p>

<hr>

<h2>📐 Como ajustar a posição do texto</h2>

<p>
Se o texto aparecer muito alto, muito baixo ou fora do lugar no certificado, ajuste a variável:
</p>

<pre><code>TEXT_BOX_Y = 300</code></pre>

<p>Você pode testar valores como:</p>

<pre><code>
TEXT_BOX_Y = 350
TEXT_BOX_Y = 300
TEXT_BOX_Y = 250
TEXT_BOX_Y = 200
</code></pre>

<hr>

<h2>🛠️ Problemas comuns</h2>

<h3>O texto não aparece no certificado</h3>

<ul>
  <li>Verifique se o PDF enviado é o modelo correto</li>
  <li>Confirme se a planilha possui as colunas <strong>Nome</strong> e <strong>E-mail</strong></li>
  <li>Ajuste o valor de <strong>TEXT_BOX_Y</strong></li>
</ul>

<p>A planilha precisa conter exatamente:</p>

<pre><code>
Nome
E-mail
</code></pre>

<hr>

<h2>📄 Licença</h2>

<p>CC0 1.0 Universal</p>
