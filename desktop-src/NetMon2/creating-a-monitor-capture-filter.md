---
description: Das Erstellen eines Erfassungs Filters, der mit Netzwerkmonitor funktioniert, ist ein fünfstufiger Prozess.
ms.assetid: 04be791c-43c5-44c2-8ab0-799a99974bf6
title: Erstellen eines Monitor Erfassungs Filters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097a8276bd6a1f311b343787b3f06175d9b7091f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347991"
---
# <a name="creating-a-monitor-capture-filter"></a>Erstellen eines Monitor Erfassungs Filters

Das Erstellen eines Erfassungs Filters, der mit Netzwerkmonitor funktioniert, ist ein fünfstufiger Prozess:

-   [Festlegen von ETYPE oder SAP-Filter](writing-etypesap-filter-portion.md)
-   [Schreiben von adresstablem Filter](writing-addresstable-filter-portion.md)
-   [Schreiben des patternmatch-Filters](writing-the-patternmatch-filter.md)
-   [Clipping eines Frames](clipping-a-frame.md)
-   [Implementieren des Erfassungs Filter Codes](implementing-the-capture-filter-code.md)

Ein [*Erfassungs Filter*](c.md) ist eine Reihe von Ergänzungen zum NPP-BLOB, die auswählen, welche Frames an den Monitor zurückgegeben werden. Wenn der NPP-BLOB von einem Monitor nicht geändert wird, wechselt der NPP in den Modus "gemischten" und sendet den gesamten Netzwerk Datenverkehr an den Monitor. Der npp ist am effizientesten, wenn er die an einen Treiber übergebenen Daten reduzieren kann, sodass ein Monitor einen Erfassungs Filter erstellen sollte. Ein Monitor legt den Erfassungs Filter fest, indem er im Aufrufe der [doconfigure](imonitor-doconfigure.md) -Funktion in das NPP-BLOB schreibt. Anschließend ruft der mcsvc den NPP mit dem NPP-BLOB auf. Weitere Informationen zum Erfassungs Filter, zu [Netzwerk Paket Anbietern](network-packet-providers.md) in NPPs und [Netzwerkmonitor BLOBs](network-monitor-blobs.md) für BLOB-Funktionen finden Sie unter [Erfassungs Filter](capture-filters.md) .

 

 



