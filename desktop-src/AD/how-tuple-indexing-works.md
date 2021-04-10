---
title: Funktionsweise der tupelindizierung
description: Tupelindizes werden verwendet, um Suchvorgänge zu optimieren, die 0 oder mehr mediensuchzeichenfolgen und 0 oder 1 Final-Search-Zeichen folgen haben. Sie können auch verwendet werden, um Suchvorgänge nach einer anfänglichen Such Zeichenfolge zu optimieren, wenn für dieses Attribut kein normaler Index verfügbar ist.
ms.assetid: 0f7b3f64-70cd-4581-a9ab-bb882eabef8c
ms.tgt_platform: multiple
keywords:
- tupelindizierung
- Suchen Active Directory Active Directory, Optimierung
- Active Directory, Such Optimierungs Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607b9a50ef0ec367bea95f82afd89aa39fbf5b1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724488"
---
# <a name="how-tuple-indexing-works"></a>Funktionsweise der tupelindizierung

Tupelindizes werden verwendet, um Suchvorgänge zu optimieren, die 0 oder mehr [mediensuchzeichenfolgen](search-string-types.md) und 0 oder 1 Final-Search-Zeichen folgen haben. Sie können auch verwendet werden, um Suchvorgänge nach einer anfänglichen Such Zeichenfolge zu optimieren, wenn für dieses Attribut kein normaler Index verfügbar ist.

Sie können die tupelindizierung für ein Attribut aktivieren, indem Sie im [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) -Attribut Bit 5 festlegen, das dem Wert 32 entspricht. Dieses Attribut wird im Schema Objekt festgelegt, das das Attribut darstellt, das den Tupelindex benötigt. Die Leistungseinbußen beim Aktivieren der tupelindizierung besteht darin, dass jeder für dieses Attribut festgelegte Zeichen folgen Wert in eine große Anzahl von Fragmenten im Tupelindex erweitert wird. Wenn ein Attribut erweitert wird, verbraucht es eine größere Menge an Speicherplatz in der Verzeichnis Informationsstruktur und wird auch langsamer aktualisiert.

Tupelindizes sind so konzipiert, dass die Suchvorgänge im Formular beschleunigt werden `*string*` . Die Beschleunigung kann beträchtlich sein, da diese Art von Suche nicht auf andere Weise optimiert werden kann. in der nicht optimierten Form erzwingt Sie, dass der Active Directory Server jedes Objekt im Bereich der Suche durchläuft, um die Abfrage auszuführen. Daher würde eine Basis Suche nur ein Objekt durchsuchen. Wenn Sie weniger Ressourcen benötigen, werden bei einer untergeordneten Suche nur die untergeordneten Elemente eines Objekts durchsucht (was je nach Containergröße weniger Ressourcen oder mehr Ressourcen verbrauchen kann), und eine Unterstruktur Suche durchläuft die gesamte Teilstruktur unter dem Basisobjekt, was normalerweise viele Ressourcen benötigt und aufgrund der Größe der Unterstruktur sehr langsam ist.

Tupelindizes funktionieren durch das Aufteilen einer Zeichenfolge in *Tupel*. Beispielsweise würde die Zeichenfolge "Active Directory" in die folgenden Tupel unterteilt:

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
> Wenn eine Zeichenfolge für die tupelindizierung erweitert wird, wird das Verzeichnis bei 32767 Zeichen angehalten.

 

Ein Tupelindex würde einen Eintrag für jedes dieser Tupel enthalten. Wenn ein Benutzer beispielsweise nach sucht `*cto*` , sucht der Active Directory Server nach allen Übereinstimmungen für "CTO" im Index und sucht in diesem Fall einen Zeiger zurück auf den Datensatz, der ein (tupelindiziertes)-Attribut mit dem Wert "Directory" enthielt.

Wenn die mediale Such Zeichenfolge ( `*cto*` im vorherigen Beispiel) spezifisch genug ist, ist die Suche Recht effizient, da Sie die Anzahl der Objekte, die der Active Directory Server überprüfen muss, um die Abfrage auszuführen, erheblich reduziert.

 

 