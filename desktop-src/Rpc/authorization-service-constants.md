---
title: Authorization-Service Konstanten (Rpcdce.h)
description: Die Autorisierungsdienstkonstanten stellen die Autorisierungsdienste dar, die an verschiedene Laufzeitfunktionen übergeben werden.
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
ms.openlocfilehash: 027b32acb8b38ac1359cee96f68542da94f48d3bdf7d454d631bf0a8eff1092e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023430"
---
# <a name="authorization-service-constants"></a>Authorization-Service Konstanten

Die Autorisierungsdienstkonstanten stellen die Autorisierungsdienste dar, die an verschiedene Laufzeitfunktionen übergeben werden.

Die folgenden Konstanten sind gültige Werte für den *Parameter AuthzSvc.* Bei den meisten Anwendungen ist RPC \_ C \_ AUTHZ \_ nicht ausreichend.



| Konstante/Wert                                                                                                                                                                                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ NONE**</dt> <dt>0</dt> </dl>                   | Der Server führt keine Autorisierung aus.<br/>                                                                                                                                                                                                                                                                 |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <dt>**RPC \_ C \_ \_ AUTHZ-NAME**</dt> <dt>1</dt> </dl>                   | Der Server führt die Autorisierung basierend auf dem Prinzipalnamen des Clients aus.<br/>                                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ DCE**</dt> <dt>2</dt> </dl>                      | Der Server führt die Autorisierungsüberprüfung mithilfe der PAC-Informationen (DCE Privilege Attribute Certificate) des Clients aus, die mit jedem Remoteprozeduraufruf, der mit dem Bindungshandle erfolgt, an den Server gesendet werden. Im Allgemeinen wird der Zugriff anhand von DCE-Zugriffssteuerungslisten[(ACLs)](/windows/desktop/api/winnt/ns-winnt-acl)überprüft.<br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <dt>**RPC \_ \_ \_ STANDARD-0XFFFFFFFF FÜR C 0XFFFFFFFF**</dt> <dt></dt> </dl> | Der Server verwendet den Standardautorisierungsdienst für den aktuellen SSP.<br/>                                                                                                                                                                                                                                |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Rpcdce.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**RpcBindingInqAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> <dt>

[**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[**RpcBindingInqAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> <dt>

[**RpcMgmtInqDefaultProtectLevel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqdefaultprotectlevel)
</dt> </dl>

 

