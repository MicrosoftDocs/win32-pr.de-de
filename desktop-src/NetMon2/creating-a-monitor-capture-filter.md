---
description: Das Erstellen eines Erfassungsfilters, der mit Netzwerkmonitor funktioniert, ist ein fünfstufiger Prozess.
ms.assetid: 04be791c-43c5-44c2-8ab0-799a99974bf6
title: Erstellen eines Monitorerfassungsfilters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e9e58aebd18f861ad8fc36c4d6f718ff3e3694c828b23436764e288d083fbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064153"
---
# <a name="creating-a-monitor-capture-filter"></a>Erstellen eines Monitorerfassungsfilters

Das Erstellen eines Erfassungsfilters, der mit Netzwerkmonitor funktioniert, ist ein fünfstufiger Prozess:

-   [Festlegen des Etype- oder SAP-Filters](writing-etypesap-filter-portion.md)
-   [Schreiben eines ADDRESSTABLE-Filters](writing-addresstable-filter-portion.md)
-   [Schreiben des PATTERNMATCH-Filters](writing-the-patternmatch-filter.md)
-   [Clipping a Frame](clipping-a-frame.md)
-   [Implementieren des Erfassungsfiltercodes](implementing-the-capture-filter-code.md)

Ein [*Erfassungsfilter*](c.md) ist eine Reihe von Ergänzungen zum NPP-BLOB, mit denen ausgewählt wird, welche Frames an den Monitor zurückübergeüberträgt werden. Wenn ein Monitor das NPP-BLOB nicht ändert, wird der NPP in den promiscuous-Modus wechseln und den ganzen Netzwerkdatenverkehr an den Monitor senden. Der NPP ist am effizientesten, wenn er die an einen Treiber übergebenen Daten reduzieren kann. Daher sollte ein Monitor einen Erfassungsfilter erstellen. Ein Monitor legt seinen Erfassungsfilter fest, indem er im Aufruf der [DoConfigure-Funktion](imonitor-doconfigure.md) in das NPP-BLOB schreibt. McSVC ruft dann den NPP mit dem NPP-BLOB auf. Weitere Informationen zu Erfassungsfiltern, [](network-packet-providers.md) Netzwerkpaketanbietern für NPPs und Netzwerkmonitor Blobs in BLOB-Funktionen finden Sie unter [](capture-filters.md) [Erfassungsfilter.](network-monitor-blobs.md)

 

 



