# Pacotes privados, Monorepo, lerna e aceito sugestões de um título melhor

Ao longo do tempo na história do desenvolvimento da codebase da field alguns pedaços de código começaram a ficar duplicados para resolver isso alguns deles se tornaram pacotes como: kate-query, response-easy, client conta azul entre outros.

Essa apresentação é para mostrar a vocês como foi preparado oque vai ser a nova casa dos pacotes privados da field **Blackspech**

Nele foram usados alguns padrões de projeto e ferramentas como:

- github actions
- github package registry
- monorepo
- lerna

Alguns são velhos conhecidos outros nem tanto, vou apresentar os que são novidades e mostrar como tudo funciona junto.

## Monorepo vs Multirepo

O nome é intuitivo

- **Multirepo:** um repositório para cada módulo de um projeto.
- **Monorepo:** vários projetos ou pacotes que são mantidos em uma único repositório.

Se você tem vários projetos que estão relacionados como um web app uma api lambda e worker é comum que uma alteração ou adição de funcionalidade afete afete mais de um módulo.

Caso todos estes projetos estejam juntos em uma única codebase processos como
review e publicação passam a ser facilitados pois o review pode ser feito em um único pr e a publicação de todos os módulos pode ser disparada com um único merge.

É claro que essa prática também tem desvantagens e temos que tomar cuidado
para tudo não virar um grande monólito que não tem divisão cara entre seus módulos.

Vários projetos famosos que usam o padrão de monorepo alguns deles são:

- jest
- Angular
- React
- Babel

## Lerna

Lerna é uma ferramenta para gerenciar monorepos.
Dentre outras coisas ela facilita coias como.

- instalar as dependências nos diferentes múdulos
- gerenciar publicação dos pacotes
- gerar um changelog das alterações automaticamente.

Vou dar mais detalhes de como fazer isso no exemplo pratico

## Github package registry

O GitHub Packages é um registro de pacotes do próprio github ele nos permite publicar pacotes e proporciona uma boa integração com o restante das ferramentas do github permitindo que os fontes e o pacote publicado fiquem juntinhos

## Vamos a prática e a demonstração

https://github.com/FieldControl/blackspeech