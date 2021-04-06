---
title: Autorisierungs Konstanten (rpcdce. h)
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
ms.openlocfilehash: ed2c46ad729e02fd63eb9b8088d31f05515c2ef8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743712"
---
# <a name="authorization-constants"></a>Autorisierungs Konstanten

Definiert, was der Server autorisiert.



| Konstante/Wert                                                                                                                                                                                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <dt>**RPC \_ C \_ Authz \_ None**</dt> <dt>0</dt> </dl>                   | Der Server führt keine Autorisierung aus. Derzeit verwenden RPC \_ c \_ authn \_ Winnt, RPC \_ c \_ authn \_ GSS \_ SChannel und RPC \_ c \_ authn \_ GSS \_ Kerberos nur RPC \_ c \_ Authz \_ None.<br/>                                                                                                                |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <dt>**RPC \_ C- \_ Authz- \_ Name**</dt> <dt>1</dt> </dl>                   | Der Server führt die Autorisierung basierend auf dem Prinzipal Namen des Clients aus. <br/>                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <dt>**RPC \_ C \_ Authz \_ DCE**</dt> <dt>2</dt> </dl>                      | Der Server führt die Autorisierungs Überprüfung mithilfe der Informationen des DCE Privilege Attribute Certificate (PAC) des Clients durch, die an den Server gesendet wird, wobei jeder Remote Prozedur Rückruf mit dem Bindungs handle erfolgt. Im Allgemeinen wird der Zugriff auf DCE-Zugriffs Steuerungs Listen (ACLs) überprüft. <br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <dt>**RPC \_ C \_ Authz \_ Standard**</dt> <dt>0xFFFFFFFF</dt> </dl> | Die Autorisierungs Ebene kann von DCOM mithilfe des normalen Algorithmus für die Sicherheits-und-Aushandlung ausgewählt werden. Weitere Informationen finden Sie unter [sicherheitspauschere Aushandlung](security-blanket-negotiation.md).<br/>                                                                                           |



## <a name="remarks"></a>Bemerkungen

Diese Konstanten werden von Methoden der [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) -Schnittstelle verwendet. Sie werden in der [**einzigen \_ Authentifizierungs \_ Dienst**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) Struktur verwendet, die von der [**coqueryauthenticationservices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) -Funktion abgerufen wird. Sie werden auch in der [**einzigen \_ Authentifizierungs \_ Informations**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) Struktur verwendet, die wiederum Mitglied der [**einzigen \_ Authentifizierungs \_ Listen**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list) Struktur ist. Diese Struktur, bei der es sich um eine Liste der Authentifizierungsdienste, die von Ihnen ausgeführten Autorisierungs Dienste und die Authentifizierungsinformationen für jeden Dienst handelt, wird an die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) -Funktion und die [**IClientSecurity:: setblanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) -Methode übermittelt.

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

 

