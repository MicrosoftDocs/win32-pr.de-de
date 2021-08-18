---
title: Entwickeln eines RPC-Servers mit hoher Leistung
description: Die Informationen in diesem Abschnitt gelten für Die Remoteprotokollsequenzen ncacn \_ ip \_ tcp, ncacn \_ http, ncacn np und Windows \_ 2000 und Windows XP.
ms.assetid: 7b4239af-951b-4d1b-8ac3-224279f6929e
keywords:
- Remoteprozeduraufruf-RPC , bewährte Methoden, Entwickeln eines Hochleistungsservers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 841c52587410b10ae17f2ebd858863327aaf5ab1def92600259c8e49edc87946
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021769"
---
# <a name="developing-a-high-performance-rpc-server"></a>Entwickeln eines RPC-Servers mit hoher Leistung

Die Informationen in diesem Abschnitt gelten für Remoteprotokollsequenzen: [**ncacn \_ ip \_ tcp,**](/windows/desktop/Midl/ncacn-ip-tcp) [**ncacn \_ http,**](/windows/desktop/Midl/ncacn-http) [**ncacn \_ np**](/windows/desktop/Midl/ncacn-np)und für Windows 2000 und Windows XP.

In diesem Abschnitt werden drei Hauptaspekte der RPC-Serverleistung behandelt:

-   [Netzwerklatenz und Durchsatz](network-latency-and-throughput.md)
-   [Skalierbarkeit](scalability.md)
-   [Verschiedene RPC-Tipps](miscellaneous-rpc-performance-tips.md)

Die Länge des Codepfads ist ein weiterer haupter Aspekt der Leistung für RPC. Die Länge des Codepfads ist allgemein gut bekannt, und da die Themen und Tools zu diesem Thema allgemein verfügbar sind, wird dies in diesem Artikel nicht behandelt.

Eine wichtige und bewährte allgemeine Leistungsregel, die Sie bei der Berücksichtigung der RPC-Leistung beachten sollten, ist folgende: Suchen Sie den Engpass im System, und arbeiten Sie daran, dies zu beheben. Der Gatingengpass ist möglicherweise nicht die RPC-Programmierung. Wenn dies der Fall ist, führt die Leistungsoptimierung in RPC erst dann zu einer verbesserten Leistung, wenn dieser Engpass behoben wird. Beispielsweise muss ein System, das durch Ressourcengeplagt wird, das Netzwerk nicht effizienter nutzen.

Wenn Ihr System in verschiedenen Umgebungen bereitgestellt wird, sollten Sie sicherstellen, dass alle Aspekte des Systems gut optimiert sind, da verschiedene Umgebungen zu unterschiedlichen Leistungsengpässen führen können.

 

 