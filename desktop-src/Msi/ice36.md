---
description: ICE36 überprüft, ob jedes Symbol in der Icon-Tabelle mindestens einmal in der ARPPRODUCTICON-Eigenschaft oder in den Tabellen Class, ProgId oder Shortcut aufgeführt ist.
ms.assetid: d502c0a9-17e5-467a-8b02-8b254e77b96b
title: ICE36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97c3d951e90ac9f3dc46a564757c1a1d5a1737bf054740e3109a26c8c7b91055
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635303"
---
# <a name="ice36"></a>ICE36

ICE36 überprüft, ob jedes Symbol in der Icon-Tabelle mindestens einmal in der [**ARPPRODUCTICON-Eigenschaft**](arpproducticon.md) oder in den [Tabellen Class,](class-table.md) [ProgId](progid-table.md)oder [Shortcut aufgeführt](shortcut-table.md) ist.

Während der Ankündigung installiert das Installationsprogramm alle Symbole, die in der [Tabelle Symbol aufgeführt sind,](icon-table.md) auf dem Computer des Benutzers. Nicht verwendete Symbole in der Icon-Tabelle verhindern nicht, dass die Installation ausgeführt wird, erhöht jedoch unnötigerweise die Größe der .msi-Datei sowie die Zeit und den Speicherplatz, die für die Ankündigung eines Features erforderlich sind.

Wenn in der Eigenschaft oder Tabelle nicht auf ein Symbol verwiesen wird und keine Benutzeroberfläche zum Erstellen eines Verweises zur Laufzeit bereitgestellt wird, sollten Sie das Symbol entfernen, um eine bessere Leistung zu erzielen.

## <a name="result"></a>Ergebnis

ICE36 stellt eine Meldung zur Verfügung, wenn in der Tabelle Icon ein Symbol vorhanden ist, auf das in den Tabellen [Class,](class-table.md) [ProgId](progid-table.md)oder [Shortcut](shortcut-table.md) nicht verwiesen wird, und wenn keine Benutzeroberfläche zum Erstellen eines solchen Verweises zur Laufzeit bereitgestellt wird.

## <a name="example"></a>Beispiel

ICE36 meldet den folgenden Fehler für das gezeigte Beispiel.

``` syntax
Icon Bloat. Icon Icon4 is not used in the Class, Shortcut, or ProgID table. This adversely affects performance.
```

[Symboltabelle](icon-table.md) (partiell)



| Name  | Daten     |
|-------|----------|
| Symbol1 | Control1 |
| Symbol2 | Control2 |
| Symbol3 | Control3 |
| Symbol4 | Control4 |



 

[ProgID-Tabelle](progid-table.md) (partiell)



| ProgID    |
|-----------|
| Property1 |



 

[Klassentabelle](class-table.md) (partiell)



| CLSID                                  |
|----------------------------------------|
| {3E469ABA-3644-11d2-8892-00A0C981B015} |



 

[Verknüpfungstabelle](shortcut-table.md) (partiell)



| Verknüpfung  | Symbol\_ |
|-----------|--------|
| Shortcut1 | Symbol2  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



