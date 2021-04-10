---
description: ICE36 überprüft, ob jedes Symbol in der Symboltabelle mindestens ein Mal in der arpproducticon-Eigenschaft oder in der Klassen-, ProgID-oder Verknüpfungs Tabelle aufgeführt ist.
ms.assetid: d502c0a9-17e5-467a-8b02-8b254e77b96b
title: ICE36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f24eebc1b591edde418c59b6765d7ee91a00dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042536"
---
# <a name="ice36"></a>ICE36

ICE36 überprüft, ob jedes Symbol in der Symboltabelle mindestens ein Mal in der [**arpproducticon**](arpproducticon.md) -Eigenschaft oder in der [Klassen](class-table.md)-, [ProgID](progid-table.md)- [oder Verknüpfungs Tabelle aufgeführt](shortcut-table.md) ist.

Während der Ankündigung werden alle in der [Symboltabelle](icon-table.md) aufgeführten Symbole auf dem Computer des Benutzers installiert. Wenn nicht verwendete Symbole in der Symboltabelle vorhanden sind, kann die Installation nicht ausgeführt werden. es wird jedoch die Größe der MSI-Datei und die Zeit und den Speicherplatz, die für die Ankündigung einer Funktion erforderlich sind, unnötig vergrößert.

Wenn in der Eigenschaft oder Tabelle nicht auf ein Symbol verwiesen wird und keine Benutzeroberfläche zum Erstellen eines Verweises zur Laufzeit bereitgestellt wird, sollten Sie das Symbol entfernen, um eine bessere Leistung zu erzielen.

## <a name="result"></a>Ergebnis

ICE36 sendet eine Meldung, wenn ein Symbol in der Symboltabelle vorhanden ist, auf das in der [Klasse](class-table.md), der [ProgID](progid-table.md)oder [der Verknüpfungs Tabelle nicht](shortcut-table.md) verwiesen wird, und wenn keine Benutzeroberfläche bereitgestellt wird, um einen solchen Verweis zur Laufzeit zu erstellen.

## <a name="example"></a>Beispiel

ICE36 meldet den folgenden Fehler für das gezeigte Beispiel.

``` syntax
Icon Bloat. Icon Icon4 is not used in the Class, Shortcut, or ProgID table. This adversely affects performance.
```

[Symboltabelle](icon-table.md) (partiell)



| Name  | Daten     |
|-------|----------|
| Icon1 | Control1 |
| Icon2 | Control2 |
| Icon3 | Control3 |
| Icon4 | Control4 |



 

[ProgID-Tabelle](progid-table.md) (partiell)



| ProgID    |
|-----------|
| Property1 |



 

[Klassen Tabelle](class-table.md) (partiell)



| CLSID                                  |
|----------------------------------------|
| {3e469aba-3644-11d2-8892-00a0c981b015} |



 

Verknüpfungs [Tabelle](shortcut-table.md) (partiell)



| Abkürzung  | Symbol\_ |
|-----------|--------|
| Shortcut1 | Icon2  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



