---
description: Die Namen der Primärschlüssel einer Mergemoduldatenbank müssen einer Standardbenennungskonvention entsprechen.
ms.assetid: 72822c25-cd21-454b-ab49-846474b55ef1
title: Benennen von Primärschlüsseln in Mergemoduldatenbanken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b5ab2f7dbb5a41f5999271e5c679b67c6ee37d9b79302509ef61e9dbca97894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627808"
---
# <a name="naming-primary-keys-in-merge-module-databases"></a>Benennen von Primärschlüsseln in Mergemoduldatenbanken

Die Namen der Primärschlüssel einer Mergemoduldatenbank müssen einer Standardbenennungskonvention entsprechen. Der Zweck dieser Benennungskonvention besteht darin, die Wahrscheinlichkeit zu verringern, dass ein Namenskonflikt zwischen den Tabellenspalten im Mergemodul und dem Zielinstallationspaket entsteht. Die Namenskonvention kann nicht auf Tabellen angewendet werden, in denen der Primärschlüssel installierbare Daten ist. Wenden Sie die Benennungskonvention nicht auf die folgenden Tabellen an:

-   [MIME-Tabelle](mime-table.md)
-   [Erweiterungstabelle](extension-table.md)
-   [Symboltabelle](icon-table.md)
-   [Verbtabelle](verb-table.md)
-   [ProgId-Tabelle](progid-table.md)

Verwenden Sie beispielsweise nicht für den Primärschlüssel der MIME-Tabelle, da dies der MIME-Typ ist und die Anwendung der Benennungsprozedur seine Bedeutung ändern würde. In diesen Fällen hängen Namenskonflikte von der Bedeutung der modulübergreifenden Eindeutigkeit der Daten ab.

Der Name eines Primärschlüssels in einem Mergemodul muss aus einem lesbaren Namen bestehen, der mit einer Zeichenfolge aus der GUID des Mergemoduls angefügt wird. Jedes Mergemodul muss über eine eigene [*GUID verfügen.*](g-gly.md) Die GUID des Mergemoduls sollte auch in der [**Revision Number Summary-Eigenschaft**](revision-number-summary.md) des Mergemoduls erstellt werden. Entwickler können GUIDs mithilfe eines Hilfsprogramms wie GUIDGEN erstellen.

Im folgenden Verfahren wird beschrieben, wie Ein primärer Datenbankschlüssel generiert wird, der der Standardbenennungskonvention entspricht. Wenden Sie das folgende Verfahren nur auf Tabellen an, in denen der Primärschlüssel keine Daten ist, die installiert werden.

**So benennen Sie einen Primärschlüssel eines Tabellendatensatzes in einem Mergemodul**

1.  Erstellen Sie den lesbaren Teil des Namens für den Primärschlüssel. Wählen Sie einen lesbaren Namen aus, der diesen Datensatz identifiziert, z. B. MyRowEntry.
2.  Generieren oder abrufen Sie die GUID des Mergemoduls. Beachten Sie, dass alle GUIDs in Großbuchstaben erstellt werden müssen. Weitere Informationen zu GUIDs finden Sie unter [GUID](guid.md). Es folgt ein Beispiel für eine GUID: {880DE2F0-CDD8-11D1-A849-006097ABDE17}. In den folgenden Schritten ändern Sie dies in eine Zeichenfolge, die an jeden Primärschlüsselnamen im Mergemodul angefügt werden muss.
3.  Entfernen Sie die geschweiften Klammern vom Anfang und Ende der GUID.
4.  Ändern Sie alle Bindestriche in Unterstriche.
5.  Fügen Sie das Ergebnis am Ende des lesbaren Teils des Primärschlüsselnamens an. Trennen Sie den lesbaren Namen durch einen Punkt von der geänderten GUID. Der Primärschlüsselname für die oben angegebene Beispiel-GUID lautet MyRowEntry.880DE2F0 \_ CDD8 \_ 11D1 \_ A849 \_ 006097ABDE17.
6.  Wiederholen Sie den Vorgang, um alle Primärschlüssel aller Tabellen im Mergemodul zu benennen.

 

 



