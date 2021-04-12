---
title: Authentication-Level Konstanten (rpcdce. h)
description: Die Konstanten auf Authentifizierungs Ebene stellen Authentifizierungs Ebenen dar, die an verschiedene Lauf Zeitfunktionen übermittelt werden.
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
ms.openlocfilehash: 114e5624b2cbc8af0b86a29daff2c1761f6fee39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518728"
---
# <a name="authentication-level-constants"></a>Konstanten auf Authentifizierungsebene

Die Konstanten auf Authentifizierungs Ebene stellen Authentifizierungs Ebenen dar, die an verschiedene Lauf Zeitfunktionen übermittelt werden. Diese Ebenen werden in der Reihenfolge der Erhöhung der Authentifizierung aufgeführt. Jede neue Ebene erhöht die Authentifizierung, die von der vorherigen Ebene bereitgestellt wird. Wenn die RPC-Lauf Zeit Bibliothek die angegebene Ebene nicht unterstützt, wird automatisch ein Upgrade auf die nächsthöhere unterstützte Ebene durchgeführt.



| Konstante                                                                                                                                                                                                                | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <dt>**Standardwert für RPC- \_ C- \_ authn \_ \_**</dt> </dl>                    | Verwendet die Standardauthentifizierungsebene für den angegebenen Authentifizierungsdienst.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <dt>**RPC- \_ C- \_ authn- \_ Ebene \_ None**</dt> </dl>                             | Führt keine Authentifizierung durch.<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <dt>**RPC- \_ C \_ authn \_ Level \_ Connect**</dt> </dl>                    | Führt nur eine Authentifizierung aus, wenn der Client eine Beziehung zu einem Server herstellt.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <dt>**RPC- \_ C \_ authn-Ebene- \_ \_ Aufruf**</dt> </dl>                             | Authentifiziert sich nur zu Beginn jedes Remote Prozedur Aufrufes, wenn der Server die Anforderung empfängt. Gilt nicht für Remote Prozedur Aufrufe, die mit den verbindungsbasierten Protokoll Sequenzen durchgeführt werden (solche, die mit dem Präfix "ncacn" beginnen). Wenn die Protokoll Sequenz in einem Bindungs handle eine Verbindungs basierte Protokoll Sequenz ist und Sie diese Ebene angeben, verwendet diese Routine stattdessen die Pkt-Konstante der RPC- \_ C- \_ authn- \_ Ebene \_ .<br/> |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <dt>**Pkt der RPC- \_ C- \_ authn- \_ Ebene \_**</dt> </dl>                                | Authentifiziert nur, dass alle empfangenen Daten vom erwarteten Client stammen. Überprüft nicht die Daten selbst.<br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <dt>**\_Pkt-Integrität der RPC C- \_ authn- \_ Ebene \_ \_**</dt> </dl> | Authentifiziert und überprüft, ob keine der zwischen Client und Server übertragenen Daten geändert wurde.<br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <dt>**\_ \_ \_ \_ Pkt- \_ Datenschutz auf RPC-C-Ebene**</dt> </dl>       | Schließt alle vorherigen Ebenen ein und stellt sicher, dass Klartext-Daten nur vom Absender und Empfänger angezeigt werden können. Im lokalen Fall umfasst dies die Verwendung eines sicheren Kanals. Im Remote Fall ist dies das Verschlüsseln des Argument Werts jedes Remote Prozedur Aufrufes.<br/>                                                                                                                                                                 |



## <a name="remarks"></a>Bemerkungen

Unabhängig von dem durch die Konstante angegebenen Wert verwendet **Ncalrpc** immer die \_ \_ \_ \_ Pkt- \_ Datenschutzebene der RPC-C-authn-Ebene.

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

[**RpcMgmtInqDefaultProtectLevel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqdefaultprotectlevel)
</dt> <dt>

[**Rpcbindinginqauthclient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[**Rpcbindinginqauthcliumtex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[**Rpcbindingsetauthinfoex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[**Rpcbindinginqauthinfoex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> </dl>

 

 





