---
title: Verwenden von MSMQ als RPC-Transport
description: Das RPC-Subsystem unterstützt die Verwendung von MSMQ als Transport im synchronen und asynchronen Modus.
ms.assetid: c3f96a91-b7bb-4c2a-8699-2100324af165
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab18f4476815929e8a7e6fb4e4a1eef0a4e4e34754ac134f023c8551899e0138
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010678"
---
# <a name="using-msmq-as-an-rpc-transport"></a>Verwenden von MSMQ als RPC-Transport

Das RPC-Subsystem unterstützt die Verwendung von MSMQ als Transport im synchronen und asynchronen Modus.

Im synchronen Modus werden herkömmliche Remoteprozeduraufrufe verwendet. Diese Aufrufe verwenden bekannte Endpunkte und den [Nachrichtenwarteschlangentransport ncadg \_ mq](/windows/desktop/Midl/ncadg-mq)als Transportprotokoll. Im synchronen Modus können Ihre Remoteprozeduren über \[ [Ein-](/windows/desktop/Midl/in) und \] \[ [Out-Parameter](/windows/desktop/Midl/out-idl) \] verfügen und die RPC-Standardsicherheitsdienste verwenden. Das RPC-Subsystem erstellt eine Antwortwarteschlange für Remoteaufrufe mit **\[ \] Out-Parametern.** Der synchrone Modus ist nützlich für Anwendungen, in denen der Client Daten vom Server empfangen muss. Die Hauptbeschränkung dieses Modus ist, dass wie bei herkömmlichen Remoteprozeduraufrufen sowohl der Client als auch der Server ausgeführt werden müssen und für die Dauer des Aufrufs weiter ausgeführt werden müssen.

Im asynchronen Modus können Clientanwendungen den Server aufrufen und unabhängig vom Status der Serveranwendung oder des Servercomputers sofort zurückgeben. Außerdem wird eine Teilmenge der MSMQ-Features für die Verwaltung von Nachrichtenwarteschlangen und Informationsflüssen zur Verfügung gestellt. Mit [**der RpcBindingSetOption-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) können Sie die Dienstqualität, die Aufrufpriorität, das Journaling, die Sicherheit und die Lebensdauer der Serverprozesswarteschlange steuern. Mit [**der RpcServerUseProtseqEpEx-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) können Sie Attribute der Serverprozesswarteschlange angeben, z. B. Warteschlangenpersistenz, Authentifizierung und Verschlüsselung.

Sie implementieren asynchrone MSMQ wie synchrone MSMQ. Sie müssen bekannte Endpunkte verwenden und das Transportprotokoll als [ncadg \_ mq definieren.](/windows/desktop/Midl/ncadg-mq) Wenden Sie in Ihrer IDL-Datei das [Nachrichtenattribut](/windows/desktop/Midl/message) auf die Funktionen an, die asynchrones Message Queuing verwenden. Beachten Sie, dass Nachrichtenfunktionen nur \[ in \] -Parametern enthalten können.

 

 