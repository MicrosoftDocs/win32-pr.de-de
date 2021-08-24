---
title: Impersonation Level Constants (RpcDce.h)
description: Gibt eine Identitätswechselebene an, die angibt, wie viel Autorität dem Server beim Identitätswechsel des Clients erteilt wird.
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
ms.openlocfilehash: 7dbc4b4a74871eb111b778d798587e53027053fe57cc8cda837a3aafb7c24d74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048488"
---
# <a name="impersonation-level-constants"></a>Identitätswechselebenenkonstationen

Gibt eine Identitätswechselebene an, die angibt, wie viel Autorität dem Server beim Identitätswechsel des Clients erteilt wird.



| Konstante/Wert                                                                                                                                                                                                                                                    | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_IMP_LEVEL_DEFAULT"></span><span id="rpc_c_imp_level_default"></span><dl> <dt>**RPC \_ C \_ IMP \_ LEVEL \_ DEFAULT**</dt> <dt>0</dt> </dl>             | DCOM kann die Identitätswechselebene mithilfe des normalen Aushandlungsalgorithmus für Sicherheitsaushandlung auswählen. Weitere Informationen finden Sie unter [Security Negotiation .](security-blanket-negotiation.md)<br/>                                                                                                                                                                                                                                                                           |
| <span id="RPC_C_IMP_LEVEL_ANONYMOUS"></span><span id="rpc_c_imp_level_anonymous"></span><dl> <dt>**RPC \_ C \_ IMP \_ LEVEL \_ ANONYMOUS**</dt> <dt>1</dt> </dl>       | Der Client ist gegenüber dem Server anonym. Der Serverprozess kann die Identität des Clients imitieren, aber das Identitätswechseltoken enthält keine Informationen und kann nicht verwendet werden.<br/>                                                                                                                                                                                                                                                                                                 |
| <span id="RPC_C_IMP_LEVEL_IDENTIFY"></span><span id="rpc_c_imp_level_identify"></span><dl> <dt>**RPC \_ C \_ IMP \_ LEVEL \_ IDENTIFY**</dt> <dt>2</dt> </dl>          | Der Server kann die Identität des Clients abrufen. Der Server kann die Identität des Clients für die ACL-Überprüfung imitieren, aber er kann nicht als Client auf Systemobjekte zugreifen. <br/>                                                                                                                                                                                                                                                                                                               |
| <span id="RPC_C_IMP_LEVEL_IMPERSONATE"></span><span id="rpc_c_imp_level_impersonate"></span><dl> <dt>**RPC \_ C \_ IMP \_ LEVEL \_ IMPERSONATE**</dt> <dt>3</dt> </dl> | Der Serverprozess kann die Identität des Sicherheitskontexts des Clients im Auftrag des Clients im Auftrag des Clients imitieren. Diese Identitätsebene ermöglicht den Zugriff auf lokale Ressourcen wie Dateien. Beim Identitätswechsel auf dieser Ebene kann das Identitätswechseltoken nur über eine Computergrenze hinweg übergeben werden. Der [Schannel-Authentifizierungsdienst](schannel.md) unterstützt nur diese Ebene des Identitätswechsels. <br/>                                                                      |
| <span id="RPC_C_IMP_LEVEL_DELEGATE"></span><span id="rpc_c_imp_level_delegate"></span><dl> <dt>**RPC \_ \_ \_ \_ C-IMP-LEVEL-DELEGAT**</dt> <dt>4</dt> </dl>          | Der Serverprozess kann die Identität des Sicherheitskontexts des Clients im Auftrag des Clients im Auftrag des Clients imitieren. Der Serverprozess kann auch ausgehende Aufrufe an andere Server durchführen, während er im Auftrag des Clients mithilfe von Cloaking agiert. Der Server kann den Sicherheitskontext des Clients auf anderen Computern verwenden, um auf lokale und Remoteressourcen als Client zu zugreifen. Beim Identitätswechsel auf dieser Ebene kann das Identitätswechseltoken über eine beliebige Anzahl von Computergrenzen hinweg übergeben werden.<br/> |



## <a name="remarks"></a>Hinweise

[**GetUserName kann**](/windows/desktop/api/winbase/nf-winbase-getusernamea) beim Identitätswechsel auf Identifizierungsebene nicht verwendet werden. Die Problemumgehung besteht im Identitätswechsel, dem Aufrufen [**von OpenThreadToken,**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken)dem Rückgängig machen, dem [**Aufruf von GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation)und schließlich dem Aufruf von [**LookupAccountSid.**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) Mithilfe [**von CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)legt der Client die Identitätswechselebene fest.

Mithilfe [**von CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)legt der Client die Identitätswechselebene und die Proxyidentität fest, die verfügbar sind, wenn ein Server [**CoImpersonateClient aufruft.**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient) Die Identität, die der Server beim Identitätswechsel sieht, wird unter [Cloaking (Verkleinern) beschrieben.](cloaking.md) Beachten Sie, dass der Aufrufer beim Identitätswechsel normalerweise das Prozesstoken des Aufrufers und nicht das Identitätswechseltoken des Aufrufers erhält. Um das Identitätswechseltoken des Aufrufers zu empfangen, muss der Aufrufer das Verkleinern aktivieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>RpcDce.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Cloaking](cloaking.md)
</dt> </dl>

 

