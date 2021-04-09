---
title: Authentifizierungsdienst Konstanten (rpcdce. h)
description: Definiert Authentifizierungsdienste durch Identifizierung des Sicherheitspakets, das den Dienst bereitstellt, z. b. NTLMSSP, Kerberos oder Schannel.
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
ms.openlocfilehash: 1227d2accdf871c2e57a25661837d10089c983ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106317"
---
# <a name="authentication-service-constants"></a>Authentifizierungsdienst Konstanten

Definiert Authentifizierungsdienste durch Identifizierung des Sicherheitspakets, das den Dienst bereitstellt, z. b. NTLMSSP, Kerberos oder Schannel.



| Konstante/Wert                                                                                                                                                                                                                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_NONE"></span><span id="rpc_c_authn_none"></span><dl> <dt>**RPC \_ C \_ authn \_ None**</dt> <dt>0</dt> </dl>                              | Keine Authentifizierung<br/>                                                                                                                                                                                                                                                  |
| <span id="RPC_C_AUTHN_DCE_PRIVATE"></span><span id="rpc_c_authn_dce_private"></span><dl> <dt>**RPC \_ C \_ authn \_ DCE \_ private**</dt> <dt>1</dt> </dl>        | Authentifizierung mit privatem DCE-Schlüssel.<br/>                                                                                                                                                                                                                                     |
| <span id="RPC_C_AUTHN_DCE_PUBLIC"></span><span id="rpc_c_authn_dce_public"></span><dl> <dt>**RPC \_ C \_ authn \_ DCE \_ Public**</dt> <dt>2</dt> </dl>           | Authentifizierung mit öffentlichem DCE-Schlüssel.<br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_DEC_PUBLIC"></span><span id="rpc_c_authn_dec_public"></span><dl> <dt>**RPC \_ C \_ authn \_ , \_ Public**</dt> <dt>4</dt> </dl>           | Authentifizierung mit öffentlichem Schlüssel für Dezember Für die zukünftige Verwendung reserviert.<br/>                                                                                                                                                                                                             |
| <span id="RPC_C_AUTHN_GSS_NEGOTIATE"></span><span id="rpc_c_authn_gss_negotiate"></span><dl> <dt>**RPC \_ C \_ authn- \_ GSS- \_ Aushandlung**</dt> <dt>9</dt> </dl>  | Schgo-Security Support Provider.<br/>                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_WINNT"></span><span id="rpc_c_authn_winnt"></span><dl> <dt>**RPC \_ C \_ authn \_ Winnt**</dt> <dt>10</dt> </dl>                          | NTLMSSP<br/>                                                                                                                                                                                                                                                             |
| <span id="RPC_C_AUTHN_GSS_SCHANNEL"></span><span id="rpc_c_authn_gss_schannel"></span><dl> <dt>**RPC \_ C \_ authn \_ GSS \_ SChannel**</dt> <dt>14</dt> </dl>    | SChannel-Security Support Provider. Dieser Authentifizierungsdienst unterstützt SSL 2,0, SSL 3,0, TLS und PCT.<br/>                                                                                                                                                            |
| <span id="RPC_C_AUTHN_GSS_KERBEROS"></span><span id="rpc_c_authn_gss_kerberos"></span><dl> <dt>**RPC \_ C \_ authn \_ GSS \_ Kerberos**</dt> <dt>16</dt> </dl>    | Kerberos-Security Support Provider.<br/>                                                                                                                                                                                                                                 |
| <span id="RPC_C_AUTHN_DPA"></span><span id="rpc_c_authn_dpa"></span><dl> <dt>**RPC \_ C \_ authn \_ DPA**</dt> <dt>17</dt> </dl>                                | DPA Security Support Provider.<br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_MSN"></span><span id="rpc_c_authn_msn"></span><dl> <dt>**RPC \_ C \_ authn \_ MSN**</dt> <dt>18</dt> </dl>                                | MSN Security Support Provider.<br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_KERNEL"></span><span id="rpc_c_authn_kernel"></span><dl> <dt>**RPC \_ C \_ -authn \_ -Kernel**</dt> <dt>20</dt> </dl>                       | Kernel-Security Support Provider.<br/>                                                                                                                                                                                                                                   |
| <span id="RPC_C_AUTHN_DIGEST"></span><span id="rpc_c_authn_digest"></span><dl> <dt>**RPC \_ C- \_ authn \_ Digest**</dt> <dt>21</dt> </dl>                       | Digest-Security Support Provider.<br/>                                                                                                                                                                                                                                   |
| <span id="RPC_C_AUTHN_NEGO_EXTENDER"></span><span id="rpc_c_authn_nego_extender"></span><dl> <dt>**RPC \_ C \_ authn- \_ \_ Extender-Extender**</dt> <dt>30</dt> </dl> | Der NGO-Extender-Security Support Provider.<br/>                                                                                                                                                                                                                            |
| <span id="RPC_C_AUTHN_PKU2U"></span><span id="rpc_c_authn_pku2u"></span><dl> <dt>**RPC \_ C- \_ authn \_ PKU2U**</dt> <dt>31</dt> </dl>                          | PKU2U-Security Support Provider.<br/>                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_MQ"></span><span id="rpc_c_authn_mq"></span><dl> <dt>**RPC \_ C \_ authn \_ MQ**</dt> <dt>100</dt> </dl>                                  | MQ-Security Support Provider.<br/>                                                                                                                                                                                                                                       |
| <span id="RPC_C_AUTHN_DEFAULT"></span><span id="rpc_c_authn_default"></span><dl> <dt>**RPC \_ C \_ authn \_ Standard**</dt> <dt>0xffffffffl</dt> </dl>           | Der Standard Authentifizierungsdienst des Systems. Wenn dieser Wert angegeben ist, verwendet com den normalen sicherheitspausierungsalgorithmus, um einen Authentifizierungsdienst auszuwählen. Weitere Informationen finden Sie unter [sicherheitspauschere Aushandlung](security-blanket-negotiation.md). <br/> |



## <a name="remarks"></a>Bemerkungen

Diese Konstanten werden im [**einzigen \_ Authentifizierungs \_ Dienst**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) und in den [**einzigen \_ Authentifizierungs \_ Informations**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) Strukturen verwendet. Die **einzige \_ Authentifizierungs \_ Dienst** Struktur wird vom Server an die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) -Funktion übergeben und kann von der [**coqueryauthenticationservices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) -Funktion abgerufen werden. Ein Zeiger auf eine **einzige \_ Authentifizierungs \_ Informations** Struktur wird vom Client an **CoInitializeSecurity** übermittelt. Weitere Informationen zu den von diesen Werten identifizierten Sicherheitspaketen, wie z. b. NTLMSSP und Kerberos, finden Sie unter [com-und Sicherheitspakete](com-and-security-packages.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Rpcdce. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**Coqueryauthenticationservices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices)
</dt> <dt>

[**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity)
</dt> <dt>

[**Informationen zur alleinigen \_ Authentifizierung \_**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info)
</dt> <dt>

[**einziger \_ Authentifizierungs \_ Dienst**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service)
</dt> </dl>

 

