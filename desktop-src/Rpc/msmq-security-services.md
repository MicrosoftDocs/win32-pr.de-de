---
title: MSMQ-Sicherheitsdienste
description: Synchrone RPC-Nachrichten können alle Sicherheitsfeatures verwenden, die über die RPC-Laufzeit verfügbar sind. Weitere Informationen finden Sie unter Sicherheit.
ms.assetid: 0f4d45c4-7457-4449-8736-e141a95f6930
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f142d83c003f1293556786167222a4e9e88d3912786aa328319efa7fb0ea345d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019650"
---
# <a name="msmq-security-services"></a>MSMQ-Sicherheitsdienste

Synchrone RPC-Nachrichten können alle Sicherheitsfeatures verwenden, die über die RPC-Laufzeit verfügbar sind. Weitere Informationen finden Sie unter [Sicherheit.](security.md)

Asynchrone \[ [](/windows/desktop/Midl/message) \] Nachrichtenaufrufe können keine RPC-Sicherheit verwenden, da kein Handshake zwischen Client und Server vorhanden ist. Tatsächlich wird der Server zum Zeitpunkt des Aufrufs möglicherweise nicht einmal ausgeführt. Um auf die von Message Queuing Services (MSMQ) bereitgestellten Sicherheitsdienste zuzugreifen, sollte die Clientanwendung [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) aufrufen, um die Ebene der Authentifizierung und des Datenschutzes für ihre Aufrufe an den Server zu steuern.

Die Serveranwendung kann [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) innerhalb eines Remoteprozeduraufrufs aufrufen, um die Sicherheitsstufe für diesen Aufruf zu bestimmen. Die Zuordnung zwischen RPC-Sicherheitskonstanten und MSMQ-Sicherheit ist in der folgenden Tabelle dargestellt.



| RPC-Sicherheitsstufe                | Beschreibung                                                                                |
|-----------------------------------|--------------------------------------------------------------------------------------------|
| \_RPC-AUTHENTIFIZIERUNGSEBENE \_ \_ KEINE           | Der Aufruf ist nicht authentifiziert oder verschlüsselt.                                                |
| \_ \_ \_ PKT-INTEGRITÄT AUF RPC-AUTHENTIFIZIERUNGSEBENE \_ | Der Aufruf wird mithilfe der MSMQ-Sicherheit authentifiziert.                                             |
| \_PKT-DATENSCHUTZ AUF RPC-AUTHENTIFIZIERUNGSEBENE \_ \_ \_   | Der Aufruf wird authentifiziert und verschlüsselt, während er zwischen client- und serverwarteschlangenverschlüsselt wird. |



 

Der Server kann auch die Aufrufauthentifizierung und -verschlüsselung erzwingen, indem [**er RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) aufruft und die RPC \_ C MQ \_ \_ AUTHN \_ LEVEL \_ NONE-, RPC \_ C MQ \_ \_ AUTHN \_ LEVEL \_ PKT \_ INTEGRITY- und RPC C MQ \_ \_ \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY-Flags in der [**RPC \_ POLICY-Struktur**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) festlegt.

 

 