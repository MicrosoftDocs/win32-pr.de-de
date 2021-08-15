---
title: Funktionsweise der Tupelindizierung
description: Tupelindizes werden verwendet, um Suchvorgänge zu optimieren, die 0 oder mehr Medial-Search-Zeichenfolgen und 0 oder 1 Zeichenfolgen für die endgültige Suche enthalten. Sie können auch verwendet werden, um Suchvorgänge für eine anfängliche Suchzeichenfolge zu optimieren, wenn kein normaler Index für dieses Attribut verfügbar ist.
ms.assetid: 0f7b3f64-70cd-4581-a9ab-bb882eabef8c
ms.tgt_platform: multiple
keywords:
- Tupelindizierung
- Suchen von Active Directory Active Directory , Optimierung
- Active Directory, Suchoptimierung Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9d15bad8de15e4f559123d2d3cb3b6b9ec6446328e6ed4c4c52cf18355d634
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188033"
---
# <a name="how-tuple-indexing-works"></a>Funktionsweise der Tupelindizierung

Tupelindizes werden verwendet, um Suchvorgänge zu optimieren, die 0 oder mehr [Medial-Search-Zeichenfolgen](search-string-types.md) und 0 oder 1 Zeichenfolgen für die endgültige Suche enthalten. Sie können auch verwendet werden, um Suchvorgänge für eine anfängliche Suchzeichenfolge zu optimieren, wenn kein normaler Index für dieses Attribut verfügbar ist.

Sie können die Tupelindizierung für ein Attribut aktivieren, indem Sie bit 5, das dem Wert 32 entspricht, im [**searchFlags-Attribut**](/windows/desktop/ADSchema/a-searchflags) festlegen. Dieses Attribut wird im Schemaobjekt festgelegt, das das Attribut darstellt, das den Tupelindex benötigt. Die Leistungssteigerung beim Aktivieren der Tupelindizierung besteht in der Erweiterung aller für dieses Attribut festgelegten Zeichenfolgenwerte in eine große Anzahl von Fragmenten im Tupelindex. Wenn ein Attribut erweitert wird, verbraucht es einen größeren Speicherplatz in der Verzeichnisinformationsstrukturdatei und wird auch langsamer aktualisiert.

Tupelindizes wurden entwickelt, um Suchvorgänge im Formular zu `*string*` beschleunigen. Die Beschleunigung kann erheblich sein, da diese Art der Suche nicht auf andere Weise optimiert werden kann, und in ihrer nicht optimierten Form erzwingt sie, dass der Active Directory-Server jedes Objekt im Bereich der Suche durchsucht, um die Abfrage auszuführen. Daher würde eine Basissuche nur ein Objekt durchsuchen, das weniger Ressourcen benötigt, eine direkte untergeordnete Suche würde nur die untergeordneten Objekte eines Objekts durchsuchen (die je nach Containergröße weniger Ressourcen oder mehr Ressourcen benötigen könnten), und eine Unterstruktursuche durchsucht die gesamte Unterstruktur unter dem Basisobjekt, was in der Regel viel Ressourcen erfordern würde und aufgrund der Unterstrukturgröße sehr langsam wäre.

Tupelindizes funktionieren, indem sie eine Zeichenfolge in *Tupel aufbrechen.* Beispielsweise würde die Zeichenfolge "Active Directory" in die folgenden Tupel zerbrochen:

-   ` "Active Dir"`
-   ` "ctive Dire"`
-   ` "tive Direc"`
-   ` "ive Direct"`
-   ` "ve Directo"`
-   ` "e Director"`
-   ` " Directory"`
-   ` "Directory"`
-   ` "irectory"`
-   ` "rectory"`
-   ` "ectory"`
-   ` "ctory"`
-   ` "tory"`
-   ` "ory"`

> [!Note]  
> Das Verzeichnis stoppt bei 32767 Zeichen, wenn eine Zeichenfolge für die Tupelindizierung erweitert wird.

 

Ein Tupelindex würde einen Eintrag für jedes dieser Tupel enthalten. Wenn ein Benutzer also nach sucht, sucht der Active Directory-Server alle Übereinstimmungen für "cto" im Index und findet in diesem Fall einen Zeiger zurück auf den Datensatz, der ein (tupelindiziertes) Attribut mit dem Wert `*cto*` "Directory" auf hatte.

Wenn die mediale Suchzeichenfolge ( im vorherigen Beispiel) spezifisch genug ist, ist die Suche sehr effizient, da sie die Anzahl der Objekte, die der Active Directory-Server überprüfen muss, um die Abfrage auszuführen, stark `*cto*` reduziert.

 

 