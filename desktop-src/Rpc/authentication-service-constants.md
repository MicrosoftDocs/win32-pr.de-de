---
title: Authentication-Service Konstanten (rpcdce. h)
description: Die Authentifizierungsdienst Konstanten stellen die Authentifizierungsdienste dar, die an verschiedene Lauf Zeitfunktionen übermittelt werden.
ms.assetid: ac95276f-230d-4993-92fe-1739d022c8b3
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
- RPC_C_AUTHN_DIGEST
- RPC_C_AUTHN_NEGO_EXTENDER
- RPC_C_AUTHN_MQ
- RPC_C_AUTHN_DEFAULT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4ace510c1c26030542090eb1b00e76db803df6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518725"
---
# <a name="authentication-service-constants"></a>Authentication-Service Konstanten

Die Authentifizierungsdienst Konstanten stellen die Authentifizierungsdienste dar, die an verschiedene Lauf Zeitfunktionen übermittelt werden.

Die folgenden Konstanten sind gültige Werte für den *authnsvc* -Parameter.



| Konstante/Wert                                                                                                                                                                                                                                               | BESCHREIBUNG                                                                                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_NONE"></span><span id="rpc_c_authn_none"></span><dl> <dt>**RPC \_ C \_ authn \_ None**</dt> <dt>0</dt> </dl>                              | Keine Authentifizierung<br/>                                                                                                                                                        |
| <span id="RPC_C_AUTHN_DCE_PRIVATE"></span><span id="rpc_c_authn_dce_private"></span><dl> <dt>**RPC \_ C \_ authn \_ DCE \_ private**</dt> <dt>1</dt> </dl>        | Verwenden Sie die Authentifizierung für den privaten Schlüssel der verteilten Computerumgebung (DCE).<br/>                                                                                                   |
| <span id="RPC_C_AUTHN_DCE_PUBLIC"></span><span id="rpc_c_authn_dce_public"></span><dl> <dt>**RPC \_ C \_ authn \_ DCE \_ Public**</dt> <dt>2</dt> </dl>           | Authentifizierung mit öffentlichem Schlüssel für DCE (für zukünftige Verwendung reserviert).<br/>                                                                                                                  |
| <span id="RPC_C_AUTHN_DEC_PUBLIC"></span><span id="rpc_c_authn_dec_public"></span><dl> <dt>**RPC \_ C \_ authn \_ , \_ Public**</dt> <dt>4</dt> </dl>           | Authentifizierung mit öffentlichem Schlüssel (für zukünftige Verwendung reserviert)<br/>                                                                                                                  |
| <span id="RPC_C_AUTHN_GSS_NEGOTIATE"></span><span id="rpc_c_authn_gss_negotiate"></span><dl> <dt>**RPC \_ C \_ authn- \_ GSS- \_ Aushandlung**</dt> <dt>9</dt> </dl>  | Verwenden Sie den [Microsoft Aushandlungs-SSP](/windows/desktop/SecAuthN/microsoft-negotiate). Dieser SSP verhandelt zwischen der Verwendung der NTLM-und Kerberos-Protokoll Sicherheits Unterstützungs Anbieter (SSP).<br/>  |
| <span id="RPC_C_AUTHN_WINNT"></span><span id="rpc_c_authn_winnt"></span><dl> <dt>**RPC \_ C \_ authn \_ Winnt**</dt> <dt>10</dt> </dl>                          | Verwenden Sie den [SSP von Microsoft NT LAN Manager (NTLM)](/windows/desktop/SecAuthN/microsoft-ntlm).<br/>                                                                                                   |
| <span id="RPC_C_AUTHN_GSS_SCHANNEL"></span><span id="rpc_c_authn_gss_schannel"></span><dl> <dt>**RPC \_ C \_ authn \_ GSS \_ SChannel**</dt> <dt>14</dt> </dl>    | Verwenden Sie den [Schannel SSP](/windows/desktop/SecAuthN/secure-channel). Dieser SSP unterstützt SSL (Secure Socket Layer), private Kommunikationstechnologie (PCT) und TLS (Transport Level Security).<br/> |
| <span id="RPC_C_AUTHN_GSS_KERBEROS"></span><span id="rpc_c_authn_gss_kerberos"></span><dl> <dt>**RPC \_ C \_ authn \_ GSS \_ Kerberos**</dt> <dt>16</dt> </dl>    | Verwenden Sie den [Kerberos-SSP von Microsoft](/windows/desktop/SecAuthN/microsoft-kerberos).<br/>                                                                                                            |
| <span id="RPC_C_AUTHN_DPA"></span><span id="rpc_c_authn_dpa"></span><dl> <dt>**RPC \_ C \_ authn \_ DPA**</dt> <dt>17</dt> </dl>                                | Verwenden Sie die Authentifizierung verteilter Kenn Wörter (dpa).<br/>                                                                                                                            |
| <span id="RPC_C_AUTHN_MSN"></span><span id="rpc_c_authn_msn"></span><dl> <dt>**RPC \_ C \_ authn \_ MSN**</dt> <dt>18</dt> </dl>                                | Der Authentifizierungsprotokoll-SSP, der für das Microsoft-Netzwerk (MSN) verwendet wird.<br/>                                                                                                         |
| <span id="RPC_C_AUTHN_DIGEST"></span><span id="rpc_c_authn_digest"></span><dl> <dt>**RPC \_ C- \_ authn \_ Digest**</dt> <dt>21</dt> </dl>                       | Windows XP oder höher: Verwenden des [Microsoft Digest SSP](/windows/desktop/SecAuthN/microsoft-digest-ssp)<br/>                                                                                        |
| <span id="RPC_C_AUTHN_NEGO_EXTENDER"></span><span id="rpc_c_authn_nego_extender"></span><dl> <dt>**RPC \_ C \_ authn- \_ \_ Extender-Extender**</dt> <dt>30</dt> </dl> | Windows 7 oder höher: reserviert. Nicht verwenden<br/>                                                                                                                                  |
| <span id="RPC_C_AUTHN_MQ"></span><span id="rpc_c_authn_mq"></span><dl> <dt>**RPC \_ C \_ authn \_ MQ**</dt> <dt>100</dt> </dl>                                  | Dieser SSP bietet einen SSPI-kompatiblen Wrapper für das Protokoll der Microsoft Message Queue (MSMQ)-Transport Ebene.<br/>                                                             |
| <span id="RPC_C_AUTHN_DEFAULT"></span><span id="rpc_c_authn_default"></span><dl> <dt>**RPC \_ C \_ authn \_ Standard**</dt> <dt>0xFFFFFFFF</dt> </dl>            | Verwenden Sie den Standard Authentifizierungsdienst.<br/>                                                                                                                                   |



## <a name="remarks"></a>Bemerkungen

Geben \_ Sie RPC C \_ authn \_ None an, um die Authentifizierung für Remote Prozedur Aufrufe, die über ein Bindungs handle erfolgen, zu deaktivieren. Wenn Sie RPC \_ c \_ authn \_ default angeben, wird von der RPC-Lauf Zeit Bibliothek der RPC- \_ c- \_ authn- \_ Winnt-Authentifizierungsdienst für Remote Prozedur Aufrufe verwendet, die mithilfe des Bindungs Handles ausgeführt wurden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Rpcdce. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Rpcbindinginqauthinfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[**Rpcbindingsetauthinfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> <dt>

[**Rpcbindinginqauthclient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[**Rpcbindinginqauthcliumtex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[**Rpcbindingsetauthinfoex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[**Rpcbindinginqauthinfoex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> </dl>

 

