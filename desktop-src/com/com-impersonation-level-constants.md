---
title: Konstanten der Identitätswechsel Ebene (rpcdce. h)
description: Gibt eine Identitätswechsel Ebene an, die die Menge an Berechtigungen angibt, die dem Server bei der Identitätswechsel des Clients erteilt werden.
ms.assetid: ea5a3b46-b607-4192-a3cc-b2ec55ca94a6
topic_type:
- apiref
api_name:
- RPC_C_IMP_LEVEL_DEFAULT
- RPC_C_IMP_LEVEL_ANONYMOUS
- RPC_C_IMP_LEVEL_IDENTIFY
- RPC_C_IMP_LEVEL_IMPERSONATE
- RPC_C_IMP_LEVEL_DELEGATE
api_location:
- RpcDce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9f16ed07235e52d9aefd7bffff9ce430c3978d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340758"
---
# <a name="impersonation-level-constants"></a>Konstanten der Identitätswechsel Ebene

Gibt eine Identitätswechsel Ebene an, die die Menge an Berechtigungen angibt, die dem Server bei der Identitätswechsel des Clients erteilt werden.



| Konstante/Wert                                                                                                                                                                                                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_IMP_LEVEL_DEFAULT"></span><span id="rpc_c_imp_level_default"></span><dl> <dt>**RPC \_ C \_ IMP- \_ Ebene, \_ Standardwert**</dt> <dt>0</dt> </dl>             | Die Identitätswechsel Ebene kann von DCOM mithilfe des normalen Algorithmus für die Sicherheits-und-Aushandlung ausgewählt werden. Weitere Informationen finden Sie unter [sicherheitspauschere Aushandlung](security-blanket-negotiation.md).<br/>                                                                                                                                                                                                                                                                           |
| <span id="RPC_C_IMP_LEVEL_ANONYMOUS"></span><span id="rpc_c_imp_level_anonymous"></span><dl> <dt>**RPC \_ C \_ IMP- \_ Ebene \_ Anonym**</dt> <dt>1</dt> </dl>       | Der Client ist gegenüber dem Server anonym. Der Server Prozess kann die Identität des Clients annehmen, das Identitätswechsel Token enthält jedoch keine Informationen und kann nicht verwendet werden.<br/>                                                                                                                                                                                                                                                                                                 |
| <span id="RPC_C_IMP_LEVEL_IDENTIFY"></span><span id="rpc_c_imp_level_identify"></span><dl> <dt>**RPC \_ C \_ IMP- \_ Ebene \_ Identifizierung**</dt> <dt>2</dt> </dl>          | Der Server kann die Identität des Clients abrufen. Der Server kann die Identität des Clients für die ACL-Überprüfung annehmen, aber nicht als Client auf Systemobjekte zugreifen. <br/>                                                                                                                                                                                                                                                                                                               |
| <span id="RPC_C_IMP_LEVEL_IMPERSONATE"></span><span id="rpc_c_imp_level_impersonate"></span><dl> <dt>**RPC \_ C \_ IMP \_ - \_ Ebene**</dt> Identitätswechsel <dt>3</dt> </dl> | Der Server Prozess kann einen Identitätswechsel für den Sicherheitskontext des Clients ausführen, während er im Auftrag des Clients agiert. Diese Identitätsebene ermöglicht den Zugriff auf lokale Ressourcen wie Dateien. Beim Identitätswechsel auf dieser Ebene kann das Identitätswechsel Token nur über eine Computer Grenze hinweg weitergegeben werden. Der [SChannel](schannel.md) -Authentifizierungsdienst unterstützt nur diese Ebene des Identitäts Wechsels. <br/>                                                                      |
| <span id="RPC_C_IMP_LEVEL_DELEGATE"></span><span id="rpc_c_imp_level_delegate"></span><dl> <dt>**RPC \_ C \_ IMP \_ - \_ Ebene**</dt> , Delegat <dt>4</dt> </dl>          | Der Server Prozess kann einen Identitätswechsel für den Sicherheitskontext des Clients ausführen, während er im Auftrag des Clients agiert. Der Server Prozess kann auch ausgehende Aufrufe an andere Server durchführen, während er im Auftrag des Clients verwendet wird. Der Server kann den Sicherheitskontext des Clients auf anderen Computern verwenden, um auf lokale und Remote Ressourcen als Client zuzugreifen. Beim Identitätswechsel auf dieser Ebene kann das Identitätswechsel Token über eine beliebige Anzahl von Computer Grenzen hinweg weitergegeben werden.<br/> |



## <a name="remarks"></a>Bemerkungen

[**GetUsername**](/windows/desktop/api/winbase/nf-winbase-getusernamea) schlägt fehl, während der Identitätswechsel auf der identifizebene erfolgt. Die Problem Umgehung besteht darin, einen Identitätswechsel durchzusetzen, [**openthumlocktoken**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken)aufzurufen, rückgängig zu machen, [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation)aufzurufen und schließlich [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida)aufzurufen. Mithilfe von [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)legt der Client die Identitätswechsel Ebene fest.

Mithilfe von [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)legt der Client die Identitätswechsel Ebene und die Proxy Identität fest, die verfügbar sind, wenn ein Server " [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)" aufruft. Die Identität, die der Server beim Identitätswechsel feststellt, wird unter " [Cloaking](cloaking.md)" beschrieben. Beachten Sie, dass der aufgerufene beim Durchführen eines Aufrufens beim Identitätswechsel normalerweise das Prozess Token des Aufrufers empfängt, nicht das Identitätswechsel Token des Aufrufers. Um das Identitätswechsel Token des Aufrufers zu empfangen, muss der Aufrufer das Cloaking aktivieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Rpcdce. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Cloaking](cloaking.md)
</dt> </dl>

 

