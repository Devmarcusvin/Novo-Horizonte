# Projeto Além do Horizonte

## 1. Identidade da equipe

- **Nome da equipe:** Além do Horizonte
- **Integrantes mencionados:** Marcus, Thayná e Rafael


## 2. Contexto

O projeto foi criado para o **Pôr do Sol**, estabelecimento frequentado por Marcus. Marcus também possui experiência como garçom e conhecimentos ligados ao setor elétrico, contribuindo com uma visão operacional e energética do negócio.

O Sr. Arthur informou uma despesa aproximada de **R$ 10.000 por mês com energia elétrica**. Esse valor precisa ser confirmado pelas últimas 12 faturas para identificar consumo em kWh, grupo tarifário, demanda, impostos e outros componentes.

O limite do desafio é de **R$ 20.000**. A proposta é conceitual e executável, mas nenhuma instalação será realizada agora. A implantação dependerá de contratação, vistoria, projeto técnico e autorização do estabelecimento.

## 3. Problema central

O Pôr do Sol possui gastos elevados com energia e água. Os equipamentos de refrigeração funcionam continuamente, enquanto informações operacionais importantes podem ficar concentradas no proprietário e não chegar de forma simples à equipe.

**Frase do problema:**

> A equipe está perto do freezer, mas longe da informação.

A avaliadora informou que muitas equipes estão desenvolvendo sistemas de alerta. Por isso, **alertar não pode ser o único diferencial**.

## 4. Conceito principal

### PDS Regenera

Uma solução integrada para reduzir custos, identificar desperdícios, melhorar a operação dos equipamentos, reaproveitar recursos e representar o funcionamento do bar em um gêmeo virtual.

**Slogan:**

> O frio preserva. O calor retorna. A energia se transforma.

**Mensagem competitiva:**

> Outros sistemas avisam quando há desperdício. O nosso evita, recupera e transforma.

A solução deve seguir quatro princípios:

1. **Antecipar:** preparar a operação antes dos horários de pico.
2. **Proteger:** orientar a equipe para reduzir perdas térmicas.
3. **Recuperar:** estudar o aproveitamento do calor e da água.
4. **Transformar:** converter dados em economia e ação operacional.

---

# 5. Energia elétrica

## 5.1 Energia renovável por assinatura

A estratégia financeira mais impactante é buscar uma comercializadora ou serviço de energia renovável com **desconto contratual mínimo de 25% sobre a parcela elegível da fatura**.

### Simulação

Se os 25% incidirem sobre toda a conta de R$ 10.000:

- economia mensal: **R$ 2.500**;
- pagamento restante: **R$ 7.500**;
- economia anual: **R$ 30.000**.

Se somente R$ 8.000 forem elegíveis:

- economia mensal: **R$ 2.000**;
- pagamento total aproximado: **R$ 8.000**;
- economia anual: **R$ 24.000**.

### Linguagem correta

Não afirmar que a economia já está garantida. Apresentar assim:

> A proposta estabelece como condição de contratação um desconto mínimo de 25% sobre a parcela elegível da fatura.

A contratação precisa confirmar:

- atendimento no Distrito Federal;
- compatibilidade com a Neoenergia Brasília;
- parcela elegível da fatura;
- existência de uma ou duas cobranças;
- prazo para início dos créditos;
- fidelidade e multa;
- taxa de adesão;
- bandeiras, impostos e encargos não compensáveis.

## 5.2 Painéis solares próprios

Também foi analisado um sistema com **seis painéis de 580 W**.

### Estimativa

- potência total: **3,48 kWp**;
- geração mensal estimada: **410 a 460 kWh**;
- economia mensal estimada: **R$ 380 a R$ 550**;
- economia anual: **R$ 4.560 a R$ 6.600**;
- redução aproximada da conta: **4% a 5,5%**;
- área aproximada: **18 a 24 m²**.

Para reduzir aproximadamente 50% da conta, seriam necessários, de forma preliminar:

- **32 a 38 kWp**;
- cerca de **56 a 66 módulos de 580 W**;
- investimento aproximado de **R$ 80 mil a R$ 118 mil**.

### Decisão recomendada

Dentro dos R$ 20 mil, a assinatura de energia tende a gerar impacto financeiro maior do que a instalação de apenas seis placas. Os painéis próprios podem ser apresentados como expansão futura.

---

# 6. Refrigeração

## 6.1 Semáforo binário

O sistema terá dois estados principais:

- **Verde:** pode abrir.
- **Vermelho:** mantenha fechado.

O vermelho pode indicar recuperação térmica ou necessidade de verificação. Não significa automaticamente que o freezer está quebrado.

### Mensagens do display

**Normal:**

```text
FREEZER LIBERADO
PODE ABRIR
```

**Recuperação:**

```text
MANTENHA FECHADO
RECUPERANDO
```

**Crítico:**

```text
TEMP. CRITICA
VERIFIQUE AGORA
```

**Falha de leitura:**

```text
SENSOR SEM SINAL
VERIFIQUE AGORA
```

## 6.2 Alarme sonoro

O buzzer será reservado para:

- temperatura crítica persistente;
- sensor sem comunicação;
- aquecimento contínuo;
- alerta sem reconhecimento.

O buzzer não deve tocar em toda recuperação normal, evitando fadiga de alertas.

## 6.3 Reconhecimento por senha

A senha pode ser exigida para:

- reconhecer alerta crítico;
- silenciar temporariamente o buzzer;
- alterar limites;
- entrar em configurações;
- registrar ação administrativa.

A senha não normaliza o equipamento. Enquanto a condição crítica continuar, a luz permanece vermelha.

## 6.4 ESP32 e Arduino

O ESP32 é mais adequado por possuir Wi-Fi. Funções previstas:

- ler temperatura;
- calcular tendência de aquecimento;
- medir tempo de porta aberta;
- controlar LEDs, buzzer e display;
- enviar dados ao sistema;
- registrar ocorrências.

O ESP32 é parte da infraestrutura, não o diferencial principal. Nenhuma placa deve ser ligada diretamente à rede elétrica dos equipamentos sem isolamento, medidores adequados, caixa protegida e instalação profissional.

---

# 7. Diferencial além dos alertas

## 7.1 Pré-resfriamento e inércia térmica

Antes do horário de maior movimento, o sistema pode recomendar uma preparação operacional:

- realizar reposição de bebidas antes do pico;
- reduzir aberturas durante a recuperação;
- agrupar retiradas;
- comparar o tempo de recuperação dos equipamentos;
- identificar equipamentos com desempenho inferior.

A proposta não deve prometer controle automático do compressor sem avaliação técnica e autorização do fabricante.

## 7.2 Recuperação do calor dos freezers

Os equipamentos retiram calor de seu interior e descartam esse calor no ambiente pelo condensador. O projeto pode prever um estudo técnico para utilizar um trocador de calor e pré-aquecer água destinada a usos compatíveis.

Possíveis destinos:

- lavagem de áreas externas;
- limpeza de pisos;
- processos não potáveis autorizados;
- pré-aquecimento antes de outro sistema.

A recuperação de calor depende de vistoria, projeto de refrigeração, avaliação sanitária e compatibilidade dos equipamentos.

## 7.3 Inspiração internacional

A **Dinamarca** foi escolhida como referência conceitual por integrar eficiência energética, refrigeração, medição inteligente e recuperação de calor.

Formulação segura:

> A Dinamarca é uma referência para nossa proposta por integrar eficiência, refrigeração e reaproveitamento de calor.

Não afirmar que o país possui oficialmente os botecos mais eficientes do mundo.

---

# 8. Piezoelétrico

O piso piezoelétrico é tecnicamente possível, mas gera pouca energia. Seu melhor uso é como recurso de engajamento e demonstração.

## Piso Vivo Pôr do Sol

A pressão das pisadas gera pequenas cargas elétricas que podem ser armazenadas e utilizadas para:

- acender LEDs;
- alimentar sinalização de baixo consumo;
- contar fluxo de pessoas;
- criar uma experiência sustentável na entrada;
- mostrar energia simbólica acumulada.

**Mensagem:**

> Sua energia também movimenta o Pôr do Sol.

O piso não deve ser apresentado como capaz de alimentar freezers, bombas ou reduzir significativamente a conta.

---

# 9. Água

## 9.1 Monitoramento e detecção de vazamentos

Arduino ou ESP32 podem trabalhar com:

- sensor de vazão;
- transdutor de pressão;
- sensores de água no piso;
- sensores de nível;
- válvula motorizada opcional.

A detecção mais confiável combina vazão, pressão, presença de água e histórico de uso.

Mensagem correta:

> Possível vazamento ou consumo não registrado.

Não declarar vazamento confirmado somente por uma queda de pressão.

## 9.2 Reúso de água

Fontes mais adequadas:

- condensação de aparelhos de ar-condicionado;
- água da chuva;
- lavatórios selecionados;
- fontes previamente analisadas.

A água da cozinha não deve entrar no piloto inicial devido a gordura, restos de alimentos e detergentes.

### Usos permitidos

- lavagem de pisos;
- limpeza externa;
- irrigação ornamental;
- lavagem de calçadas;
- descargas sanitárias, se houver rede separada e aprovada.

### Usos proibidos

- beber;
- preparar alimentos;
- fabricar gelo;
- lavar copos e talheres;
- higienizar as mãos;
- limpar superfícies em contato direto com alimentos.

### Fluxo do reúso

```text
Captação
   ↓
Reservatório de água coletada
   ↓
Filtro de resíduos
   ↓
Filtro de sedimentos
   ↓
Carvão ativado
   ↓
Desinfecção
   ↓
Reservatório tratado
   ↓
Bomba
   ↓
Rede não potável identificada
```

## 9.3 Orçamento de R$ 8 mil

O piloto conceitual inclui:

- dois reservatórios de 500 litros;
- filtro inicial;
- filtro de sedimentos;
- carvão ativado;
- desinfecção;
- unidade UV dimensionada;
- bomba;
- ESP32;
- sensores de nível;
- medidor de vazão;
- sensor de vazamento;
- válvulas e registros;
- tubulação identificada;
- instalação, projeto e testes;
- reserva técnica.

## 9.4 Meta de economia

Para economizar aproximadamente **R$ 1.000 por mês**, foi estimada a necessidade de reutilizar cerca de:

- **24 mil litros mensais**, se a redução atingir água e esgoto;
- aproximadamente **920 litros por dia**, considerando 26 dias;
- meta operacional arredondada de **1.000 litros por dia**.

Frase para a apresentação:

> Reutilizando mil litros por dia, o Pôr do Sol pode economizar até R$ 1 mil por mês.

Essa é uma economia potencial, dependente da conta real da Caesb, da tarifa, da cobrança de esgoto, da disponibilidade de água para captação e da demanda não potável.

---

# 10. Gêmeo virtual

O gêmeo virtual será uma representação operacional 2D, e não uma instalação já executada.

## Informações principais

- equipamentos refrigerados;
- temperatura e estado térmico;
- porta aberta ou fechada;
- consumo energético;
- falha de comunicação;
- fluxo e pressão da água;
- volume reaproveitado;
- ocorrências e ações da equipe.

## Simplificação visual

A tela principal deve evitar textos pequenos e excesso de cards. Manter quatro indicadores grandes:

1. **Consumo atual**
2. **Equipamentos eficientes**
3. **Calor recuperável**
4. **Economia potencial**

Quando não houver medição real, mostrar:

> Calculado após vistoria.

Todos os números simulados devem receber a identificação:

> Simulação conceitual baseada na arquitetura proposta.

## Modos de apresentação

### Agora

Estado dos equipamentos e ação recomendada.

### Oportunidade

Perdas, tempo de recuperação e calor descartado.

### Ciclo Inteligente

```text
Energia
   ↓
Refrigeração
   ↓
Calor recuperável
   ↓
Água de reúso
   ↓
Economia
```

---

# 11. PDS Mesas

O sistema de mesas é uma expansão separada da solução principal de energia e água.

## Maquininha do garçom

- login por PIN;
- 15 mesas;
- estados Livre, Ocupada e Aguardando pagamento;
- abertura da mesa;
- pedidos e categorias;
- conta parcial;
- transferência e junção;
- divisão da conta;
- pagamento simulado;
- encerramento da mesa;
- atualização do estoque.

## Computador do gestor

- acompanhamento das mesas;
- cadastro de produtos;
- estoque e entradas;
- estoque mínimo;
- sugestão de compras;
- relatórios mensais;
- exportação para Power BI;
- histórico e auditoria.

Os dois sistemas devem compartilhar a mesma base de dados em uma implantação futura. O PDS Mesas não deve ocupar o centro do pitch atual sobre energia e água.

---

# 12. Orçamento integrado preliminar

Uma divisão conceitual do limite de R$ 20 mil pode ser:

| Frente | Reserva |
|---|---:|
| Reúso e monitoramento de água | R$ 8.000 |
| Monitoramento energético e térmico | R$ 5.000 |
| Gêmeo virtual, integração e interface | R$ 4.000 |
| Instalação, testes e treinamento | R$ 2.000 |
| Reserva técnica | R$ 1.000 |
| **Total** | **R$ 20.000** |

A energia renovável por assinatura deve ser tratada como contratação externa, preferencialmente sem consumir o orçamento de implantação. Recuperação de calor e piso piezoelétrico precisam ser cotados antes de entrar no escopo contratado.

---

# 13. Estrutura recomendada do pitch

## Problema

> O Pôr do Sol paga cerca de R$ 10 mil por mês em energia e ainda perde recursos que poderiam ser monitorados, recuperados ou reaproveitados.

## Insight

> Alertar é importante, mas alertar sozinho não elimina o desperdício.

## Solução

> O PDS Regenera integra economia contratual, eficiência da refrigeração, recuperação de calor e reúso de água.

## Diferencial

> Outros sistemas avisam. O nosso antecipa, protege, recupera e transforma.

## Demonstração

1. Mostrar o mapa do estabelecimento no gêmeo virtual.
2. Mostrar um freezer em recuperação térmica.
3. Acionar o farol vermelho com a orientação “Mantenha fechado”.
4. Mostrar o reconhecimento da ocorrência pela equipe.
5. Exibir o calor atualmente descartado como oportunidade de recuperação.
6. Mostrar o fluxo de captação, tratamento e reúso da água.
7. Encerrar com economia potencial e plano de contratação.

## Fechamento

> Além do Horizonte transforma desperdício em informação, informação em ação e ação em economia.

---

# 14. Fatos, hipóteses e validações necessárias

## Fatos informados

- O limite do desafio é de R$ 20 mil.
- O Sr. Arthur informou gasto aproximado de R$ 10 mil mensais em energia.
- O Pôr do Sol possui equipamentos de refrigeração e infraestrutura existente que pode ser reaproveitada após avaliação.
- O projeto será apresentado como proposta conceitual, não como instalação executada.

## Hipóteses

- desconto de 25% na parcela elegível da energia;
- reutilização de 1.000 litros de água por dia;
- economia mensal próxima de R$ 1.000 em água e esgoto;
- potencial de recuperação de calor;
- compatibilidade dos equipamentos existentes;
- viabilidade física do piso piezoelétrico.

## Validações antes da contratação

- analisar 12 contas de energia;
- analisar contas da Caesb;
- vistoriar telhado, quadros e equipamentos;
- medir temperatura, potência, vazão e pressão;
- conferir espaço para reservatórios;
- verificar rede hidráulica separada;
- solicitar proposta comercial de energia;
- obter cotações reais;
- consultar profissionais de elétrica, refrigeração e hidráulica;
- confirmar requisitos sanitários e normas aplicáveis.

---

# 15. Prioridades

## Fazer agora

1. Simplificar o gêmeo virtual.
2. Destacar o Ciclo Inteligente.
3. Separar fatos de projeções.
4. Mostrar claramente o diferencial além do alerta.
5. Organizar o orçamento dentro de R$ 20 mil.
6. Ensaiar uma história curta e visual.

## Depois

1. Conseguir proposta de energia com desconto mínimo.
2. Analisar as contas reais.
3. Cotar peças, instalação e manutenção.
4. Dimensionar reúso e recuperação de calor.
5. Refinar o retorno financeiro.

## Somente se sobrar tempo

1. Animação do piso piezoelétrico.
2. Sistema PDS Mesas no pitch.
3. Gráficos detalhados.
4. Funcionalidades administrativas secundárias.

---

## Resumo em uma frase

> **O PDS Regenera reduz custos ao combinar energia renovável, operação térmica inteligente, recuperação de calor e reúso monitorado de água.**
