---
title: Verwenden von MSMQ als RPC-Transport
description: Das RPC-Subsystem unterstützt die Verwendung von MSMQ als Transport in synchronen und asynchronen Modi.
ms.assetid: c3f96a91-b7bb-4c2a-8699-2100324af165
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a647fe4111e3ba4fc2ad0fe05fb7bcb48729a4c2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729297"
---
# <a name="using-msmq-as-an-rpc-transport"></a>Verwenden von MSMQ als RPC-Transport

Das RPC-Subsystem unterstützt die Verwendung von MSMQ als Transport in synchronen und asynchronen Modi.

Der synchrone Modus verwendet herkömmliche Remote Prozedur Aufrufe. Diese Aufrufe verwenden bekannte Endpunkte und den Nachrichten Warteschlangen Transport ( [ncadg \_ MQ](/windows/desktop/Midl/ncadg-mq)) als Transportprotokoll. Im synchronen Modus können Ihre Remote Prozeduren über \[ [](/windows/desktop/Midl/in) \] -und \[ [out](/windows/desktop/Midl/out-idl) - \] Parameter verfügen und die Standard-RPC-Sicherheitsdienste verwenden. Das RPC-Subsystem erstellt eine Antwort Warteschlange für Remote Aufrufe **\[ , die Out \]** -Parameter enthalten. Der synchrone Modus ist nützlich für Anwendungen, bei denen der Client Daten vom Server empfangen muss. Die Haupt Beschränkung für diesen Modus besteht darin, dass sowohl der Client als auch der Server ausgeführt werden müssen und für die Dauer des Aufrufs weiterhin ausgeführt werden müssen, wie bei herkömmlichen Remote Prozedur aufrufen.

Im asynchronen Modus können Client Anwendungen Aufrufe an den Server durchführen und sofort zurückkehren, unabhängig vom Status der Serveranwendung oder des Server Computers. Außerdem wird eine Teilmenge der MSMQ-Funktionen für die Verwaltung von Nachrichten Warteschlangen und des Informationsflusses zur Verfügung gestellt. Mit der [**rpcbindingsetoption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) -Funktion können Sie die Qualität des Diensts, die rufpriorität, das journalisieren, die Sicherheit und die Lebensdauer der Server Prozess Warteschlange steuern. Mit der [**rpcserveruseprotonqepex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) -Funktion können Sie Attribute der Server Prozess Warteschlange angeben, z. b. Warteschlangen Persistenz, Authentifizierung und Verschlüsselung.

Asynchrone MSMQ wird wie synchrone MSMQ implementiert. Sie müssen bekannte Endpunkte verwenden und das Transportprotokoll als [ncadg \_ MQ](/windows/desktop/Midl/ncadg-mq)definieren. Wenden Sie in der IDL-Datei das [Message](/windows/desktop/Midl/message) -Attribut auf die Funktionen an, die asynchrone Message Queueing verwenden. Beachten Sie, dass Nachrichten Funktionen \[ nur in-Parameter enthalten können \] .

 

 