---
title: Authorization-Service Konstanten (rpcdce. h)
description: Die Autorisierungs Dienst Konstanten stellen die Autorisierungs Dienste dar, die an verschiedene Lauf Zeitfunktionen übermittelt werden.
ms.assetid: b773bb51-7af0-4eb3-9438-fe3ef9a350db
topic_type:
- apiref
api_name:
- RPC_C_AUTHZ_NONE
- RPC_C_AUTHZ_NAME
- RPC_C_AUTHZ_DCE
- RPC_C_AUTHZ_DEFAULT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0394163e97a822126e71eeda3cf8382f1dcc20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519263"
---
# <a name="authorization-service-constants"></a>Authorization-Service Konstanten

Die Autorisierungs Dienst Konstanten stellen die Autorisierungs Dienste dar, die an verschiedene Lauf Zeitfunktionen übermittelt werden.

Die folgenden Konstanten sind gültige Werte für den *authzsvc* -Parameter. Die meisten Anwendungen finden RPC \_ C \_ Authz \_ nicht ausreichend.



| Konstante/Wert                                                                                                                                                                                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <dt>**RPC \_ C \_ Authz \_ None**</dt> <dt>0</dt> </dl>                   | Der Server führt keine Autorisierung aus.<br/>                                                                                                                                                                                                                                                                 |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <dt>**RPC \_ C- \_ Authz- \_ Name**</dt> <dt>1</dt> </dl>                   | Der Server führt die Autorisierung basierend auf dem Prinzipal Namen des Clients aus.<br/>                                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <dt>**RPC \_ C \_ Authz \_ DCE**</dt> <dt>2</dt> </dl>                      | Der Server führt die Autorisierungs Überprüfung mithilfe der Informationen des DCE Privilege Attribute Certificate (PAC) des Clients durch, die an den Server gesendet wird, wobei jeder Remote Prozedur Rückruf mit dem Bindungs handle erfolgt. Im Allgemeinen wird der Zugriff auf DCE-Zugriffs Steuerungs Listen ([ACLs](/windows/desktop/api/winnt/ns-winnt-acl)) überprüft.<br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <dt>**RPC \_ C \_ Authz \_ Standard**</dt> <dt>0xFFFFFFFF</dt> </dl> | Der Server verwendet den Standard Autorisierungs Dienst für den aktuellen SSP.<br/>                                                                                                                                                                                                                                |



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
</dt> <dt>

[**RpcMgmtInqDefaultProtectLevel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqdefaultprotectlevel)
</dt> </dl>

 

