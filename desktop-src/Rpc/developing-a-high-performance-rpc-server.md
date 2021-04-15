---
title: Entwickeln eines Hochleistungs-RPC-Servers
description: Die Informationen in diesem Abschnitt gelten für Remote Protokoll Sequenzen ncacn \_ IP \_ TCP, ncacn \_ http, ncacn \_ NP und Windows 2000 und Windows XP.
ms.assetid: 7b4239af-951b-4d1b-8ac3-224279f6929e
keywords:
- Remote Prozedur Aufruf RPC, bewährte Methoden, entwickeln eines Hochleistungs Servers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a18319c1f4ade80ae026b68c8f5540030b992b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473989"
---
# <a name="developing-a-high-performance-rpc-server"></a>Entwickeln eines Hochleistungs-RPC-Servers

Die Informationen in diesem Abschnitt gelten für Remote Protokoll Sequenzen: [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp), [**ncacn \_ http**](/windows/desktop/Midl/ncacn-http), [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np)und Windows 2000 und Windows XP.

In diesem Abschnitt werden drei Hauptaspekte der RPC-Serverleistung behandelt:

-   [Netzwerk Latenz und Durchsatz](network-latency-and-throughput.md)
-   [Skalierbarkeit](scalability.md)
-   [Sonstige RPC-Leistungs Tipps](miscellaneous-rpc-performance-tips.md)

Die Codepfad-Länge ist eine weitere primäre Leistungs Überlegung für RPC. Die Länge des Codepfade ist im Allgemeinen gut verständlich, und da Literatur und Tools in diesem Thema allgemein verfügbar sind, wird es in diesem Artikel nicht behandelt.

Eine wichtige und bewährte allgemeine Leistungs Regel, die bei der Betrachtung der RPC-Leistung beachtet werden muss, ist dies: ermitteln Sie den Engpass im System, und arbeiten Sie daran, diesen zu beheben. Beim Gating-Engpass darf es sich nicht um die RPC-Programmierung handeln. wenn dies der Fall ist, führt die Leistungsoptimierung in RPC nicht zu einer verbesserten Leistung, bis der Engpass behoben wird. Beispielsweise muss ein System, das von Ressourcenkonflikten geplagt ist, nicht die effizientere Verwendung des Netzwerks durchführen.

Wenn Ihr System in verschiedenen Umgebungen bereitgestellt wird, ist es ratsam, sicherzustellen, dass alle Aspekte des IT-Systems gut optimiert sind, da unterschiedliche Umgebungen zu unterschiedlichen Leistungs Engpässen führen können.

 

 