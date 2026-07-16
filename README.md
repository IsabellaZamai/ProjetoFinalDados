```markdown
# Projeto Final — Previsão de Preço de Carros Usados

Descrição
- API em Flask que prevê o preço de carros usados usando Regression Linear (scikit-learn).
- Salva histórico de previsões no Supabase.
- Frontend público: calculadora de preço (link abaixo).

Links
- Site (frontend): https://auto-worth-guide.lovable.app
- API (deploy): https://projetofinaldados.onrender.com

Funcionalidades
- Endpoint GET `/` — checagem de status (retorna "API online, Flask rodando corretamente").
- Endpoint POST `/prever` — recebe JSON com campos:
  - ano (int)
  - quilometragem (int)
  - motor (float)
  - num_revisoes (int)
  Retorna `{ "preco": <valor> }` e grava no Supabase.

Estrutura principal
- `app.py` — aplicação Flask, carregamento do dataset `dataset_carros_usados_2.csv`, treinamento do modelo e rotas.
- `dataset_carros_usados_2.csv` — dados usados para treinar o modelo.

Como rodar localmente
1. Criar um virtualenv (recomendado) e ativar.
2. Instalar dependências:
   pip install -r requirements.txt
3. Definir variáveis de ambiente (arquivo `.env`):
   - SUPABASE_URL
   - SUPABASE_KEY
4. Executar:
   python app.py
5. Teste:
   - GET http://localhost:8000/
   - POST http://localhost:8000/prever com JSON conforme campos acima.

Observações
- O modelo é treinado ao iniciar a aplicação; em produção, considerar persistir o modelo treinado.
- Verifique permissões e custo do Supabase ao gravar dados.
- Ajustes de validação de entrada podem ser adicionados para maior robustez.

Licença
- README e código do projeto: revisar conforme necessidade do repositório.
```
