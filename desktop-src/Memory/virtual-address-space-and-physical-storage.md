---
description: Die von Microsoft Windows unterstützte maximale Menge an physischem Arbeitsspeicher liegt abhängig von der Windows-Version zwischen 2 GB und 2 TB.
ms.assetid: 5e8fca7a-b85f-4bbd-80c1-e580a815fdce
title: Virtueller Adressraum und physischer Speicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d36445eb2639cbfc4db2a6e4abaf28b9af87cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528889"
---
# <a name="virtual-address-space-and-physical-storage"></a>Virtueller Adressraum und physischer Speicher

Die von Microsoft Windows unterstützte maximale Menge an physischem Arbeitsspeicher liegt abhängig von der Windows-Version zwischen 2 GB und 24 TB. Weitere Informationen finden Sie unter Arbeits [Speicher Grenzwerte für Windows-Releases](memory-limits-for-windows-releases.md). Der virtuelle Adressraum der einzelnen Prozesse kann kleiner oder größer als der auf dem Computer verfügbare physische Arbeitsspeicher sein. Die Teilmenge des virtuellen Adressraums eines Prozesses, der sich im physischen Arbeitsspeicher befindet, wird als *Workingset* bezeichnet. Wenn die Threads eines Prozesses versuchen, mehr physischen Speicher zu verwenden, als zurzeit verfügbar ist, wird ein Teil der Arbeitsspeicher Inhalte vom System auf den Datenträger über gestellt. Die Gesamtmenge des virtuellen Adressraums, der für einen Prozess verfügbar ist, wird durch den physischen Speicher und den verfügbaren freien Speicherplatz auf dem Datenträger für die Auslagerungs Datei beschränkt.

Physischer Speicher und der virtuelle Adressraum der einzelnen Prozesse sind in *Seiten*, Arbeitsspeicher Einheiten, angeordnet, deren Größe vom Host Computer abhängig ist. Auf x86-Computern beträgt die Größe der Host Seite z. b. 4 Kilobyte.

Um die Flexibilität bei der Verwaltung des Arbeitsspeichers zu maximieren, kann das System physische Arbeitsspeicher Seiten in eine und aus einer Auslagerungs Datei auf dem Datenträger verschieben. Wenn eine Seite in den physischen Speicher verschoben wird, aktualisiert das System die Seiten Zuordnungen der betroffenen Prozesse. Wenn das Systemspeicher Platz im physischen Speicher benötigt, werden die zuletzt verwendeten Seiten des physischen Speichers in die Auslagerungs Datei verschoben. Die Bearbeitung des physischen Speichers durch das System ist für Anwendungen, die nur in Ihren virtuellen Adressräumen funktionieren, vollständig transparent.

 

 



