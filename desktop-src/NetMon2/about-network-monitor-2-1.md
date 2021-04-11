---
description: Netzwerkmonitor ist eine Komponente von Microsoft Systems Management Server (SMS), die zum erkennen und Beheben von Problemen auf LANs, Wens und seriellen Links verwendet wird, auf denen Microsoft Remote Access Server (RAS) ausgeführt wird.
ms.assetid: bd273439-daa2-4263-8f12-28ec988beea0
title: Informationen zu Netzwerkmonitor 2,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f447f4763e0c73dc0dcac4cf719a0bad4b61f073
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042228"
---
# <a name="about-network-monitor-21"></a>Informationen zu Netzwerkmonitor 2,1

Netzwerkmonitor ist eine Komponente von Microsoft Systems Management Server (SMS), die zum erkennen und Beheben von Problemen auf LANs, Wens und seriellen Links verwendet wird, auf denen Microsoft Remote Access Server (RAS) ausgeführt wird. Netzwerkmonitor stellt die Analyse von Netzwerkdaten nach der Erfassung bereit.

Bei der Analyse nach der Erfassung wird der Netzwerk Datenverkehr in einer proprietären Erfassungs Datei gespeichert, sodass die erfassten Daten später analysiert werden können. In diesem Fall kann die Analyse in Form von Protokoll- [*Parser*](p.md) vorliegen, die bestimmte Netzwerk Frame Typen auswählen und die Frame Daten in der Netzwerkmonitor-Benutzeroberfläche anzeigen. oder die Analyse kann in Form von [*Experten*](e.md) vorliegen, die die Netzwerkdaten untersuchen und einen Bericht anzeigen (Experten können auch die Netzwerkdaten verändern).

Netzwerkmonitor stellt die folgenden Arten von Funktionen bereit:

-   Erfasst Netzwerkdaten im Echtzeitmodus oder im verzögerten Modus.
-   Stellt Filterfunktionen beim Erfassen von Daten bereit.
-   Verwendet Experten und Parser für eine ausführliche nach Erfassungs Analyse.

Weitere Informationen zu Netzwerkmonitor Funktionen finden Sie unter:

-   [Architektur von Experten und Parsers](expert-and-parser-architecture.md)
-   [Experten](experts.md)
-   [Parser](parsers.md)
-   [Netzwerk Paketanbieter](network-packet-providers.md)
-   [BlobNetzwerkmonitor](network-monitor-blobs.md)
-   [Seite "Ereignis Verweis"](event-reference-page.md)
-   [Erfassungs Filter](capture-filters.md)

**Windows Vista:** Netzwerkmonitor 2,1 und frühere Versionen werden auf dieser Plattform nicht unterstützt.

 

 



