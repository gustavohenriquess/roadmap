# Semana Arquiteto - Full Cycle

[System Design na Prática: Google Drive](https://www.youtube.com/watch?v=bdXdHcGILn0)

[Arquitetura Hexagonal vs Clean Architecture](https://www.youtube.com/watch?v=Fxih_8wiq4U)

[DEFINIÇÕES IMPORTANTES](./Semana%20Arquiteto%20-%20Full%20Cycle/DEFINIÇÕES%20IMPORTANTES.md)

> FOCO em Liderar, Arquitetar e Desenvolve soluções de grande porte.
> 

- Quais as demandas das empresas ?
    - Escalar Operações  (Arquitetura de Solução)
    - Software que dure por longos anos (Aquitetura de Software (não é MVC, MVVC, etc))
    - Entrega a Confiabilidade (DevOps e SRE (Site Reliability Engineering))
    - Combinação e Equilibrio de todas as áreas (Soft Skills)
- Quais as expectativas das empresas?
    - Mais receita
    - Eficiência com menos recursos
    - Menos riscos
    - Profissionais capacitados de VERDADE
- Realidade das empresas
    - Maioria dos projetos já fracassaram por falharem antes de serem iniciados (Arquitetura de solução)
    - Soluções criadas sem levar em conta as restrições de negócios dos clientes (Arquitetura de solução)
    - Sistemas que possuem dificuldades em crescer na mesma velocidade da empresa (Arquitetura de Software)
    - Dificuldade de entregar novas features ao longo do tempo (Arquitetura de Software)
    - Tempo alto entre a feature fica pronta e entrar em produção (DevOps e SRE)
    - Falta de confiabilidade nas métricas e disponibilidade dos sistemas (SRE)
- Dificuldades para alcançar as expectativas e cumprir as demandas
    - Liderança, empreendedorismo e negócio, trabalho em equipe
    - Falta de Visão de alto nível para projetar soluções
    - Falta de maturidade para criar soluções que possam durar muitos anos
    - Falta de padrões de desenvolvimento
    - Má execução de implementações
    - Processos ineficiente e complexo para entrega
    - Baixa observabilidade de todo o ecossistema
    - Falta de medricas especificas para mitigação de riscos e recuperação a falha
- Como se ajudar e se posicionar
    - Sou visto como uma referencia?
    - Projeto soluções que faz sentido em logo prazo?
    - Ser capaz de desenhar um ecossistema de forma expressiva que todos possam entender
    - Ter uma visão 360° de uma solução entendendo suas restrições e necessidades
    - Garantir boas práticas de desenvolvimento
- Realidade
    - Grandes projetos falham antes de serem publicados
    - Dinheiro jogado fora por reescrita de software
    - Solução que não leva em conta as restrições de negócios
    - Sistemas possuem dificuldades para crescer na mesma velocidade que a empresa
- Porque alcançar isto é difícil ?
    - Falta de visão alto nível para projetar soluções
    - Falta de maturidade técnica para criar soluções que vão durar anos
    - Falta de padrões de projeto e desenvolvimento

## System Design - Google Drive

- Mais Leitura ou Gravação
- O que é mais importante: Consistência ou Disponibilidade?  (Teorema CAP)

- Principais Recursos
    - Sincronização entre Client / Server
        - Client avisa o server quando houver alguma mudança e vice e versa
        - Endpoint pelo servidor para leitura dos arquivos (chunks) e tamb[em para gravação
        Chunks: Pedaços de arquivos.

- Requisitos não funcionais
    - Multi-tenancy (pode ter diversos usuários isolados utilizando a mesma aplicação)
    - Baixa latência
    - Resiliência  (dados jamais devem ser perdidos)
    

- Plano de Capacidade
    - DAU (Daily Active Users)
    - Picos de acesso ?
    - Quantos usuários utilizam a aplicação por dia
    - tamanho médio dos arquivos
    - Relação entre R/W
    - Replication Factor
    - Quantos arquivos por usuário por dia

- Exemplo Google Drive
    - 500Mi de usuários e 100M DAU
    - 2x mais do que a media
    - Upload 2 arquivos por dia
    - 1MB e 100kb por cada mudança
    - 1:10
    - 3x
    - 100 arquivos
    

![Untitled](./Semana%20Arquiteto%20-%20Full%20Cycle/Untitled.png)

Arquivo Editável: 

[Semana Arquiteto.excalidraw](./Semana%20Arquiteto%20-%20Full%20Cycle/Semana_Arquiteto.excalidraw)

## Arquitetura Hexagonal vs Clean Archtecture

Robert C. Martin - (Uncle Bob) Blog

[Clean Coder Blog](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html)

![Captura de Tela 2024-06-27 às 13.41.08.png](./Semana%20Arquiteto%20-%20Full%20Cycle/Captura_de_Tela_2024-06-27_as_13.41.08.png)

![Untitled](./Semana%20Arquiteto%20-%20Full%20Cycle/Untitled%201.png)

- Repositórios Utéis
    
    [https://github.com/devfullcycle/mba_fullcycle_design_patterns](https://github.com/devfullcycle/mba_fullcycle_design_patterns)
    
    [https://github.com/devfullcycle/MBA-hexagonal-architecture](https://github.com/devfullcycle/MBA-hexagonal-architecture)
    
    [https://github.com/devfullcycle/mba-domain-driven-design](https://github.com/devfullcycle/mba-domain-driven-design)
    
- Livros sobre os Temas
    
    [Domain-Driven Design: Atacando as Complexidades no Coração do Software](https://www.amazon.com.br/Domain-Driven-Design-Atacando-Complexidades-Software/dp/8550800651/ref=asc_df_8550800651/?tag=googleshopp00-20&linkCode=df0&hvadid=379739109739&hvpos=&hvnetw=g&hvrand=15183659697733918016&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=1001767&hvtargid=pla-809277038576&psc=1&mcid=adb9b45316093284abfc5f620bf43afb)
    
    [Implementando Domain-Driven Design](https://www.amazon.com.br/Implementando-Domain-Driven-design-Vernon/dp/8576089521/ref=asc_df_8576089521/?tag=googleshopp00-20&linkCode=df0&hvadid=379748659420&hvpos=&hvnetw=g&hvrand=15183659697733918016&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=1001767&hvtargid=pla-460804278877&psc=1&mcid=4af905bfed633c81b25d7ebf3f277392)
    
    [Clean Architecture: A Craftsman's Guide to Software Structure and Design](https://www.amazon.com.br/Clean-Architecture-Craftsmans-Software-Structure/dp/0134494164/ref=sr_1_1?adgrpid=80528380799&dib=eyJ2IjoiMSJ9.gg8SRT5zDyWOOcfFXv2zVRHf8g2YswCJ-9pthP6aLrl8gF1JvgQIXazKxFDCS-t1apScxVKNz2o2FiL25DuKpIjo4N2_eDJDdT7s-x6r-2VasB7SkMeJpg6LlzyWZlzFoIbUKw-nug68tla6-lABb2IEhI0rZ9La2unMuPCHktIAqVlapb9j50ypJUMNuWRI_lVyXby30i5IywCUYT2qCiU2Lcyvknu4njBCb1kWVVTVUedNvxnWYnDZJSTuXtb0_T0ltTBjCMTmifhlA9aeIdKwNPsHZTkLTrrWjjqZ7M8.9-er02MwWyRmSCfYa1xQs_h3_XMn2i1MUpewk27aWds&dib_tag=se&hvadid=634265156816&hvdev=c&hvlocphy=9196892&hvnetw=g&hvqmt=e&hvrand=5415081096413063332&hvtargid=kwd-847840762744&hydadcr=5659_13279526&keywords=clean+architecture+uncle+bob&qid=1720003751&sr=8-1)
    

![Untitled](./Semana%20Arquiteto%20-%20Full%20Cycle/Untitled%202.png)