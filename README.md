# Trabalho-MetodologiasAgeis
# link: https://trello.com/b/7YaGRUsY/trabalho-metodologias-ageis

## Trabalho em Grupo B1-T3
## Implementação de Kanban para um time de desenvolvimento web

## 1. Contexto do produto e do serviço observado
O produto é um sistema de gestão de pedidos para um restaurante, utilizado por diferentes perfis de usuário: administrador (cadastro de produtos, funcionários, mesas e relatórios), garçom (visualização do cardápio, associação de pedidos a mesas, alteração de itens), cozinheiro (visualização dos pedidos recebidos) e atendente (registro de pagamento e finalização da conta).
O serviço observado neste trabalho é o fluxo de desenvolvimento das funcionalidades desse sistema: desde o momento em que uma necessidade é solicitada até o momento em que a funcionalidade correspondente está disponível em produção para os usuários do restaurante.

## 2. Quadro Kanban — mapeamento textual do fluxo
O quadro representa o caminho real de uma funcionalidade dentro do time de desenvolvimento, evitando o modelo genérico "A fazer / Fazendo / Feito". As seis colunas abaixo foram escolhidas por representarem responsabilidades e transições de estado relevantes para a gestão do trabalho:
Coluna	Significado do estado	Marco
Solicitações	Ideia ou necessidade registrada pelo cliente/usuário, ainda não avaliada nem priorizada pelo time.	—
Prontas Para Dev	Item compreendido, com critérios de aceite definidos e priorizado. Ainda não ocupa capacidade de desenvolvimento.	Ponto de Compromisso
Em Andamento	Implementação ativa da funcionalidade pelo desenvolvedor responsável.	—
CodeReview	Código implementado está sendo revisado por outro membro do time antes de seguir para testes.	—
Testes	Validação da funcionalidade contra os critérios de aceite, incluindo testes manuais ou automatizados.	—
Entregues	Funcionalidade validada e disponível para uso no sistema do restaurante.	Ponto de Entrega

## 3. Tipos de trabalho
Para diferenciar a natureza das demandas que chegam ao time, os cartões são classificados por cor conforme a legenda a seguir:
Cor da etiqueta	Tipo de trabalho	Exemplo no quadro
Verde-água	Funcionalidade	"Como garçom, quero visualizar o cardápio (...)"
Vermelho	Defeito	"Corrigir erro ao calcular total da conta quando há desconto"
Roxo	Melhoria técnica	"Otimizar consulta de produtos do cardápio para reduzir tempo de carregamento"
Cinza	Suporte / solicitação operacional	"Restaurar acesso de um funcionário que perdeu a senha"

Essa classificação ajuda o time a responder perguntas como: quantos defeitos estão interrompendo o fluxo de novas funcionalidades? Melhorias técnicas estão sendo sempre adiadas em favor de funcionalidades?

## 4. Limites de WIP
Os limites abaixo foram definidos para as colunas que representam trabalho ativo (não se aplicam a "Solicitações", que é apenas um repositório de ideias, nem a "Entregues", que representa trabalho concluído):
Coluna	Limite de WIP proposto	Situação atual
Prontas Para Dev	3 itens	3 itens — dentro do limite
Em Andamento	3 itens	4 itens — acima do limite (ver observação)
CodeReview	2 itens	2 itens — dentro do limite
Testes	2 itens	1 item — dentro do limite

Observação: a coluna "Em Andamento" está atualmente com 4 itens, um acima do limite proposto de 3. Isso é um sinal para o time parar de puxar novos itens e priorizar a conclusão dos que já estão em progresso antes de iniciar outro — em vez de simplesmente ignorar o limite.

## 5. Bloqueio identificado
O cartão "Como cliente, quero consultar o cardápio digital, para conhecer os produtos e preços disponíveis" está marcado como bloqueado.
•	Motivo: Motivo do bloqueio: aguardando definição do layout do cardápio digital pelo administrador do restaurante.
•	Data: Data de início do bloqueio: 08/09.
•	Próxima ação: Próxima ação: reunião de alinhamento com o administrador do restaurante para validar o layout antes de seguir com a implementação.

## 6. Políticas explícitas
As políticas abaixo orientam como os itens entram, avançam e saem do sistema, reduzindo decisões improvisadas pelo time:
•	Entrada: um item só entra em "Prontas Para Dev" quando os critérios de aceite estiverem completos, o tipo de trabalho estiver classificado e a prioridade estiver definida.
•	Puxada: um desenvolvedor só puxa um item de "Prontas Para Dev" para "Em Andamento" quando houver espaço dentro do limite de WIP da coluna, priorizando sempre os itens de prioridade Alta.
•	Avanço para revisão: um item só avança para "CodeReview" quando todos os critérios da checklist do cartão estiverem marcados como concluídos pelo desenvolvedor.
•	Avanço para testes: um item só avança de "CodeReview" para "Testes" após receber a aprovação de pelo menos um outro membro do time.
•	Tratamento de bloqueio: um item bloqueado recebe a etiqueta "Bloqueado" e deve ter na descrição o motivo, a data de início e a próxima ação necessária; o time discute o bloqueio na reunião diária até sua remoção.
•	Entrega: um item só é movido para "Entregues" após ser validado na coluna "Testes" e estar disponível para uso no ambiente de produção do sistema.

## 7. Justificativa das decisões
As seis colunas escolhidas refletem etapas com responsáveis e critérios de saída diferentes (desenvolvimento, revisão de código e testes são atividades distintas dentro do time), o que as torna relevantes para a gestão do trabalho — diferente de um quadro genérico, que esconderia essas transições.
O time decide qual item puxar com base na prioridade registrada em cada cartão (Alta, Média ou Baixa) e no respeito ao limite de WIP da coluna de destino: um novo item só é iniciado quando há espaço disponível, evitando sobrecarga e multitarefa.
Bloqueios são tratados de forma visível: o cartão recebe uma etiqueta específica e a descrição registra motivo, data e próxima ação, garantindo que o impedimento seja discutido pelo time em vez de ficar escondido até prejudicar o prazo de entrega.
