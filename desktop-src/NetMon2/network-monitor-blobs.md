---
description: Das Netzwerkmonitor Binary Large Object (BLOB) ist eine generische Datenstruktur, die Konfigurations- und Standortinformationen von Netzwerkschnittstellenkarten (NICs) enthält.
ms.assetid: 910bf929-aa89-434d-83c3-07c80c627405
title: Netzwerkmonitor BLOBs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d15ce2a8f85860720c6f38b0d6c019a33e57df0a1b589ba23455db0319d0436
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799550"
---
# <a name="network-monitor-blobs"></a>Netzwerkmonitor BLOBs

Das Netzwerkmonitor Binary Large Object (BLOB) ist eine generische Datenstruktur, die Konfigurations- und Standortinformationen von Netzwerkschnittstellenkarten (NICs) enthält. Verwenden Sie BLOBs, um NICs zu darstellen und Einträge in einer Liste von NICs zu filtern. BLOBS können auch anwendungsspezifische Daten enthalten, ohne die anderen Daten zu beeinflussen, die sie enthalten. Die BLOB-Implementierung ist für alle Ebenen nicht transparent, die mit BLOB-APIs auf BLOBs zugreifen müssen.

## <a name="blob-structure"></a>BLOB-Struktur

Ein BLOB kann als hierarchische Struktur betrachtet werden, die zum Festlegen von Zeichenfolgen verwendet wird. Diese Struktur verfügt über drei Ebenen: Besitzer, Kategorie und Tag. Besitzer ist eine Zeichenfolge, die im Allgemeinen angibt, wer einen Eintrag liest. Die Kategorie ist auch eine Zeichenfolge, die eine allgemeine funktionale Gruppierung von Tags unter dem Besitzer bestimmt. Das Tag ist der tatsächliche Name des Eintrags.

Zu den strukturellen Merkmalen von BLOBs gehören:

-   BLOB-Hilfsatoren innerhalb eines Prozesses werden durch einen in jedes BLOB integrierten Mutex voneinander geschützt.
-   Jedes BLOB verfügt über eine interne Versionsnummer, sodass die Hilfsatoren sowohl aktuelle als auch zukünftige BLOB-Formulare verarbeiten können. Versionskonflikte können auftreten, wenn Sie ein BLOB über einen Remoteprozeduraufruf an einen anderen Computer senden.
-   Das BLOB selbst ist ein Zeiger auf ein void-Feld. Beachten Sie, dass Anwendungen BLOBs mit dem const-Modifizierer zuordnen sollten, um eine Änderung des Inhalts zu vermeiden. 
-   Jeder der Designatoren sowie deren Werte sind Zeichenfolgen. Beachten Sie, dass die von **GetString-Funktionen** zurückgegebenen Zeichenfolgen tatsächlich Zeiger auf das BLOB sind und nicht geändert werden sollten. Aus diesem Grund müssen diese Zeichenfolgen als **const char** _ pX* angegeben werden, damit Anwendungen sie nicht \_ versehentlich ändern.

Im Allgemeinen empfehlen alle  Parameter mit dem const-Designator dem Aufrufer, die Werte nicht zu ändern, anstatt zu verhindern, dass die Hilfsfunktionen sie ändern. Tatsächlich ändern die Hilfsfunktionen diese Werte in der Regel.

 

 



