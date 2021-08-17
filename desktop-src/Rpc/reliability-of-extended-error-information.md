---
title: Zuverlässigkeit erweiterter Fehlerinformationen
description: Erweiterte Fehlerinformationen sind nicht zuverlässig.
ms.assetid: d4735a7b-ede0-4230-b10a-bf9772aca6a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2cb85e31f993719e5f0a555a63dd83a80064ed76df1ebda43cf03f994dab9fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926838"
---
# <a name="reliability-of-extended-error-information"></a>Zuverlässigkeit erweiterter Fehlerinformationen

Erweiterte Fehlerinformationen sind nicht zuverlässig. Erweiterte Fehlerinformationen können nicht zum Erstellen von Codelogik verwendet werden. Es ist sinnvoll, das Vorhandensein erweiterter Fehlerinformationen zu überprüfen und diese Informationen zu sichern, zu speichern oder zu protokollieren. Verlassen Sie sich jedoch nicht auf die Informationen oder deren Inhalt.

Die folgenden Gründe erläutern, warum erweiterte Fehlerinformationen nicht zuverlässig sind:

-   Die Sequenz und der Inhalt der erweiterten Fehlerdatensätze hängen von der internen Architektur des Systems ab, die sich ändern kann. Ein bestimmter Vorgang kann NPFS auf aktuellen Systemen durchgehen, aber morgen könnte tcp durchgehen. Diese verschiedenen Komponenten generieren sehr unterschiedliche Fehlercodes, und Codeprüfungen sind daher grundsätzlich unzuverlässig und werden nicht empfohlen.
-   Die Weitergabe erweiterter Fehlerinformationen kann wie zuvor erläutert deaktiviert werden. Wenn Erkennungscode enthalten ist, funktioniert die Anwendung wahrscheinlich in bestimmten Umgebungen nicht mehr.
-   Die Weitergabe erweiterter Fehlerinformationen erfolgt auf bestmögliche Weise. Die Weitergabe oder Generierung erweiterter Fehlerinformationen kann fehlschlagen, wenn nicht genügend Arbeitsspeicher auf dem Computer vorhanden ist, um die Kette zu verarbeiten oder zu propagieren. Unter diesen Umständen wird die Kette gelöscht. Einige Protokolle haben eine begrenzte Länge für Fehlerpakete, da sie in der Regel nicht viele Informationen enthalten. Wenn die Länge der Kette die zulässige Länge des Pakets überschreitet, beginnt die RPC-Laufzeit damit, Informationen aus der Kette zu löschen, um die Kette in das Paket zu passen. Die Laufzeit löscht zuerst Datensätze, beginnend mit dem vorletzten Datensatz, die rückwärts gehen, bis nur die ersten und letzten Datensätze verbleiben. Wenn die Kette immer noch nicht in ein Paket passt, löscht die Laufzeit Zeichenfolgenparameter und Computernamen. Wenn ein Zeichenfolgenparameter gelöscht wird, wird der Typ des Parameters auf none festgelegt. Wenn ein Datensatz gelöscht wird, wird das Flag EEInfoNextRecordsMissing im nächsten Datensatz und EEInfoPreviousRecordsMissing im vorherigen Datensatz festgelegt.

 

 




