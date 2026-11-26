# Publicação a partir de motores privados

A arquitetura preparada separa três responsabilidades:

1. Motores e integrações calculam no privado. Não enviam código ou credenciais ao navegador.
2. Um exportador privado aprova os campos e publica apenas produtos com esquema estrito e SHA-256 em https://github.com/dsantananet/ignispyro-public-products .
3. O visualizador lê o manifesto público e verifica o hash do produto, sem autenticar nos repositórios privados.

O piloto funciona com o catálogo oficial de estações IPMA. Não são observações em tempo real nem resultados dos motores de risco. O carregamento local de GeoJSON continua disponível.

A publicação é manual nesta fase. O template de automação permanece desativado no privado e não tem credenciais configuradas. O leitor público não recebe tokens nem requer acesso ao código privado.

As páginas antigas e o IGNISPYRO V2 mantêm os seus endereços e serviços. A migração dos motores antigos ainda não foi concluída: há cópias públicas que só podem ser retiradas depois de substituir as dependências e validar os fluxos autenticados. Colocar a origem num repositório privado não oculta algoritmos que continuem a ser enviados em JavaScript para o navegador.

A passagem final deve preservar URLs, confirmar a mesma apresentação e os produtos, verificar atualização recorrente, testar os percursos do V2 e manter a última publicação aprovada para recuperação. Não confundir HTTP 200 com atualização dos dados ou validação científica.
