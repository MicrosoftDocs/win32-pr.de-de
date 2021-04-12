---
description: Es gibt andere Situationen, in denen ein Lese-oder Schreibvorgang mit weniger als der angeforderten Anzahl von Zeichen abgeschlossen werden kann, obwohl kein Timeout aufgetreten ist.
ms.assetid: 05f84661-34ff-4e1f-9ec8-e4682138dfee
title: Kommunikationsfehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eeace990620928ce898a3e8a31049a0083cdf07
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483286"
---
# <a name="communications-errors"></a>Kommunikationsfehler

Es gibt andere Situationen, in denen ein Lese-oder Schreibvorgang mit weniger als der angeforderten Anzahl von Zeichen abgeschlossen werden kann, obwohl kein Timeout aufgetreten ist. Nachstehend sind einige Beispiele aufgeführt:

-   Einige Treiber unterstützen die Verwendung von Sonderzeichen, die einen Lesevorgang sofort mit nur den Zeichen durchführen, die bis zu dem Zeitpunkt gelesen wurden, zu dem Sie empfangen wurden.
-   Die [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm) -Funktion kann aufgerufen werden, um ausstehende Lese-oder Schreibvorgänge vorzeitig zu beenden. Diese Funktion kann auch den Inhalt der Ausgabe-oder Eingabepuffer oder beides löschen.
-   Wenn während eines Lese-oder Schreibvorgangs ein Kommunikationsfehler auftritt, werden alle e/a-Vorgänge für die Kommunikations Ressource beendet. Unterbrechen von Bedingungen, Paritäts Fehlern oder framingfehlern sind Beispiele für derartige Fehler. Wenn ein Fehler auftritt, muss der Prozess die [**clearcommerror**](/windows/desktop/api/Winbase/nf-winbase-clearcommerror) -Funktion aufrufen, um das Fehlerflag zu löschen, bevor zusätzliche e/a-Vorgänge beginnen können. **Clearcommerror** meldet den spezifischen Fehler und den aktuellen Status des Geräts.

 

 



