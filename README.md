# Projeto DragonDiet
* Repositório para projeto em JAVA para aplicação desktop.
* Aplicação para gerenciamento de dietas e progresso para nutricionistas 
* Versão open-source para projeto de disciplina Linguagem de Programação 3

## Decisão de Design
Como implementação inicial, decidi criar as seguintes classes para essa aplicação:
1. Alimentos(abstrata)
2. Usuário
3. Cliente
4. Dieta
5. Progresso
6. Database
7. Classes para interface gráfica(ainda estou estudando)

* A classe Alimentos forncerá o molde para a criação de objetos alimentos. Estudarei banco de dados para conseguir implementar eficientemente um banco de dados para essa aplicação.
* A aplicação irá conter por 'definição de fabrica' alguns alimentos em seu banco de dados. O Usuário(profissional) tem a opção de criar novos alimentos e automaticamente serão armazenados em banco de dados local.
* A seguinte associação será efetuada: Usuário *tem um/tem uns* Cliente. Cliente *tem um* Dieta e *tem um* Progresso. Dieta *tem uns* Alimentos.
* Como não sou experiente com banco de dados, possa ser que a classe *Database* possa ser fragmentada
* A mesma associação de classes será utilizada no esquema do banco de dados por foreign keys.
* Usuário terá login e senha, a senha será armazenada em sha ou md5.
* A classe dieta terá atributos privados (ArrayList's) que conterá os alimentos. Cada atributo representa 1 refeição do dia. Gostaria da viabilidade de o Usuário poder criar uma Dieta com atributos variáveis. Exemplo: O Usuário poderia criar uma dieta com 4,5,6 refeições tendo respectivamente 4,5,6 atributos(É possivel?)
* A classe Alimentos conterá os seguintes atributos: Quantidade de carboidrato(gramas), quantidade de gordura(gramas), quantidade de proteína(gramas), quantidade de calorias(gramas). Essas quantidades são referentes a cada X gramas do alimento, valor X é passado com a criação do alimento. Gostaria de estabelecer um 'link' entre esses atributos, por exemplo, se eu crio um Alimento abóbora com valores a cada 80 g de 25g carboidratos,40g gordura,5g proteína, gostaria que quando o Usuário fosse adicionar esse alimento na dieta de um Cliente, ele podesse estabelecer a quantidade específica do alimento. A quantidade de proteína, carboidrato e gordura iria variar conforme a quantidade que o Usuário colocou com base nos valores pre-definidos do alimento.

