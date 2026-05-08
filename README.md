# entendendo-sobre-seguran-a-identidade-azure
Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO

# Desafio: Entendendo sobre Segurança e Identidade na Azure

## Objetivo
Este projeto tem como objetivo aplicar os conceitos aprendidos sobre **segurança e gerenciamento de identidades no Microsoft Azure**, documentando o processo e os aprendizados.

## O que aprendi
Durante o desenvolvimento do laboratório, explorei os seguintes pontos:
- Diferença entre **Microsoft Entra ID** (antigo Azure AD) e outros serviços de segurança.  
- Como funciona a **autenticação multifator (MFA)**: algo que você sabe, possui e é.  
- Uso de **Acesso Condicional** para aplicar políticas de segurança baseadas em contexto (local, dispositivo, risco).  
- Conceito de **Confiança Zero (Zero Trust)** e sua aplicação prática.  
- Estratégia de **Defesa em Profundidade**, aplicando múltiplas camadas de proteção.  
- Funções do **Microsoft Defender para Nuvem** para monitoramento e proteção contra ameaças.  
- Diferença entre **Azure Monitor** e **Microsoft Purview** dentro da estratégia de segurança.  
- Importância de alinhar **segurança, identidade e governança** para proteger dados e aplicações.  

## Passo a Passo Documentado
1. Configurar **Microsoft Entra ID** para gerenciamento de usuários e grupos.  
2. Habilitar **MFA** para contas críticas.  
3. Criar políticas de **Acesso Condicional** para restringir logins suspeitos.  
4. Explorar relatórios de segurança no **Defender para Nuvem**.  
5. Aplicar práticas de **Zero Trust** em cenários simulados.  
6. Revisar logs e alertas no **Azure Monitor**.  
7. Documentar boas práticas de governança com **Purview**.  

## Fluxo de Login Seguro no Azure

Usuário → [Microsoft Entra ID] → Verificação de credenciais  
   │  
   ├──> **Senha (Algo que você sabe)**  
   │  
   ├──> **MFA (Algo que você possui/é)**  
   │       • Código via aplicativo de autenticação  
   │       • SMS ou token físico  
   │       • Biometria (impressão digital/face)  
   │  
   └──> **Acesso Condicional**  
           • Verifica localização (ex.: bloqueio fora do país)  
           • Verifica dispositivo (gerenciado ou não)  
           • Avalia risco da sessão (baixo, médio, alto)  
           • Decide: permitir, bloquear ou exigir MFA adicional  

Resultado → **Acesso concedido ou negado**  
 

## Comparativo: Segurança e Identidade na Azure

| Conceito/Serviço              | O que é | Função Principal | Exemplos de Uso |
|--------------------------------|---------|-----------------|-----------------|
| **Microsoft Entra ID**         | Serviço de gerenciamento de identidades e acesso baseado em nuvem (antigo Azure AD). | Centraliza autenticação e autorização de usuários e apps. | Login único (SSO), integração com SaaS, gerenciamento de grupos e permissões. |
| **MFA (Multi-Factor Authentication)** | Mecanismo de autenticação que exige mais de um fator de verificação. | Aumenta a segurança exigindo senha + dispositivo + biometria. | Login com senha + aplicativo de autenticação, ou senha + SMS. |
| **Acesso Condicional**         | Política de segurança baseada em contexto. | Permite ou bloqueia acesso dependendo de condições (local, dispositivo, risco). | Bloquear login de fora do país, exigir MFA em dispositivos não gerenciados. |
| **Zero Trust (Confiança Zero)** | Modelo de segurança que assume que nenhuma conexão é confiável por padrão. | Protege sistemas aplicando verificação contínua em cada acesso. | Exigir autenticação e autorização em cada requisição, mesmo dentro da rede corporativa. |


## Conclusão
Esse desafio reforçou minha compreensão sobre como **segurança e identidade são pilares fundamentais no Azure**, garantindo proteção contra ameaças e acesso controlado aos recursos.

---

**Autor:** Ana Quézia de Oliveira Souza
