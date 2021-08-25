---
title: Authentifizierungsdienstkonstanten (RpcDce.h)
description: Definiert Authentifizierungsdienste, indem das Sicherheitspaket identifiziert wird, das den Dienst bereitstellt, z. B. NTLMSSP, Kerberos oder Schannel.
ms.assetid: c16a8e52-a7f9-40d9-99ef-10b382b5cb3c
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_NONE
- RPC_C_AUTHN_DCE_PRIVATE
- RPC_C_AUTHN_DCE_PUBLIC
- RPC_C_AUTHN_DEC_PUBLIC
- RPC_C_AUTHN_GSS_NEGOTIATE
- RPC_C_AUTHN_WINNT
- RPC_C_AUTHN_GSS_SCHANNEL
- RPC_C_AUTHN_GSS_KERBEROS
- RPC_C_AUTHN_DPA
- RPC_C_AUTHN_MSN
- RPC_C_AUTHN_KERNEL
- RPC_C_AUTHN_DIGEST
- RPC_C_AUTHN_NEGO_EXTENDER
- RPC_C_AUTHN_PKU2U
- RPC_C_AUTHN_MQ
- RPC_C_AUTHN_DEFAULT
api_location:
- RpcDce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14cf6f0ab42b03d028d52df8160cad286e8c37af3988d8ca3b9736dad538012e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993780"
---
# <a name="authentication-service-constants"></a>Authentifizierungsdienstkonstanten

Definiert Authentifizierungsdienste, indem das Sicherheitspaket identifiziert wird, das den Dienst bereitstellt, z. B. NTLMSSP, Kerberos oder Schannel.



| Konstante/Wert                                                                                                                                                                                                                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_NONE"></span><span id="rpc_c_authn_none"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ NONE**</dt> <dt>0</dt> </dl>                              | Keine Authentifizierung<br/>                                                                                                                                                                                                                                                  |
| <span id="RPC_C_AUTHN_DCE_PRIVATE"></span><span id="rpc_c_authn_dce_private"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ DCE \_ PRIVATE**</dt> <dt>1</dt> </dl>        | Authentifizierung mit privatem DCE-Schlüssel.<br/>                                                                                                                                                                                                                                     |
| <span id="RPC_C_AUTHN_DCE_PUBLIC"></span><span id="rpc_c_authn_dce_public"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ DCE \_ PUBLIC**</dt> <dt>2</dt> </dl>           | Authentifizierung mit öffentlichem DCE-Schlüssel.<br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_DEC_PUBLIC"></span><span id="rpc_c_authn_dec_public"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ DEC \_ PUBLIC**</dt> <dt>4</dt> </dl>           | Authentifizierung mit öffentlichem DEC-Schlüssel. Für die zukünftige Verwendung reserviert.<br/>                                                                                                                                                                                                             |
| <span id="RPC_C_AUTHN_GSS_NEGOTIATE"></span><span id="rpc_c_authn_gss_negotiate"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ GSS \_ NEGOTIATE**</dt> <dt>9</dt> </dl>  | Snego-Sicherheitssupportanbieter.<br/>                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_WINNT"></span><span id="rpc_c_authn_winnt"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ WINNT**</dt> <dt>10</dt> </dl>                          | Ntlmssp<br/>                                                                                                                                                                                                                                                             |
| <span id="RPC_C_AUTHN_GSS_SCHANNEL"></span><span id="rpc_c_authn_gss_schannel"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ GSS \_ SCHANNEL**</dt> <dt>14</dt> </dl>    | Schannel-Sicherheitssupportanbieter. Dieser Authentifizierungsdienst unterstützt SSL 2.0, SSL 3.0, TLS und PCT.<br/>                                                                                                                                                            |
| <span id="RPC_C_AUTHN_GSS_KERBEROS"></span><span id="rpc_c_authn_gss_kerberos"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ GSS \_ KERBEROS**</dt> <dt>16</dt> </dl>    | Kerberos-Sicherheitsunterstützungsanbieter.<br/>                                                                                                                                                                                                                                 |
| <span id="RPC_C_AUTHN_DPA"></span><span id="rpc_c_authn_dpa"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ DPA**</dt> <dt>17</dt> </dl>                                | DPA-Sicherheitssupportanbieter.<br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_MSN"></span><span id="rpc_c_authn_msn"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ MSN**</dt> <dt>18</dt> </dl>                                | MSN-Sicherheitssupportanbieter.<br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_KERNEL"></span><span id="rpc_c_authn_kernel"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ KERNEL**</dt> <dt>20</dt> </dl>                       | Kernelsicherheits-Supportanbieter.<br/>                                                                                                                                                                                                                                   |
| <span id="RPC_C_AUTHN_DIGEST"></span><span id="rpc_c_authn_digest"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ DIGEST**</dt> <dt>21</dt> </dl>                       | Digestsicherheits-Supportanbieter.<br/>                                                                                                                                                                                                                                   |
| <span id="RPC_C_AUTHN_NEGO_EXTENDER"></span><span id="rpc_c_authn_nego_extender"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ NEGO \_ EXTENDER**</dt> <dt>30</dt> </dl> | NEGO-Extender-Sicherheitssupportanbieter.<br/>                                                                                                                                                                                                                            |
| <span id="RPC_C_AUTHN_PKU2U"></span><span id="rpc_c_authn_pku2u"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ PKU2U**</dt> <dt>31</dt> </dl>                          | PKU2U-Sicherheitssupportanbieter.<br/>                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_MQ"></span><span id="rpc_c_authn_mq"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ MQ**</dt> <dt>100</dt> </dl>                                  | MQ-Sicherheitsunterstützungsanbieter.<br/>                                                                                                                                                                                                                                       |
| <span id="RPC_C_AUTHN_DEFAULT"></span><span id="rpc_c_authn_default"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ DEFAULT**</dt> <dt>0xFFFFFFFFL</dt> </dl>           | Der Standardauthentifizierungsdienst des Systems. Wenn dieser Wert angegeben wird, verwendet COM den normalen Algorithmus für die Aushandlung von Sicherheitsaushandlungen, um einen Authentifizierungsdienst auszuwählen. Weitere Informationen finden Sie unter [Sicherheitsaushandlung.](security-blanket-negotiation.md) <br/> |



## <a name="remarks"></a>Hinweise

Diese Konstanten werden in den Strukturen [**SOLE \_ AUTHENTICATION \_ SERVICE**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) und [**SOLE AUTHENTICATION \_ \_ INFO**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) verwendet. Die **STRUKTUR SOLE AUTHENTICATION \_ \_ SERVICE** wird vom Server an die [**CoInitializeSecurity-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) übergeben und kann von der [**CoQueryAuthenticationServices-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) abgerufen werden. Ein Zeiger auf eine **SOLE \_ AUTHENTICATION \_ INFO-Struktur** wird vom Client an **CoInitializeSecurity** übergeben. Weitere Informationen zu den von diesen Werten identifizierten Sicherheitspaketen, z. B. NTLMSSP und Kerberos, finden Sie unter [COM- und Sicherheitspakete.](com-and-security-packages.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>RpcDce.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices)
</dt> <dt>

[**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity)
</dt> <dt>

[**EINZIGE \_ \_ AUTHENTIFIZIERUNGSINFORMATIONEN**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info)
</dt> <dt>

[**EINZIGER \_ \_ AUTHENTIFIZIERUNGSDIENST**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service)
</dt> </dl>

 

