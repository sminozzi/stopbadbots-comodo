# Comodo ModSecurity Rules (CWAF) - Versão Customizada e Atualizada

Este repositório contém a base de regras original do Comodo Web Application Firewall (CWAF), mantida de forma independente e enriquecida com as atualizações frequentes baseadas no projeto [SBB-WAF-Rules](https://github.com/sminozzi/SBB-WAF-Rules). 

O pacote conta com otimizações globais para redução de falsos positivos e suporte a regras personalizadas, ideal para quem deseja manter o ecossistema Comodo ativo e protegido contra novas ameaças.

## 📁 Estrutura do Repositório

* `cwaf.conf`: Arquivo mestre que gerencia a ordem de carregamento do ecossistema.
* `rules/`: Pasta contendo as regras oficiais (.conf) e arquivos de dados (.data) alimentados por patches atualizados.
* `global/zzz_exclude_global.conf`: Arquivo de mitigação com regras desativadas globalmente para evitar quebras em aplicações comuns.
* `custom_user.conf`: Arquivo destinado para as suas regras personalizadas.
* `domains/`: Pasta para configurações e exceções específicas por domínio.

---

## 🚀 Como Instalar

### Pré-requisitos
* ModSecurity instalado e ativo no servidor (Apache, Nginx ou LiteSpeed).
* Acesso root ou privilégios de administrador para editar as configurações do servidor web.

### Passo 1: Baixar as regras
Clone este repositório diretamente no diretório de segurança do seu servidor (o padrão sugerido na configuração é `/usr/local/apache/modsecurity-cwaf/`):

```bash
git clone [https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git](https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git) /usr/local/apache/modsecurity-cwaf/
