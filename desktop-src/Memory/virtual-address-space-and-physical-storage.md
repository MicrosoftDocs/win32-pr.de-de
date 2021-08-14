---
description: Die maximale Menge an physischem Speicher, die von Microsoft Windows unterstützt wird, liegt je nach Version des Windows.
ms.assetid: 5e8fca7a-b85f-4bbd-80c1-e580a815fdce
title: Virtueller Adressraum und physische Storage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 774e0af302fbd965f16b09a88d6dabb7c95948855c8d939d3c856ebe098337d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386155"
---
# <a name="virtual-address-space-and-physical-storage"></a>Virtueller Adressraum und physische Storage

Die maximale Menge an physischem Speicher, die von Microsoft Windows unterstützt wird, liegt je nach Version des Windows. Weitere Informationen finden Sie unter [Arbeitsspeicherlimits für Windows Releases](memory-limits-for-windows-releases.md). Der virtuelle Adressraum der einzelnen Prozesse kann kleiner oder größer sein als der gesamte physische Arbeitsspeicher, der auf dem Computer verfügbar ist. Die Teilmenge des virtuellen Adressraums eines Prozesses, der sich im physischen Speicher befindet, wird als *Arbeitssatz bezeichnet.* Wenn die Threads eines Prozesses versuchen, mehr physischen Arbeitsspeicher zu verwenden, als derzeit verfügbar ist, seitent das System einen Teil des Arbeitsspeicherinhalts auf den Datenträger. Die Gesamtmenge des für einen Prozess verfügbaren virtuellen Adressraums wird durch den physischen Speicher und den freien Speicherplatz auf dem Datenträger beschränkt, der für die Auslagerungsdatei verfügbar ist.

Physischer Speicher und der virtuelle Adressraum der einzelnen Prozesse sind in Seiten *und* Arbeitsspeichereinheiten organisiert, deren Größe vom Hostcomputer abhängt. Auf x86-Computern beträgt die Hostseitengröße beispielsweise 4 KB.

Um seine Flexibilität bei der Verwaltung des Arbeitsspeichers zu maximieren, kann das System Seiten des physischen Speichers in eine und aus einer Auslagerungsdatei auf dem Datenträger verschieben. Wenn eine Seite im physischen Speicher verschoben wird, aktualisiert das System die Seitenzuordnungen der betroffenen Prozesse. Wenn das System Speicherplatz im physischen Speicher benötigt, verschiebt es die seiten mit dem geringsten Physischen Speicher in die Auslagerungsdatei. Die Manipulation des physischen Speichers durch das System ist für Anwendungen, die nur in ihren virtuellen Adressräumen ausgeführt werden, vollständig transparent.

 

 



