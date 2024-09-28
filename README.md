# PokeToken

Esse projeto é um contrato inteligente baseado no padrão ERC721, que cria tokens representando Pokémons. Ele permite criar, visualizar e batalhar com Pokémons, utilizando tecnologia blockchain para armazenamento e gerenciamento dos dados. O contrato é escrito em Solidity e implementa funcionalidades para interação entre os tokens de forma segura e transparente.

## 💻 Tecnologias utilizadas no projeto

- 📖[Solidity](https://soliditylang.org/): Linguagem de programação usada para escrever contratos inteligentes no Ethereum.
- 🦊[Metamask](https://metamask.io/): Carteira digital que permite interagir com a blockchain Ethereum.
- ⛵[RemixIDE](https://remix.ethereum.org/): IDE online para desenvolver e testar contratos Solidity.
- 🫕[Ganache](https://trufflesuite.com/ganache/): Simulador de blockchain local para testes e desenvolvimento.
- 🧊[IPFS](https://ipfs.tech/): Sistema de armazenamento de arquivos descentralizado, usado para hospedar imagens dos Pokémons.

## ✨ Funcionalidades principais

- **Criar Novo Pokémon (`createNewPokemon`)**: Permite ao dono do contrato criar novos tokens representando Pokémons. Cada Pokémon tem um nome, nível inicial (1) e uma imagem. A função garante que apenas o dono do contrato possa criar novos Pokémons.
  
- **Batalhar (`battle`)**: Permite que dois Pokémons batalhem. Apenas o dono do Pokémon atacante pode iniciar a batalha. O resultado da batalha é baseado no nível dos Pokémons: o atacante e o defensor recebem incrementos de nível dependendo do resultado.

- **Visualização de Pokémons**: A função pública `pokemons` permite listar todos os Pokémons criados no contrato. A função `ownerOf` permite verificar quem é o dono de um Pokémon específico.

## 🚀 Como utilizar

1. **Clone o repositório**:
   ```bash
   git clone https://github.com/usuario/poketoken.git
   ```

2. **Instale as dependências** (se necessário):
   - Certifique-se de que você possui o `Node.js` e o `Truffle` instalados para gerenciar o ambiente de desenvolvimento.

3. **Compile e implemente o contrato**:
   - Acesse o `Remix IDE`, importe o arquivo `PokeToken.sol`, e faça a compilação do contrato.
   - Conecte sua carteira Metamask e faça o deploy do contrato em uma rede de teste Ethereum.

4. **Interaja com o contrato**:
   - Após o deploy, use as funções `createNewPokemon` para criar novos Pokémons e `battle` para iniciar batalhas entre eles.

## 🔧 Estrutura do Código

- **Contrato ERC721**: O contrato herda de `ERC721` da biblioteca OpenZeppelin, garantindo a conformidade com o padrão de token não fungível (NFT) e fornecendo funcionalidades de segurança como `_safeMint` para criação de tokens.
  
- **Modificadores de Acesso**:
  - `onlyOwnerOf`: Restringe certas ações (como batalhar) para apenas o dono do Pokémon.
  - `gameOwner`: Restrição de criação de novos Pokémons ao criador do contrato.

## 📄 License

Este projeto está licenciado sob a [MIT License](https://opensource.org/licenses/MIT).

## 🤝 Contribuições

Contribuições são bem-vindas! Se você deseja colaborar:
- Faça um fork do projeto.
- Crie uma branch para sua feature: `git checkout -b minha-nova-feature`.
- Envie um pull request.

## 📞 Contato

Se tiver dúvidas ou sugestões, entre em contato via:
- Email: gustavogoncalves3ch@gmail.com
- LinkedIn: [Seu LinkedIn](https://www.linkedin.com/in/gustavohenrique-dev/)
