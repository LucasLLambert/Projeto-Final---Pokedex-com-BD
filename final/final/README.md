# Pokédex com Banco de Dados

Projeto final de DS: Pokédex em Python com SQLite e interface em Streamlit.

## Como rodar
```bash
pip install -r requirements.txt
streamlit run gerenciamento.py
```
O navegador abre em http://localhost:8501.

## Funcionalidades
- **Cadastro**: o usuário digita todos os dados do Pokémon; só a imagem vem da API (PokeAPI), é baixada e gravada no banco (BLOB).
- **Consulta**: busca por nome, número da Pokédex ou tipo.
- **Edição e exclusão** dos Pokémon cadastrados.
- **PC Storage**: caixas com 30 Pokémon cada.

## Estrutura (Interface + POO)
| Pasta/arquivo | Papel |
|---|---|
| `classes/pokemon.py` | Classe `Pokemon` (modelo) |
| `repositorio/repositorio.py` | Interface `IPokemonRepository` e implementação `PokemonRepositorySQLite` (uma única tabela `pokemon`) |
| `api/imagem_service.py` | Interface `ImagemPokemonService` |
| `api/pokeapi_imagem_service.py` | Implementação que baixa a imagem da PokeAPI |
| `gerenciamento.py` | Telas em Streamlit |
| `pokedex.db` | Banco SQLite com os Pokémon cadastrados |
