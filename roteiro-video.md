# Roteiro do Vídeo Pitch — Clyvo Vet (IA)

> Duração de no máximo 5 minutos.

---

## Bloco 1 — Abertura e o problema (0:00–0:40)

Oi, meu nome é Liana e vou apresentar a segunda fase do projeto Clyvo Vet, focada no componente de Inteligência Artificial.

O problema que a gente resolve é simples de entender: animal não fala o que está sentindo. Então, na prática, o responsável só percebe que algo está errado quando o quadro já está avançado — e sem um histórico de saúde estruturado, isso vira diagnóstico tardio na maioria das vezes. Além disso, hoje não existe uma forma rápida de saber quando uma doença está se espalhando numa região, porque cada clínica só enxerga os próprios pacientes.

## Bloco 2 — Proposta da solução (0:40–1:40)

A nossa proposta é que o Clyvo passe a contar com três "vigias" diferentes cuidando da saúde dos animais.

O primeiro, que já existe desde a primeira fase do projeto, compara o animal com ele mesmo — ele sabe, por exemplo, que aquele cachorro específico sempre bebeu 300ml de água por dia, e que hoje ele bebeu só 150.

O segundo, que é novo, sabe o que é esperado pra um animal daquele perfil — raça, idade, peso — e cruza isso com os dados dos sensores. Ele não olha uma informação isolada, ele monta um quadro geral.

E o terceiro, também novo, não olha um animal específico — ele olha uma região inteira, juntando dados de várias clínicas parceiras pra perceber quando uma doença está se espalhando.

Esses três vigias não trabalham separados. Eles se retroalimentam: se a região de um animal está com um alerta ativo, isso pode elevar o risco calculado pra aquele animal específico, mesmo que os sinais dele sozinhos não fossem suficientes.

## Bloco 3 — Papel da IA, com exemplos (1:40–3:10)

Deixa eu mostrar como isso funciona na prática, com dois exemplos.

Primeiro, o Rex, um Labrador. O sistema observa, ao mesmo tempo: o peso dele está 4kg acima do ideal pra raça e idade; ele come mais do que a média esperada; ele se movimenta menos do que o esperado; Labrador é uma raça com tendência conhecida a obesidade; e ele não vai ao veterinário há mais de um ano. Nenhum desses sinais sozinho seria conclusivo, mas juntos formam um padrão claro. O resultado: um alerta alto de risco de obesidade, recomendando consulta veterinária.

Segundo exemplo, a Mel, uma Dachshund de 6 anos. O peso dela está normal — mas o sistema sabe que essa raça tem forte tendência a desenvolver problema de coluna a partir dos 5 anos, e o sensor de movimento mostra uma queda gradual nos últimos dias. Mesmo com o peso normal, essa combinação gera um alerta de possível problema de coluna.

E tem o terceiro vigia, o regional: se várias clínicas parceiras no mesmo bairro registram casos de uma doença nas últimas semanas, o sistema junta essas informações e percebe que o número está bem acima do esperado — e aí dispara um alerta pra toda a região, não só pra um responsável.

## Bloco 4 — Benefícios para o responsável e para a clínica (3:10–4:10)

Pro responsável, o benefício é receber alertas antecipados e já traduzidos em algo simples de entender — tipo "considere agendar uma consulta" — sem precisar interpretar dado técnico nenhum.

Pra clínica e pro veterinário, o benefício é ganhar visibilidade sobre pacientes que precisam de atenção antes de chegarem em estado grave, e ainda receber alertas agregados de vigilância epidemiológica da região, permitindo ação preventiva em vez de só reagir depois que o problema já apareceu.

E pro animal, o benefício final é ter problemas identificados mais cedo, quando o tratamento tende a ser mais simples, mais barato e menos invasivo — com um cuidado calibrado pro perfil dele, não um padrão genérico aplicado a todo mundo.

## Bloco 5 — Arquitetura de funcionamento (4:10–4:50)

Pra fechar, aqui está como tudo isso se conecta [mostrar o diagrama na tela].

O ESP32, com os sensores de peso e movimento, envia os dados pro Thinger.io. Dali, nosso backend grava tudo no banco Oracle, que centraliza tanto os dados do dia a dia — cadastro, consultas, leituras de sensor — quanto os dados de referência que a gente usa pra saber o que é esperado pra cada raça e idade.

Os três vigias consultam esse banco, cruzam as informações, e gravam o resultado numa tabela de alertas. Esses alertas então chegam até o app do responsável e o painel da clínica, fechando o ciclo entre monitorar e agir.

## Encerramento (4:50–5:00)

É isso. Essa é a proposta da Clyvo pra essa fase: transformar dado bruto de sensor e cadastro em inteligência real, que ajuda o responsável, ajuda a clínica, e principalmente ajuda o animal. Obrigado(a)!
