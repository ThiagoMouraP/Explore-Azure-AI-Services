# Explore-Azure-AI-Services
Desafio DIO para testar as funcionalidades do Azure

Explore os serviços de IA do Azure

Os serviços de IA do Azure ajudam os usuários a criar aplicativos de IA com APIs e modelos prontos para uso, pré-construídos e personalizáveis. Neste exercício, você verá um dos serviços, Azure AI Content Safety, no Content Safety Studio.

O Content Safety Studio permite explorar como o conteúdo de texto e imagem pode ser moderado. Você pode executar testes em amostras de texto ou imagens e obter uma pontuação de gravidade que varia de segura a alta para cada categoria. Neste exercício de laboratório, você criará um recurso de serviço único no Content Safety Studio e testará suas funcionalidades.

**Observação O objetivo deste exercício é obter uma noção geral de como os serviços de IA do Azure são provisionados e usados. Segurança de conteúdo é usada como exemplo, mas não se espera que você obtenha um conhecimento abrangente sobre segurança de conteúdo neste exercício!**

Navegue no Content Safety Studio
![image](https://github.com/ThiagoMouraP/Explore-Azure-AI-Services/assets/43223265/155f8d1d-0330-4ba1-bb50-310c8d96350b)

1. Abra o Content Safety Studio (https://contentsafety.cognitive.azure.com/?azure-portal=true). Se não estiver logado, você precisará fazer login. Selecione **Entrar** no canto superior direito da tela. Use o email e a senha associados à sua assinatura do Azure para entrar.

2. O Content Safety Studio é configurado como muitos outros estúdios para serviços de IA do Azure. No menu na parte superior da tela, clique no ícone à esquerda do *Azure AI*. Você verá uma lista suspensa de outros estúdios projetados para desenvolvimento com os serviços de IA do Azure. Você pode clicar no ícone novamente para ocultar a lista.
   ![image](https://github.com/ThiagoMouraP/Explore-Azure-AI-Services/assets/43223265/ede9dddc-e698-4fba-acbc-70ccc97e1327)

Associar um recurso ao estúdio
Antes de utilizar o estúdio, é necessário associar um recurso de serviços Azure AI ao estúdio. Dependendo do estúdio, você pode achar que precisa de um recurso específico de serviço único ou pode usar um recurso geral de vários serviços. No caso do Content Safety Studio, você pode usar o serviço criando um recurso de segurança de conteúdo de serviço único ou um recurso geral de vários serviços do Azure AI . Nas etapas abaixo, criaremos um recurso de segurança de conteúdo de serviço único.

1. No canto superior direito da tela, clique no ícone **Configurações**.
![image](https://github.com/ThiagoMouraP/Explore-Azure-AI-Services/assets/43223265/55f0592d-9423-4fd9-9071-e76b602897e4)
2. Na página **Configurações**, você verá uma guia Diretório e uma guia Recursos . Na guia Recurso , selecione **Criar um novo recurso**. Isso leva você à página para criar um recurso no Portal do Azure.
  Nota: A guia Diretório permite que os usuários selecionem diferentes diretórios a partir dos quais criar recursos. Você não precisa alterar suas configurações, a menos que queira usar um diretório diferente.
![image](https://github.com/ThiagoMouraP/Explore-Azure-AI-Services/assets/43223265/75cc2ce0-6837-47e0-a06b-a685e571a026)

1. Na página Criar Segurança de Conteúdo no Portal do Azure (https://portal.azure.com/?auzre-portal=true), você precisa configurar vários detalhes para criar seu recurso. Configure-o com as seguintes configurações:
  Assinatura: sua assinatura do Azure.
  Grupo de recursos : Selecione ou crie um grupo de recursos com um nome exclusivo.
  Região: Escolha qualquer região disponível.
  Nome: Insira um nome exclusivo.
  Nível de preços: F0 grátis
2. Selecione **Revisar + Criar** e revise a configuração. Em seguida, selecione **Criar**. A tela indicará quando a implantação for concluída.

*Parabéns! Você acabou de criar ou provisionar um recurso de serviços de IA do Azure. Aquele que você provisionou em particular é um recurso de serviço de Segurança de Conteúdo de serviço único.*

1. Quando a implantação for concluída, abra uma nova guia e retorne ao Content Safety Studio (https://contentsafety.cognitive.azure.com/?azure-portal=true).

2. Selecione o ícone **Configurações** no canto superior direito da tela novamente. Desta vez, você verá que seu recurso recém-criado foi adicionado à lista.

3. Na página Configurações do Content Safety Studio, selecione o recurso de serviço Azure AI que você acabou de criar e clique em **Usar recurso** na parte inferior da tela. Você será levado de volta à página inicial do estúdio. Agora você pode começar a usar o estúdio com o recurso recém-criado.

Experimente a moderação de texto no Content Safety Studio

1. Na página inicial do Content Safety Studio, em Executar testes de moderação , navegue até a caixa **Moderar conteúdo de texto** e clique em **Experimentar**.
2. Em executar um teste simples, clique em **Conteúdo seguro**. Observe que o texto é exibido na caixa abaixo.
3. Clique em **Executar teste**. A execução de um teste chama o modelo de aprendizagem profunda do Content Safety Service. O modelo de aprendizagem profunda já foi treinado para reconhecer conteúdo inseguro.
4. No painel Resultados , inspecione os resultados. Existem quatro níveis de gravidade, de seguro a alto, e quatro tipos de conteúdo prejudicial. O serviço Content Safety AI considera esta amostra aceitável ou não? O que é importante observar é que os resultados estão dentro de um intervalo de confiança. Um modelo bem treinado, como um dos modelos prontos para uso do Azure AI, pode retornar resultados que têm uma alta probabilidade de corresponder ao que um humano rotularia o resultado. Cada vez que você executa um teste, você chama o modelo novamente.
5. Agora tente outra amostra. Selecione o texto em Conteúdo violento com erros ortográficos. Verifique se o conteúdo é exibido na caixa abaixo.
6. Clique em Executar teste e inspecione os resultados no painel Resultados novamente.

Você pode executar teste em todas as amostras fornecidas e depois inspecionar os resultados.

Confira as chaves e o endpoint

Esses recursos que você testou podem ser programados em todos os tipos de aplicativos. As chaves e o endpoint usados para o desenvolvimento de aplicativos podem ser encontrados no Content Safety Studio e no Portal do Azure.
1. No Content Safety Studio, navegue de volta para a página **Configurações**, com a guia *Recursos* selecionada. Procure o recurso que você usou. Role para ver o endpoint e a chave do seu recurso.
2. No Portal do Azure, você verá que estes são o mesmo ponto final e chaves diferentes para o seu recurso. Para conferir, acesse o Portal do Azure. Pesquise *Segurança de Conteúdo* na barra de pesquisa superior. Encontre seu recurso e clique nele. No menu à esquerda, procure em *Resource Management for Keys and Endpoints*. Selecione **Chaves e Pontos Finais** para visualizar o ponto final e as chaves do seu recurso.

Depois de terminar, você poderá excluir o recurso Segurança de Conteúdo do Portal do Azure. Eliminar o recurso é uma forma de reduzir os custos acumulados quando o recurso existe na subscrição. Para fazer isso, navegue até a página **Visão geral** do seu recurso Segurança de conteúdo. Selecione **Excluir** na parte superior da tela.



Explore o Machine Learning Automatizado no Azure Machine Learning

Neste exercício, você usará o recurso de aprendizado de máquina automatizado do Azure Machine Learning para treinar e avaliar um modelo de aprendizado de máquina.

Crie um espaço de trabalho do Azure Machine Learning

Para utilizar o Azure Machine Learning, é necessário aprovisionar um espaço de trabalho do Azure Machine Learning na sua subscrição do Azure. Depois, você poderá usar o estúdio Azure Machine Learning para trabalhar com os recursos do seu workspace.

Dica: se você já tiver um espaço de trabalho do Azure Machine Learning, poderá usá-lo e pular para a próxima tarefa.

1. Entre no portal do Azure (https://portal.azure.com/), usando suas credenciais da Microsoft;
2. Selecione + Criar um recurso, pesquisa Machine Learning e crie um novo recurso do Azure Machine Learning com as seguintes configurações:
   Assinatura : sua assinatura do Azure .
   Grupo de recursos : Crie ou selecione um grupo de recursos .
   Nome : Insira um nome exclusivo para seu espaço de trabalho .
   Região : Selecione a região geográfica mais próxima .
   Conta de armazenamento : observe a nova conta de armazenamento padrão que será criada para seu espaço de trabalho .
   Cofre de chaves : Observe o novo cofre de chaves padrão que será criado para seu espaço de trabalho .
   Insights de aplicativo : observe o novo recurso padrão de insights de aplicativo que será criado para seu espaço de trabalho .
   Registro de contêiner : Nenhum ( um será criado automaticamente na primeira vez que você implantar um modelo em um contêiner ).
3. Selecione Revisar + criar e selecione Criar . Aguarde a criação do seu espaço de trabalho (pode demorar alguns minutos) e, em seguida, vá para o recurso implantado.
4. Selecione Launch Studio (ou abra uma nova guia do navegador e navegue até https://ml.azure.com e entre no Azure Machine Learning Studio usando sua conta da Microsoft). Feche todas as mensagens exibidas.
5. No estúdio Azure Machine Learning, você deverá ver seu espaço de trabalho recém-criado. Caso contrário, selecione Todos os espaços de trabalho no menu à esquerda e selecione o espaço de trabalho que você acabou de criar.

Use aprendizado de máquina automatizado para treinar um modelo

O aprendizado de máquina automatizado permite que você experimente vários algoritmos e parâmetros para treinar vários modelos e identificar o melhor para seus dados. Neste exercício, você usará um conjunto de dados de detalhes históricos de aluguel de bicicletas para treinar um modelo que prevê o número de aluguel de bicicletas esperado em um determinado dia, com base em características sazonais e meteorológicas.

1. No Azure Machine Learning Studio (https://ml.azure.com/?azure-portal=true), veja a página Automated ML (em Authoring ).
2. Crie um novo trabalho de ML automatizado com as seguintes configurações, usando Next conforme necessário para avançar pela interface do usuário:
   Configurações básicas :
      Nome do trabalho : mslearn-bike-automl
      Novo nome do experimento : mslearn-bike-rental
      Descrição : Aprendizado de máquina automatizado para previsão de aluguel de bicicletas
      Marcadores : nenhum
   
   Tipo de tarefa e dados :
      Selecione o tipo de tarefa : Regressão
      Selecionar conjunto de dados : crie um novo conjunto de dados com as seguintes configurações:
         Tipo de dados :
         Nome : aluguel de bicicletas
         Descrição : dados históricos de aluguel de bicicletas
         Tipo : Tabular
         Fonte de dados :
         Selecione Dos arquivos da web
         URL da Web :
         URL da Web :https://aka.ms/bike-rentals
         Ignorar validação de dados : não selecionar
         Configurações :
         Formato de arquivo : Delimitado
         Delimitador : Vírgula
         Codificação : UTF-8
         Cabeçalhos de coluna : apenas o primeiro arquivo possui cabeçalhos
         Pular linhas : Nenhum
         O conjunto de dados contém dados multilinhas : não selecione
      Esquema :
         Incluir todas as colunas exceto Caminho
         Revise os tipos detectados automaticamente
      Selecione Criar . Após a criação do conjunto de dados, selecione o conjunto de dados de aluguel de bicicletas para continuar a enviar o trabalho de ML automatizado.
   
   Configurações de tarefa :
   
      Tipo de tarefa : Regressão
      Conjunto de dados : aluguel de bicicletas
      Coluna de destino : Aluguéis (inteiro)
      Configurações adicionais :
         Métrica primária : raiz do erro quadrático médio normalizado
         Explique o melhor modelo : Não selecionado
         Usar todos os modelos suportados : Desmarcado . Você restringirá o trabalho para tentar apenas alguns algoritmos específicos.
         Modelos permitidos : Selecione apenas RandomForest e LightGBM — normalmente você gostaria de tentar o máximo possível, mas cada modelo adicionado aumenta o tempo necessário             para executar o trabalho.
      Limites : expanda esta seção
         Máximo de testes : 3
         Máximo de testes simultâneos : 3
         Máximo de nós : 3
         Limite de pontuação da métrica : 0,085 ( para que, se um modelo atingir uma pontuação da métrica de erro quadrático médio normalizado de 0,085 ou menos, o trabalho termina. )
         Tempo limite : 15
         Tempo limite de iteração : 15
         Habilitar rescisão antecipada : selecionado
      Validação e teste :
         Tipo de validação : divisão de validação de trem
         Porcentagem de dados de validação : 10
         Conjunto de dados de teste : Nenhum
   Calcular :
      Selecione o tipo de computação : sem servidor
      Tipo de máquina virtual : CPU
      Camada de máquina virtual : Dedicada
      Tamanho da máquina virtual : Standard_DS3_V2*
      Número de instâncias : 1
   * Se a sua assinatura restringir os tamanhos de VM disponíveis para você, escolha qualquer tamanho disponível.
3. Envie o trabalho de treinamento. Ele inicia automaticamente.
4. Espere o trabalho terminar. Pode demorar um pouco – agora pode ser um bom momento para uma pausa para o café!

Avalie o melhor modelo

Quando o trabalho automatizado de aprendizado de máquina for concluído, você poderá revisar o melhor modelo treinado.
1. Na guia **Visão geral** do trabalho automatizado de aprendizado de máquina, observe o melhor resumo do modelo.
   ![image](https://github.com/ThiagoMouraP/Explore-Azure-AI-Services/assets/43223265/35d353d8-c0e6-4190-91e7-ced46021f922)
   Observação: Você poderá ver uma mensagem com o status “Aviso: pontuação de saída especificada pelo usuário alcançada…”. Esta é uma mensagem esperada. Continue para a próxima etapa.
2. Selecione o texto em Nome do algoritmo do melhor modelo para visualizar seus detalhes.
3. Selecione a guia Métricas e selecione os gráficos residuais e predito_true se eles ainda não estiverem selecionados.
   Revise os gráficos que mostram o desempenho do modelo. O gráfico de resíduos mostra os resíduos (as diferenças entre os valores previstos e reais) como um histograma. O gráfico          predito_true compara os valores previstos com os valores verdadeiros.

Implantar e testar o modelo

1. Na guia Modelo do melhor modelo treinado pelo seu trabalho automatizado de machine learning, selecione Implantar e use a opção de serviço Web para implantar o modelo com as seguintes configurações:
   Nome : prever-aluguéis
   Descrição : Prever aluguel de bicicletas
   Tipo de computação : Instância de Contêiner do Azure
   Habilitar autenticação : selecionado
2. Aguarde o início da implantação – isso pode levar alguns segundos. O status de implantação do endpoint de previsão de aluguel será indicado na parte principal da página como Running .
3. Aguarde até que o status da implantação mude para Succeeded . Isso pode levar de 5 a 10 minutos.


Testar o serviço implantado

Agora você pode testar seu serviço implantado.
1. No estúdio Azure Machine Learning, no menu esquerdo, selecione Endpoints e abra o ponto final em tempo real de previsão de alugueres .
2. Na página do endpoint em tempo real de previsão de aluguel, visualize a guia Teste .
3. No painel Dados de entrada para testar o endpoint , substitua o modelo JSON pelos seguintes dados de entrada:

Código
 {
   "Inputs": { 
     "data": [
       {
         "day": 1,
         "mnth": 1,   
         "year": 2022,
         "season": 2,
         "holiday": 0,
         "weekday": 1,
         "workingday": 1,
         "weathersit": 2, 
         "temp": 0.3, 
         "atemp": 0.3,
         "hum": 0.3,
         "windspeed": 0.3 
       }
     ]    
   },   
   "GlobalParameters": 1.0
 }
4. Clique no botão Testar .
5. Revise os resultados do teste, que incluem um número previsto de aluguéis com base nos recursos de entrada - semelhante a este:

Código
 {
   "Results": [
     444.27799000000000
   ]
 }
 
O painel de teste pegou os dados de entrada e usou o modelo treinado para retornar o número previsto de aluguéis.

Vamos revisar o que você fez. Você usou um conjunto de dados históricos de aluguel de bicicletas para treinar um modelo. O modelo prevê o número de alugueres de bicicletas esperados num determinado dia, com base em características sazonais e meteorológicas .


Limpar

O serviço web que você criou está hospedado em uma instância de contêiner do Azure . Se não pretender experimentá-lo ainda mais, deverá eliminar o ponto final para evitar acumular utilização desnecessária do Azure.

1. No estúdio Azure Machine Learning , na guia Endpoints , selecione o ponto de extremidade de previsão de aluguel . Em seguida, selecione Excluir e confirme que deseja excluir o endpoint.
   Excluir sua computação garante que sua assinatura não será cobrada por recursos de computação. No entanto, será cobrada uma pequena quantia pelo armazenamento de dados, desde que o      espaço de trabalho do Azure Machine Learning exista na sua assinatura. Se tiver terminado de explorar o Azure Machine Learning, poderá eliminar o espaço de trabalho Azure Machine        Learning e os recursos associados.

Para excluir seu espaço de trabalho:

1. No portal Azure , na página Grupos de recursos , abra o grupo de recursos que especificou ao criar o seu espaço de trabalho Azure Machine Learning.
2. Clique em Excluir grupo de recursos , digite o nome do grupo de recursos para confirmar que deseja excluí-lo e selecione Excluir .
