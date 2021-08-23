---
title: Autorisierungskonstanten (RpcDce.h)
description: Definiert, was der Server autorisiert.
ms.assetid: a0bc9337-b7e4-41c5-ae36-4843fa7d98ce
topic_type:
- apiref
api_name:
- RPC_C_AUTHZ_NONE
- RPC_C_AUTHZ_NAME
- RPC_C_AUTHZ_DCE
- RPC_C_AUTHZ_DEFAULT
api_location:
- RpcDce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb89786a0c27c66177bc29861fdcf53a9341f73e498b5627e1cb826e83f61cc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048668"
---
# <a name="authorization-constants"></a>Autorisierungskonstanten

Definiert, was der Server autorisiert.



| Konstante/Wert                                                                                                                                                                                                                                    | Beschreibung                                                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ NONE**</dt> <dt>0</dt> </dl>                   | Der Server führt keine Autorisierung aus. Derzeit verwenden RPC \_ C \_ \_ AUTHN WINNT, RPC \_ C \_ AUTHN \_ GSS \_ SCHANNEL und RPC C \_ \_ AUTHN \_ GSS \_ KERBEROS nur RPC C \_ \_ RPHZ \_ NONE.<br/>                                                                                                                |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <dt>**RPC \_ C \_ \_ AUTHZ-NAME**</dt> <dt>1</dt> </dl>                   | Der Server führt die Autorisierung basierend auf dem Prinzipalnamen des Clients aus. <br/>                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ DCE**</dt> <dt>2</dt> </dl>                      | Der Server führt eine Autorisierungsprüfung mithilfe der INFORMATIONEN zum DCE-Berechtigungsattributzertifikat (PAC) des Clients durch, die mit jedem Remoteprozeduraufruf, der mit dem Bindungshandle erfolgt, an den Server gesendet werden. Im Allgemeinen wird der Zugriff anhand von DCE-Zugriffssteuerungslisten (ACLs) überprüft. <br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <dt>**RPC \_ STANDARDMÄßIGE \_ \_ C-0XFFFFFFFF**</dt> <dt></dt> </dl> | DCOM kann die Autorisierungsstufe mithilfe des normalen Algorithmus für die Aushandlung von Sicherheitsaushandlungen auswählen. Weitere Informationen finden Sie unter [Sicherheitsaushandlung.](security-blanket-negotiation.md)<br/>                                                                                           |



## <a name="remarks"></a>Hinweise

Diese Konstanten werden von Methoden der [**IClientSecurity-Schnittstelle**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) verwendet. Sie werden in der [**SOLE \_ AUTHENTICATION \_ SERVICE-Struktur**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) verwendet, die von der [**CoQueryAuthenticationServices-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) abgerufen wird. Sie werden auch in der [**SOLE \_ AUTHENTICATION \_ INFO-Struktur**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) verwendet, die wiederum Ein Member der [**STRUKTUR SOLE AUTHENTICATION \_ \_ LIST**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list) ist. Diese Struktur, bei der es sich um eine Liste der Authentifizierungsdienste, der von ihnen ausgeführten Autorisierungsdienste und der Authentifizierungsinformationen für jeden Dienst handelt, wird an die [**CoInitializeSecurity-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) und die [**IClientSecurity::SetBlanket-Methode**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) übergeben.

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

 

