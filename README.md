<h1>Verificação do Tempo de Volta</h1>

<p>Este repositório contém um script Python para verificar os tempos de volta em uma corrida, baseado na média dos tempos das voltas inseridas pelo usuário. O script solicita ao usuário a entrada de valores para os tempos das voltas, calcula a média desses tempos, e determina se a média está dentro do padrão recomendável de 1.16 segundos.</p>

<h2>Integrantes do Grupo</h2>
<ul>
    <li>RICKELMYN DE SOUZA RUESCAS(RM556055)</li>
    <li>GUILHERME CEZARINO SIMÕES(RM557724)</li>
    <li>FABRINI SOAREZ(RM557813)</li>
    <li>VINICIUS DOS SANTOS WINCE (RM557033)</li>
</ul>

<h2>Código do Projeto</h2>
<pre><code>
def obter_tempos(num_voltas):
    # Essa função pega 5 resultados de tempo e os armazena em uma lista (temp_lista) e retorna a lista
    temp_lista = []

    print("Vamos tirar a média de tempo de todas as voltas até agora.\n")

    print("Agora insira o tempo das voltas.\n")
    for i in range(num_voltas):
        temp_voltas = float(input(f"Insira o tempo da volta {i+1}: "))
        print(f"Tempo da volta {i+1}: {temp_voltas}\n")
        temp_lista.append(temp_voltas)

    return temp_lista

def calcular_media(temp_lista):
    # Essa função soma os valores dentro da lista de média e divide pelo tamanho da lista (nesse caso 5).
    media = sum(temp_lista) / len(temp_lista)
    return media

def verificar_media(media, referencia=1.16):
    # Essa função verifica se a média está acima ou abaixo de 1.16 segundos, se estiver abaixo ele retorna que a média está boa
    # caso contrário ele fala que está ruim. Em ambos os casos ele dá a diferença entre a média calculada e a de referência.
    if media < referencia:
        print(f"A média de tempo das voltas é: {media:.2f} segundos.")
        print("A média está boa!")
        diferenca = referencia - media
        print(f"A média está {diferenca:.2f} segundos abaixo da média de referência (1.16 segundos).")
    else:
        print(f"A média de tempo das voltas é: {media:.2f} segundos.")
        print("A média precisa melhorar.")
        diferenca = media - referencia
        print(f"A média está {diferenca:.2f} segundos acima da média de referência (1.16 segundos).")

# Usando as funções
num_voltas = 5  # Número de voltas que você deseja
tempos = obter_tempos(num_voltas)
media = calcular_media(tempos)
verificar_media(media)
</code></pre>

<h2>Estrutura do Código</h2>
<p>O código está organizado em três funções principais que lidam com a coleta dos tempos das voltas, cálculo da média dos tempos e verificação da média em relação a um valor de referência.</p>

<h2>Lista de Funções</h2>
<ul>
    <li>
        <strong>obter_tempos(num_voltas)</strong>: Pede ao usuário os tempos de volta.
        <ul>
            <li>Coleta 5 valores de tempo de volta.</li>
            <li>Armazena os valores em uma lista <code>temp_lista</code>.</li>
            <li>Retorna a lista de tempos.</li>
        </ul>
    </li>
    <li>
        <strong>calcular_media(temp_lista)</strong>: Calcula a média dos tempos fornecidos.
        <ul>
            <li>Recebe uma lista de tempos como parâmetro.</li>
            <li>Calcula a média dos valores na lista.</li>
            <li>Retorna a média calculada.</li>
        </ul>
    </li>
    <li>
        <strong>verificar_media(media, referencia=1.16)</strong>: Verifica se a média está dentro do padrão recomendável.
        <ul>
            <li>Recebe a média calculada e um valor de referência (1.16 segundos).</li>
            <li>Imprime se a média está boa (abaixo de 1.16 segundos) ou se precisa melhorar (acima de 1.16 segundos).</li>
            <li>Calcula e imprime a diferença entre a média calculada e a referência.</li>
        </ul>
    </li>
</ul>

<h2>Requisitos do Sistema</h2>
<p>Para rodar a aplicação, são necessários os seguintes requisitos do sistema:</p>
<ul>
    <li><strong>Sistema Operacional</strong>: Windows 7 ou superior, macOS 10.13 ou superior, ou distribuições Linux modernas.</li>
    <li><strong>Python</strong>: Python 3.6 ou superior.</li>
    <li><strong>Espaço em Disco</strong>: Pelo menos 100 MB de espaço livre.</li>
    <li><strong>Memória RAM</strong>: Pelo menos 1 GB de RAM.</li>
    <li><strong>Outros Requisitos</strong>: Acesso à internet para baixar o Python e outras dependências, se necessário.</li>
</ul>

<h2>Requisitos</h2>
<p>Para rodar o código, você precisa ter o Python e o Visual Studio Code (VSCode) instalados em sua máquina.</p>

<h3>Instalação do Python</h3>
<p>Você pode baixar o Python <a href="https://www.python.org/downloads/">aqui</a>. A versão recomendada é o Python 3.6 ou superior.</p>

<h3>Instalação do Visual Studio Code</h3>
<p>Você pode baixar o Visual Studio Code <a href="https://code.visualstudio.com/">aqui</a>.</p>

<h2>Execução</h2>
<p>Para executar o script utilizando o Visual Studio Code (VSCode), siga os passos abaixo:</p>
<ol>
    <li>Abra o Visual Studio Code.</li>
    <li>Certifique-se de que a extensão do Python está instalada no VSCode. Caso não esteja, você pode instalá-la a partir da aba de extensões.</li>
    <li>Baixe o script Python do repositório e salve-o em um diretório de sua escolha.</li>
    <li>No VSCode, clique em <strong>File &gt; Open Folder</strong> e navegue até o diretório onde o script foi salvo. Abra esse diretório.</li>
    <li>Clique duas vezes no arquivo do script para abri-lo no editor.</li>
    <li>Com o arquivo aberto, clique no botão "Run" no canto superior direito (Símbolo de "Play") ou pressione <strong>F5</strong> para executar o script.</li>
</ol>

<h2>Exemplo de Uso</h2>
<ul>
    <li>O usuário será solicitado a inserir os tempos de volta.</li>
    <li>Para cada volta, o usuário deve fornecer 5 valores de tempo.</li>
    <li>O script calculará a média dos tempos fornecidos.</li>
    <li>Será verificado se a média está dentro do limite recomendável de 1.16 segundos.</li>
    <li>O script exibirá se a média dos tempos está boa ou precisa melhorar, juntamente com a diferença em relação ao valor de referência.</li>
</ul>

<h2>Limitações</h2>
<ul>
    <li>O script não possui validações de entrada robustas e assume que o usuário fornecerá entradas numéricas válidas.</li>
    <li>O limite recomendável de 1.16 segundos é fixo no código e pode precisar de ajustes conforme as normas ou necessidades específicas.</li>
</ul>

<h2>Contribuições</h2>
<p>Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou pull requests para melhorias no código, validações de entrada, ou ajustes nos limites dos parâmetros.</p>
