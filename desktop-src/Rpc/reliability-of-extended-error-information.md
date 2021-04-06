---
title: Zuverlässigkeit erweiterter Fehlerinformationen
description: Erweiterte Fehlerinformationen sind nicht zuverlässig.
ms.assetid: d4735a7b-ede0-4230-b10a-bf9772aca6a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20edfbaa68f2a9ce80893f4f47bba33ec5ce595
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707325"
---
# <a name="reliability-of-extended-error-information"></a>Zuverlässigkeit erweiterter Fehlerinformationen

Erweiterte Fehlerinformationen sind nicht zuverlässig. Erweiterte Fehlerinformationen können nicht zum Entwickeln von Code Logik verwendet werden. Es ist angemessen, das vorhanden sein von erweiterten Fehlerinformationen zu überprüfen, und wenn dies der Fall ist, um diese Informationen zu speichern, zu speichern oder zu protokollieren. Verlassen Sie sich jedoch nicht auf die Informationen oder ihren Inhalt.

Die folgenden Gründe erläutern, warum erweiterte Fehlerinformationen nicht zuverlässig sind:

-   Die Reihenfolge und der Inhalt der erweiterten Fehler Datensätze hängen von der internen Architektur des Systems ab, das geändert werden kann. Ein bestimmter Vorgang kann NPFS auf aktuellen Systemen durchlaufen, aber morgen könnte über TCP. Diese unterschiedlichen Komponenten generieren sehr unterschiedliche Fehlercodes, und Code Überprüfungen sind daher grundsätzlich unzuverlässig und nicht empfehlenswert.
-   Die Weitergabe erweiterter Fehlerinformationen kann wie zuvor erläutert deaktiviert werden. Wenn Erkennungs Code enthalten ist, wird die Anwendung wahrscheinlich nicht mehr in bestimmten Umgebungen funktionieren.
-   Die Weitergabe erweiterter Fehlerinformationen wird auf bestmögliche Weise ausgeführt. Die Weitergabe oder Generierung erweiterter Fehlerinformationen kann fehlschlagen, wenn nicht genügend Arbeitsspeicher auf dem Computer vorhanden ist, um die Kette zu verarbeiten oder weiterzugeben. Unter diesen Umständen wird die Kette gelöscht. Einige Protokolle weisen eine begrenzte Länge für fehlerpakete auf, da Sie in der Regel keine großen Informationen enthalten. Wenn die Länge der Kette die zulässige Länge des Pakets überschreitet, beginnt die RPC-Laufzeit mit dem Löschen von Informationen aus der Kette, wenn versucht wird, die Kette in das Paket einzufügen. Die Laufzeit löscht zunächst Datensätze, beginnend mit dem vorletzten Datensatz, bis die ersten und letzten Datensätze verbleiben. Wenn die Kette immer noch nicht in ein Paket passt, löscht die Laufzeit Zeichen folgen Parameter und Computernamen. Wenn ein Zeichen folgen Parameter gelöscht wird, wird der Typ des Parameters auf "None" festgelegt. Wenn ein Datensatz gelöscht wird, wird das Flag eeinfonextrecordsmissing im nächsten Datensatz festgelegt, und eeinf opreviousrecordsmissing wird im vorherigen Datensatz festgelegt.

 

 




