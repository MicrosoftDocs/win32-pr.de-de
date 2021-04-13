---
title: Dynamische virtuelle Kanäle
description: Die APIs des dynamischen virtuellen Kanals (DVC) erweitern die vorhandenen virtuellen Channel-APIs für Remotedesktopdienste, die als statische virtuelle Kanal-APIs bezeichnet werden.
ms.assetid: bddf0048-482d-40f3-a973-9d7bc15be8fa
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3181c0960b50289846018c3ace773a8351cb20
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388264"
---
# <a name="dynamic-virtual-channels"></a>Dynamische virtuelle Kanäle

Die APIs des dynamischen virtuellen Kanals (DVC) erweitern die vorhandenen virtuellen Channel-APIs für Remotedesktopdienste, die als statische virtuelle Kanal-APIs bezeichnet werden. DVC-APIs erfüllen mehrere Einschränkungen, die in SVC-APIs zwischen Client und Server vorhanden waren, wie z. b.:

-   Eine begrenzte Anzahl von Kanälen
-   Paket-Wiederherstellung

DVC-APIs unterstützen Sie bei der Implementierung von Modulen auf Server-und Clientseite einer Remotedesktopdienste Verbindung, die miteinander kommunizieren.

Wie viele andere Client/Server-Architekturen wird eine Verbindung auf Grundlage eines häufig vereinbarten Daten Abschnitts hergestellt, der als Endpunkt bezeichnet wird. Ein ähnliches Beispiel ist TCP/IP, bei dem ein Endpunkt durch eine Kombination aus Server-IP-Adresse und dem Portnamen festgelegt wird. Ein weiteres Beispiel sind Named Pipes, bei denen ein Endpunkt eine Kombination aus dem Servernamen und dem Pipenamen ist. In einer Remotedesktopdienste Verbindung sind nur zwei Seiten beteiligt. Daher besteht der Endpunkt aus einer einfachen beliebigen Zeichenfolge, die die Verbindung eindeutig identifiziert. Ähnlich wie bei TCP/IP und Named Pipes können mehrere Verbindungen über denselben Endpunkt Namen initiiert werden. In diesem Sinne haben Verbindungen keine Namen. nur ein Listener, der auf eingehende Anforderungen für den Endpunkt wartet.

Die DVC-APIs bestehen aus folgendem:

-   Client-APIs

    Diese APIs sind im Remotedesktopverbindung-Client (RDC) als Plug-in verfügbar. Die Clientseite befindet sich im passiven Modus, in dem Sie auf eingehende Verbindungen lauscht, aber keine aktive Verbindung hergestellt wird.

-   Server-APIs

    Diese APIs initiieren die Verbindung aktiv.

Weitere Informationen zum Schreiben eines Moduls für einen dynamischen virtuellen Kanal (DVC) finden Sie unter [DVC-Implementierungs Details](dvc-implementation-details.md).

 

 




