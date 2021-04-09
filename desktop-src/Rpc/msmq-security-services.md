---
title: MSMQ-Sicherheitsdienste
description: Synchrone RPC-Nachrichten können beliebige Sicherheitsfunktionen verwenden, die zur RPC-Laufzeit verfügbar sind. Weitere Informationen finden Sie unter Sicherheit.
ms.assetid: 0f4d45c4-7457-4449-8736-e141a95f6930
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd2e12cd9f32a571088de769adb079327caab9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101986"
---
# <a name="msmq-security-services"></a>MSMQ-Sicherheitsdienste

Synchrone RPC-Nachrichten können beliebige Sicherheitsfunktionen verwenden, die zur RPC-Laufzeit verfügbar sind. Weitere Informationen finden Sie unter [Sicherheit](security.md) .

Asynchrone \[ [Nachrichten](/windows/desktop/Midl/message) \] Aufrufe können keine RPC-Sicherheit verwenden, da kein Handshake zwischen Client und Server vorliegt. Tatsächlich wird der Server möglicherweise nicht einmal zum Zeitpunkt des Aufrufes ausgeführt. Um auf die von Message Queuing Services (MSMQ) bereitgestellten Sicherheitsdienste zuzugreifen, sollte die Client Anwendung [**rpcbindingsetauthinfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) aufrufen, um den Grad der Authentifizierung und den Datenschutz für Ihre Aufrufe an den Server zu steuern.

Die Serveranwendung kann [**rpcbindinginqauthclient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) innerhalb eines Remote Prozedur Aufrufes aufzurufen, um die Sicherheitsstufe für diesen-Befehl zu ermitteln. Die Zuordnung zwischen den RPC-Sicherheits Konstanten und der MSMQ-Sicherheit ist in der folgenden Tabelle dargestellt.



| RPC-Sicherheitsstufe                | BESCHREIBUNG                                                                                |
|-----------------------------------|--------------------------------------------------------------------------------------------|
| RPC \_ authn \_ Level \_ None           | Der-Befehl wird weder authentifiziert noch verschlüsselt.                                                |
| Pkt-Integrität der RPC- \_ authn- \_ Ebene \_ \_ | Der-Rückruf wird mithilfe der MSMQ-Sicherheit authentifiziert.                                             |
| Datenschutz auf RPC- \_ authn- \_ Ebene \_ Pkt \_   | Der-Rückruf wird bei der Übertragung zwischen der Client-und der Server Warteschlange authentifiziert und verschlüsselt. |



 

Der Server kann auch die Aufruf Authentifizierung und-Verschlüsselung erzwingen, indem er [**rpcserveruseprotseqepex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) aufruft \_ und \_ \_ \_ in der Struktur der RPC-Richtlinie den Wert für RPC-c MQ authn Level \_ None, RPC c MQ authn Level \_ \_ \_ \_ \_ Pkt \_ Integrity und RPC \_ c \_ MQ \_ authn \_ Level \_ Pkt- \_ [**\_**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) datenschutzkennzeichen festlegt.

 

 