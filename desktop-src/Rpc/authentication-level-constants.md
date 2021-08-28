---
title: Authentication-Level Konstanten (Rpcdce.h)
description: Die Konstanten auf Authentifizierungsebene stellen Authentifizierungsebenen dar, die an verschiedene Laufzeitfunktionen übergeben werden.
ms.assetid: b8bb2517-e1a0-4607-a672-259f8686fc3e
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_LEVEL_DEFAULT
- RPC_C_AUTHN_LEVEL_NONE
- RPC_C_AUTHN_LEVEL_CONNECT
- RPC_C_AUTHN_LEVEL_CALL
- RPC_C_AUTHN_LEVEL_PKT
- RPC_C_AUTHN_LEVEL_PKT_INTEGRITY
- RPC_C_AUTHN_LEVEL_PKT_PRIVACY
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03c27fa63a437c3c8a93c3d2e5e1f1983e341d5709e986c83459a3f505b46c6f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080920"
---
# <a name="authentication-level-constants"></a>Konstanten auf Authentifizierungsebene

Die Konstanten auf Authentifizierungsebene stellen Authentifizierungsebenen dar, die an verschiedene Laufzeitfunktionen übergeben werden. Diese Ebenen werden in der Reihenfolge aufgeführt, in der die Authentifizierung erhöht wird. Jede neue Ebene fügt der Authentifizierung hinzu, die von der vorherigen Ebene bereitgestellt wird. Wenn die RPC-Laufzeitbibliothek die angegebene Ebene nicht unterstützt, wird automatisch ein Upgrade auf die nächste höhere unterstützte Ebene ausgeführt.



| Konstante                                                                                                                                                                                                                | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ LEVEL \_ DEFAULT**</dt> </dl>                    | Verwendet die Standardauthentifizierungsebene für den angegebenen Authentifizierungsdienst.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ LEVEL \_ NONE**</dt> </dl>                             | Führt keine Authentifizierung aus.<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ LEVEL \_ CONNECT**</dt> </dl>                    | Führt nur eine Authentifizierung aus, wenn der Client eine Beziehung zu einem Server herstellt.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <dt>**\_ \_ RPC-C-AUTHENTIFIZIERUNGSEBENENAUFRUF \_ \_**</dt> </dl>                             | Authentifiziert sich nur am Anfang jedes Remoteprozeduraufrufs, wenn der Server die Anforderung empfängt. Gilt nicht für Remoteprozeduraufrufe, die mithilfe der verbindungsbasierten Protokollsequenzen (die mit dem Präfix "ncacn" beginnen) vorgenommen werden. Wenn die Protokollsequenz in einem Bindungshand handle eine verbindungsbasierte Protokollsequenz ist und Sie diese Ebene angeben, verwendet diese Routine stattdessen die RPC \_ C \_ AUTHN \_ LEVEL \_ PKT-Konstante.<br/> |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ LEVEL \_ PKT**</dt> </dl>                                | Authentifiziert nur, dass alle empfangenen Daten vom erwarteten Client empfangen werden. Überprüft die Daten selbst nicht.<br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <dt>**PKT-INTEGRITÄT AUF \_ \_ \_ \_ RPC-C-AUTHENTIFIZIERUNGSEBENE \_**</dt> </dl> | Authentifiziert und überprüft, ob keine der zwischen Client und Server übertragenen Daten geändert wurde.<br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**</dt> </dl>       | Schließt alle vorherigen Ebenen ein und stellt sicher, dass Klartextdaten nur für den Absender und den Empfänger angezeigt werden können. Im lokalen Fall umfasst dies die Verwendung eines sicheren Kanals. Im Remotefall umfasst dies die Verschlüsselung des Argumentwerts jedes Remoteprozeduraufrufs.<br/>                                                                                                                                                                 |



## <a name="remarks"></a>Hinweise

Unabhängig vom durch die Konstante angegebenen Wert verwendet **ncalrpc** immer RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY.

## <a name="requirements"></a>Requirements (Anforderungen)



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

[**RpcMgmtInqDefaultProtectLevel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqdefaultprotectlevel)
</dt> <dt>

[**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[**RpcBindingInqAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> </dl>

 

 





