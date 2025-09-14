# **REPOSITÓRIO COM ANOTAÇÕES DE ESTUDO E PRÁTICAS SOBRE CLOUD AWS**

# TÓPICO: Gerenciamento de Instâncias EC2

  ## 📌 AWS EC2
  - **Instâcias no EC2** são máquinas virtuais armazenadas em cloud.
  - Modelo **IAAS (infraestrutura como serviço)**
  - Etapas para Criação/Execução de uma Instância:
    - Nomear a instância
    - Selecionar uma AMI (Imagem da VM)
    - Escolher o tipo de instância
    - Criar um novo par de chaves
    - Editar regras do seu grupo de segurança
    - Configurar grupo de segurança
    - Especificar configurações de armazenamento
    - Revisar e executar a instância
   ![1a2](https://github.com/user-attachments/assets/593f3f07-5a41-4b37-a9b2-c0dd46bb8800)
     
  - **Dos custos:**
       - **ON-DEMAND**
        - **Flexibilidade:** Você paga pela capacidade computacional hora ou segundo, sem compromissos de longo prazo.
        - **Escalabilidade:** Ideal para cargas de trabalho que mudam de forma variável e precisam de escalabilidade automática, conforme o uso.
        - **Uso:** Indicado para testar novas configurações, desenvolver novos aplicativos e para cargas de trabalho com demanda irregular.
       - **RESERVED**
        - **O que são:** Um compromisso de longo prazo (1 a 3 anos) para um recurso específico, oferecendo descontos significativos em comparação ao On-Demand.  
        - **Prós:** Economia de custos significativa para cargas de trabalho estáveis e previsíveis e capacidade garantida.
        - **Contras:** Exige um compromisso de longo prazo, o que resulta em menos flexibilidade caso suas necessidades mudem.
       - **SPOT**
        - **Desconto:** Oferecem economias de até 90% sobre os preços On-Demand.
        - **Risco de interrupção:** A capacidade pode ser recuperada pela AWS com um aviso de dois minutos.
        - **Uso:** Ideal para aplicativos sem estado, tolerantes a falhas ou que podem ser interrompidos, como:
            - Análise de dados
            - Tarefas em lote
            - Processamento em segundo plano
  
  ---
  
  ## 📌 AMI (Amazon Machine Image)
  - Iimagem que fornece o software para configurar e inicializar uma instância do Amazon EC2. 
  - Permite criar ambientes/instâncias a partir de uma já existente (em execução ou parada).  
  - Pode-se usar AMIs diferentes para iniciar instâncias quando se deseja configurações distintas.  
  - As AMIs podem ser **públicas** ou **privadas**.  
  - As instâncias geradas são **idênticas** à imagem base.  
  <img width="815" height="448" alt="image" src="https://github.com/user-attachments/assets/df4db359-c4ef-4bbb-9063-d351b2d4e62b" />
  
  ---
  
  ## 📌 Snapshots com EBS
  - Serviço de armazenamento em bloco confiável.  
  - Desenvolvido para ser utilizado com instâncias **EC2**.  
  - **Snapshot** é um **backup incremental**. São **cópias point-in-time** dos dados.  
  - Os snapshots do EBS são **armazenados no S3**.  
  - Modelo de serviço: **IaaS (Infrastructure as a Service)**.  
  
  ---
  
  - **Custos Snapshots com EBS:**
    - A cobrança é baseada na **quantidade de dados armazenados**.  
    - Como os snapshots são incrementais, **excluir um snapshot pode não reduzir imediatamente os custos**.  
    - Dados **exclusivos de um snapshot** são removidos ao excluí-lo.  
    - Dados **compartilhados entre snapshots** são preservados.  
  
  ---
  
  ## 📊 Diferença entre Snapshot e AMI
  - **AMI**: backup completo do servidor, incluindo volumes EBS.  
  - **Snapshot**: backup incremental e pontual de um volume específico.
  ---

  ## Arquiteturas (draw.io)
  - EBS
<img width="601" height="506" alt="Armazenamento EBS drawio" src="https://github.com/user-attachments/assets/90ff0d20-c631-45ed-a87a-e638c6bd0128" />

  - S3
<img width="621" height="514" alt="Diagrama DB drawio" src="https://github.com/user-attachments/assets/2ed9c1a1-da8d-4576-90ab-a66fa6d46207" />


