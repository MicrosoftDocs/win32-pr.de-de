---
title: Konstanten der Authentifizierungsebene (Rpcdce.h)
description: Diese Werte geben eine Authentifizierungsebene an, die den Umfang der bereitgestellten Authentifizierung angibt, um die Integrität der Daten zu schützen. Jede Ebene enthält den Von den vorherigen Ebenen bereitgestellten Schutz.
ms.assetid: 06c409e4-3772-45cf-8c31-c64f99aca244
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
- rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcdcdf2ec566bafc962114d691c1962533b843d4c9299d01107eaaf132ea3050
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048678"
---
# <a name="authentication-level-constants"></a>Konstanten der Authentifizierungsebene

Diese Werte geben eine Authentifizierungsebene an, die den Umfang der bereitgestellten Authentifizierung angibt, um die Integrität der Daten zu schützen. Jede Ebene enthält den Von den vorherigen Ebenen bereitgestellten Schutz.



| Konstante/Wert                                                                                                                                                                                                                                                                 | Beschreibung                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ LEVEL \_ DEFAULT**</dt> <dt>0</dt> </dl>                    | Weist DCOM an, die Authentifizierungsebene mithilfe des normalen Algorithmus für die Aushandlung der Sicherheitsaushandlung zu wählen. Weitere Informationen finden Sie unter [Security Negotiation .](security-blanket-negotiation.md) <br/> |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <dt>**RPC \_ \_C-AUTHENTIFIZIERUNGSEBENE \_ \_ NONE**</dt> <dt>1</dt> </dl>                             | Führt keine Authentifizierung aus.<br/>                                                                                                                                                                         |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <dt>**RPC \_ \_C-AUTHENTIFIZIERUNGSEBENE \_ \_ CONNECT**</dt> <dt>2</dt> </dl>                    | Authentifiziert die Anmeldeinformationen des Clients nur, wenn der Client eine Beziehung mit dem Server einigt. Datagrammtransporte verwenden stattdessen immer RPC \_ AUTHN \_ LEVEL \_ PKT. <br/>                        |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <dt>**RPC \_ \_ \_ C-AUTHENTIFIZIERUNGSEBENENAUFRUF \_**</dt> <dt>3</dt> </dl>                             | Authentifiziert sich nur am Anfang jedes Remoteprozeduraufrufs, wenn der Server die Anforderung empfängt. Datagrammtransporte verwenden stattdessen RPC \_ C \_ AUTHN \_ LEVEL \_ PKT.<br/>                                  |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <dt>**RPC \_ \_ \_ C-AUTHENTIFIZIERUNGSEBENE \_ PKT**</dt> <dt>4</dt> </dl>                                | Authentifiziert, dass alle empfangenen Daten vom erwarteten Client empfangen werden.<br/>                                                                                                                                   |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <dt>**RPC \_ \_C-AUTHENTIFIZIERUNGSEBENE \_ \_ \_ PKT-INTEGRITÄT**</dt> <dt>5</dt> </dl> | Authentifiziert und überprüft, ob keine der zwischen Client und Server übertragenen Daten geändert wurde.<br/>                                                                                           |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <dt>**RPC \_ DATENSCHUTZ AUF \_ \_ C-AUTHENTIFIZIERUNGSEBENE \_ PKT \_**</dt> <dt>6</dt> </dl>       | Authentifiziert alle vorherigen Ebenen und verschlüsselt den Argumentwert jedes Remoteprozeduraufrufs.<br/>                                                                                                    |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Rpcdce.h</dt> </dl> |



 

 





