---
description: ICEM10 überprüft, ob ein Mergemodul nur Eigenschaften enthält, die in der Eigenschaftentabelle zulässig sind.
ms.assetid: 9ac7a724-ea0e-4caa-bb4f-846bfb802037
title: ICEM10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bb9634ecec212954031e665fa0ebdc3c19856a9bcd02d894eb6e579455d059b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129410"
---
# <a name="icem10"></a>ICEM10

ICEM10 überprüft, ob ein Mergemodul nur Eigenschaften enthält, die in der [Eigenschaftentabelle zulässig sind.](property-table.md) Die folgenden produktspezifischen Eigenschaften sind in der Eigenschaftentabelle nicht zulässig:

-   [**ProductLanguage-Eigenschaft**](productlanguage.md)
-   [**ProductCode-Eigenschaft**](productcode.md)
-   [**ProductVersion-Eigenschaft**](productversion.md)
-   [**ProductName-Eigenschaft**](productname.md)
-   [**Manufacturer-Eigenschaft**](manufacturer.md)

## <a name="result"></a>Ergebnis

ICEM10 gibt einen Fehler aus, wenn ein Mergemodul eine Eigenschaft enthält, die in der [Eigenschaftentabelle nicht zulässig ist.](property-table.md)

## <a name="example"></a>Beispiel

ICEM10 stellt die folgenden Fehlermeldungen für ein Modul mit den angezeigten Datenbankeinträgen zur Verfügung.

``` syntax
The property 'ProductLanguage' is not allowed in a merge module.

The property 'Manufacturer' is not allowed in a merge module.
```

Die folgende Tabelle zeigt eine partielle [Eigenschaftentabelle.](property-table.md)



| Eigenschaft                                   | Werte    |
|--------------------------------------------|-----------|
| Color                                      | Red       |
| [**Hersteller**](manufacturer.md)       | Microsoft |
| [**ProductLanguage**](productlanguage.md) | 1033      |



 

Im folgenden Verfahren wird gezeigt, wie Sie Fehler beheben.

**So beheben Sie die Fehler**

1.  Entfernen Sie die [**Manufacturer-Eigenschaft**](manufacturer.md)aus der [Eigenschaftentabelle](property-table.md).
2.  Entfernen Sie die [**ProductLanguage-Eigenschaft**](productlanguage.md)aus der [Eigenschaftentabelle](property-table.md).

## <a name="table-used-during-execution"></a>Während der Ausführung verwendete Tabelle

Die [Eigenschaftentabelle](property-table.md) wird während der Ausführung verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Merge Module ICE Reference](merge-module-ice-reference.md)
</dt> </dl>

 

 



