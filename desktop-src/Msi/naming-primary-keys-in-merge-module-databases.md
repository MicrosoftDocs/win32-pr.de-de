---
description: Die Namen der Primärschlüssel einer mergemoduldatenbank müssen einer Standard Benennungs Konvention entsprechen.
ms.assetid: 72822c25-cd21-454b-ab49-846474b55ef1
title: Benennen von primär Schlüsseln in mergemoduldatenbanken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e5481e7fd29c4d3750e8fac01b6ca4bd6593af3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528178"
---
# <a name="naming-primary-keys-in-merge-module-databases"></a>Benennen von primär Schlüsseln in mergemoduldatenbanken

Die Namen der Primärschlüssel einer mergemoduldatenbank müssen einer Standard Benennungs Konvention entsprechen. Der Zweck dieser Benennungs Konvention besteht darin, die Möglichkeit zu verringern, einen namens Konflikt zwischen den Tabellen Spalten im Mergemodul und dem Ziel Installationspaket zu erstellen. Die Benennungs Konvention kann nicht auf Tabellen angewendet werden, in denen der Primärschlüssel installierbare Daten ist. Wenden Sie die Benennungs Konvention nicht auf die folgenden Tabellen an:

-   [MIME-Tabelle](mime-table.md)
-   [Erweiterungs Tabelle](extension-table.md)
-   [Symboltabelle](icon-table.md)
-   [Verb Tabelle](verb-table.md)
-   [ProgID-Tabelle](progid-table.md)

Verwenden Sie z. b. nicht für den Primärschlüssel der MIME-Tabelle, da dies der MIME-Typ ist, und wenn Sie die Benennungs Prozedur anwenden, ändert sich ihre Bedeutung. In diesen Fällen sind Namenskonflikte abhängig von der Bedeutung der Daten, die über Module hinweg eindeutig sind.

Der Name eines Primärschlüssels in einem Mergemodul muss aus einem lesbaren Namen bestehen, der mit einer aus der GUID des Mergemoduls erstellten Zeichenfolge versehen ist. Jedes Mergemodul muss über eine eigene [*GUID*](g-gly.md)verfügen. Die GUID des Mergemoduls sollte auch in der Eigenschaft [**Revisionsnummern Zusammenfassung**](revision-number-summary.md) des Mergemoduls erstellt werden. Entwickler können GUIDs mithilfe eines Hilfsprogramms wie GUIDGEN erstellen.

Im folgenden Verfahren wird beschrieben, wie ein primärer Daten Bank Schlüssel generiert wird, der der Standard Benennungs Konvention entspricht. Wenden Sie das folgende Verfahren nur auf Tabellen an, in denen der Primärschlüssel nicht als Daten installiert wird.

**So benennen Sie einen Primärschlüssel eines Tabellendaten Satzes in einem Mergemodul**

1.  Erstellen Sie den lesbaren Teil des Namens für den Primärschlüssel. Wählen Sie einen lesbaren Namen aus, der diesen Datensatz identifiziert, z. b. myrowentry.
2.  Generieren oder Abrufen der GUID des Mergemoduls. Beachten Sie, dass alle GUIDs in Großbuchstaben erstellt werden müssen. Weitere Informationen zu GUIDs finden Sie unter [GUID](guid.md). Im folgenden finden Sie ein Beispiel für eine GUID: {880de2f 0-cdd8-11d1-a849-006097abde17}. In den folgenden Schritten ändern Sie dies in eine Zeichenfolge, die an jeden Primärschlüssel Namen im Mergemodul angehängt werden muss.
3.  Entfernen Sie die geschweiften Klammern am Anfang und am Ende der GUID.
4.  Ändern Sie alle Bindestriche in Unterstriche.
5.  Fügen Sie das Ergebnis an das Ende des lesbaren Teils des Primärschlüssel namens an. Trennen Sie den lesbaren Namen von der geänderten GUID um einen bestimmten Zeitraum. Der Primärschlüssel Name für die oben angegebene beispielguid wird myrowentry. 880un2f 0 \_ CDD8 \_ 11d1 \_ A849 \_ 006097abde17.
6.  Wiederholen Sie den Vorgang, um alle Primärschlüssel aller Tabellen im Mergemodul zu benennen.

 

 



