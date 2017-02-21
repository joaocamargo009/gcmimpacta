Word Press
----------

Versão             - 4.6
Codinome           - Pepper
Data de Lançamento - 16/08/2016
Notas         - Agora tanto os plugins e temas podem ser instalados, atualizados ou  excluídos sem recarregar a página. 
O painel  do  WordPress  agora aproveita as fontes que o  usuário  já  tem,  tornando  o  carregamento mais                      rápido.  O  editor  verifica  automaticamente  erros acidentais  nos  links criados pelo usuário e também                      salva  no  navegador tudo que é digitado, permitindo recuperação a qualquer momento.

Versão             - 4.7
Codinome           - Vaughan
Data de Lançamento - 06/12/2016
Notas              - Foi  adicionado  o tema padrão Twenty Seventeen, que trabalha  com  cabeçalhos  em  vídeo  e  este  mesmo   recurso  pode  ser  usado em outros layouts. Agora o usuário   pode   personalizar   enquanto  instala  o                      sistema. Na  demonstração  ao  vivo,  foi adicionado atalhos em secções do layout para facilitar a edição                      destes. Pode ser criado páginas diretamente enquanto se  cria   menus.  Uma  ótima  ferramente  que  foi                      adicionada  é o CSS customizado, onde o usuário pode adicionar seus próprios estilos diretamente no site,                      sem relação direta com o tema ativo. Para quem gosta de  publicar  arquivos  PDF,  agora  é  possível ver                      em   miniaturas  na  galeria.  Para  quem  gosta  de utilizar    multi    idiomas,   foi   adicionada   a                      possibilidade  de  ter  vários idiomas que o usuário pode escolher ao utilizar o painel do WordPress.


NGINX
-----

Versão             - 1.11.10
Data de Lançamento - 14.02.2017
Notas              - Alteração:  o  formato  do  cabeçalho  do  cache foi alterado, previamente armazenado em cache. As respostas serão invalidadas.

Recurso: suporte de "stale-while0-revalidate" e "stale-if-error"
Extensões na linha de cabeçalho de resposta do back-end "Cache-Control".

Recurso: o "proxy_cache_background_update", "Fastcgi_cache_background_update",                      "scgi_cache_background_update", E "uwsgi_cache_background_update" diretivas.

Recurso: nginx agora é capaz de cache respostas com o "Vary" cabeçalho Até 
128 caracteres (em vez de 42 caracteres em caracteres Versões).
 
Recurso: o parâmetro "build" da diretiva "server_tokens".

Bugfix: "[crit] SSL_write () falhou" mensagens podem aparecer em logs Ao tratar 
solicitações com o cabeçalho de  solicitação "Expect: 100-continue" linha.

Bugfix: o ngx_http_slice_module não funcionou em locais nomeados.

Bugfix: uma falha de segmentação pode ocorrer em um processo de Usando AIO após um redirecionamento "X-                     Accel-Redirect".

Bugfix: consumo reduzido de memória para pedidos de longa duração usando Gzipping

Versão             - 1.11.9
Data de Lançamento - 24.01.2017
Notas              - Bugfix: nginx pode hog CPU ao usar o módulo de fluxo; O bug tinha Apareceu em 1.11.5.

Bugfix: mecanismo de autenticação EXTERNAL no proxy de e-mail foi aceito Mesmo que não tenha sido                      habilitado na configuração.
 
Bugfix: uma falha de segmentação pode ocorrer em um  processo de A diretiva "ssl_verify_client" do módulo                      de fluxo foi usada.

Bugfix: a diretiva "ssl_verify_client" do módulo de fluxo pode não funciona.

Bugfix: fechando conexões keepalive devido a nenhum   trabalhador livre Conexões podem ser muito                      agressivas.

Bugfix: uma resposta incorreta pode ser retornada ao  usar o Diretriz "sendfile" no FreeBSD e no macOS; O                       bug apareceu em 1.7.8.

Bugfix: uma resposta truncada pode ser armazenada no cache ao usar o "Aio_write".

Bugfix: um vazamento de soquete pode ocorrer ao usar o "aio_write" Directiva.

Apache HTTP Server
------------------

Alterações com o Apache 2.4.25

  *) Corrigir alguns problemas de compilação relacionados a vários módulos.
     

Alterações com o Apache 2.4.24

  *) SEGURANÇA: CVE-2016-8740 (cve.mitre.org)
     Mod_http2: Mitigar a exaustão de memória DoS via interminável
     CONTINUAÇÃO.

  *) SEGURANÇA: CVE-2016-5387 (cve.mitre.org)
     Core: Mitigar [f] cgi "httpoxy" questões.

  *) SEGURANÇA: CVE-2016-2161 (cve.mitre.org)
Mod_auth_digest: Impedir segfaults durante a alocação de entrada do cliente quando O espaço de memória compartilhada está esgotado.
     
  *) SEGURANÇA: CVE-2016-0736 (cve.mitre.org)
Mod_session_crypto: Autentica os dados de sessão / cookie com um MAC (SipHash) para evitar decifrar ou adulterar um preenchimento Ataque oracle 

  *) SEGURANÇA: CVE-2016-8743 (cve.mitre.org)
Aplicar gramática de solicitação HTTP correspondente a RFC7230 para linhas de solicitação E cabeçalhos de solicitação, para evitar a divisão da resposta e a poluição Clientes maliciosos ou proxies a jusante. 

  *) Validar a gramática de cabeçalho de resposta HTTP definida pelo RFC7230, resultando Em um erro 500 no caso de conteúdo de cabeçalho de resposta inválido são Detectado ao servir a resposta, para evitar a divisão de resposta e cachê Poluição por clientes mal-intencionados, servidores upstream ou módulos defeituosos.
     
  *) Mod_rewrite: Limite o uso da memória fugitiva por curto-circuito de alguns tipos de Looping RewriteRules quando o caminho local excede LimitRequestLine. 

  *) Mod_ratelimit: Permitir inicial "burst" montante a toda velocidade antes Estrangulamento: PR 60145 

  *) Mod_socache_memcache: Fornece memcache stats para mod_status.

  *) Http_filters: Corrigir looping em novos check_headers () devido a novos Padrão de ap_die () do filtro de cabeçalho http.      Explicitamente Cabeçalhos anteriores e corpo.

  *) Core: Drop Content-Length cabeçalho e mensagem-corpo de HTTP 204 respostas.
     
  *) Mod_proxy: Honra uma exceção ProxyPass com escopo de servidor quando ProxyPass é Configurado em <Location>, como em 2.2. 

  *) Mod_lua: Corrige o valor padrão da diretiva LuaInherit. Deveria ser 'Parent-first' em vez de 'none', conforme documentação. 

  *) Core: Nova diretiva HttpProtocolOptions para controlar a execução de httpd De vários requisitos RFC7230. 

  *) Core: Permitir não codificado ';' Para aparecer em solicitações de proxy e Localização: cabeçalhos de resposta. Corresponde ao comportamento moderno do navegador.

  *) Core: ap_rgetline_core agora puxa de r-> proto_input_filters.

  *) Core: Corretamente analisar uma especificação IPv6 literal host em um absoluto URL na linha de solicitação. 

  *) Core: Nova diretiva RegisterHttpMethod para registro não-padrão Métodos HTTP. 

  *) Mod_socache_memcache: Passar o tempo de expiração até memcached.

  *) Mod_cache: Use o caminho URI real e query-string para identificar o Em cache (chave), de forma que as reescritas sejam levadas em conta quando Executando depois (CacheQuickHandler off). 

  *) Mod_http2: nova diretiva 'H2EarlyHints' para habilitar o envio de status HTTP 103 respostas provisórias. Desativado por padrão.      

  *) Mod_ssl: Fix renegociação rápida (OptRenegotiaton) sem intermediário Na cadeia de certificados do cliente.

  *) Event: Permitir usar todo o placar atribuído (até ServerLimit Slots) para evitar erros no placar quando alguns processos estão terminando graciosamente. Além disso, faça com que os processos de acabamento Manter-vivo conexões. 

  *) Mpm_event: Não aproveite os slots do placar para terminar graciosamente tópicos. 

  *) Mpm_event: Memória livre anterior ao encerrar processos.

  *) Mod_status: Exibe o número do slot de processo na conexão async Visão geral. 

  *) Mod_dir: Respostas que passam por "FallbackResource" podem aparecer para Pendurar devido à codificação fragmentada não terminada. 

  *) Mod_dav: Corrigir uma causa potencial de uso de memória ilimitada ou incorreta Comportamento em uma rotina que envia <DAV: response> 's para os filtros de saída.

  *) Mod_http2: nova diretiva 'H2PushResource' para habilitar os empurrões iniciais antes Início do pedido principal
