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
