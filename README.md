# LivroMágico — protótipo com integração WebLLM

## Como testar
1. Publique `index.html` em um host HTTPS (por exemplo, GitHub Pages) ou rode em um servidor local seguro. Não abra por `file://` se o navegador bloquear módulos/WebGPU.
2. Abra o site em uma versão atualizada do Chrome e verifique se o aparelho oferece WebGPU.
3. Crie uma conta de teste.
4. Entre em **Criar livro** e toque em **Carregar IA gratuita**.
5. Na primeira vez, aguarde o download dos arquivos do modelo. Isso pode consumir centenas de MB ou mais e precisa de internet.
6. Informe título/sinopse e gere capítulos. Cada capítulo é salvo localmente após ser concluído.

## Limitações importantes
- Usa WebLLM via CDN e um modelo pequeno compatível disponível na lista prebuilt do WebLLM. A seleção do modelo depende da lista disponibilizada pelo SDK.
- Requer WebGPU e memória/armazenamento suficientes. Nem todo Android/browser é compatível.
- O primeiro carregamento baixa arquivos grandes. Depois, o cache do navegador pode reaproveitá-los.
- A geração é local e não usa API key de nuvem, mas não garante 100–200 páginas em 30 minutos. O protótipo gera até 1000 tokens por capítulo; para um livro realmente longo será preciso ajustar o orçamento de tokens e medir a velocidade do aparelho.
- As contas, créditos e livros continuam no `localStorage` deste navegador; não são multiusuário nem seguros para produção.
- Capa ilustrada por IA, PDF real, venda/pagamentos, backend e administração segura ainda não estão conectados.
- Não coloque senhas reais. Isto é um protótipo de teste, não um serviço pronto para público.

## Referências
- WebLLM: https://github.com/mlc-ai/web-llm
- Documentação: https://webllm.mlc.ai/docs/user/get_started.html
