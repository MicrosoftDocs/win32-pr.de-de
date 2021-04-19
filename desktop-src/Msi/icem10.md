---
description: ICEM10 überprüft, ob ein Mergemodul nur Eigenschaften enthält, die in der Eigenschaften Tabelle zulässig sind.
ms.assetid: 9ac7a724-ea0e-4caa-bb4f-846bfb802037
title: ICEM10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80263e5033ec14bd669c5d046c7f3842d58e332f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349529"
---
# <a name="icem10"></a>ICEM10

ICEM10 überprüft, ob ein Mergemodul nur Eigenschaften enthält, die in der Eigenschaften [Tabelle](property-table.md)zulässig sind. Die folgenden produktspezifischen Eigenschaften sind in der Eigenschaften Tabelle nicht zulässig:

-   [**Productlanguage-Eigenschaft**](productlanguage.md)
-   [**ProductCode-Eigenschaft**](productcode.md)
-   [**ProductVersion-Eigenschaft**](productversion.md)
-   [**ProductName-Eigenschaft**](productname.md)
-   [**Manufacturer-Eigenschaft**](manufacturer.md)

## <a name="result"></a>Ergebnis

ICEM10 gibt einen Fehler aus, wenn ein Mergemodul eine Eigenschaft enthält, die in der [Eigenschaften Tabelle](property-table.md)nicht zulässig ist.

## <a name="example"></a>Beispiel

ICEM10 gibt die folgenden Fehlermeldungen für ein Modul aus, das die angezeigten Datenbankeinträge enthält.

``` syntax
The property 'ProductLanguage' is not allowed in a merge module.

The property 'Manufacturer' is not allowed in a merge module.
```

In der folgenden Tabelle wird eine partielle [Eigenschaften Tabelle](property-table.md)gezeigt.



| Eigenschaft                                   | Werte    |
|--------------------------------------------|-----------|
| Color                                      | Red       |
| [**Hersteller**](manufacturer.md)       | Microsoft |
| [**Productlanguage**](productlanguage.md) | 1033      |



 

Im folgenden Verfahren wird gezeigt, wie Sie Fehler beheben.

**So beheben Sie die Fehler**

1.  Entfernen Sie die Eigenschaft "[**Manufacturer**](manufacturer.md)" aus der [Eigenschaften Tabelle](property-table.md).
2.  Entfernen Sie die [**productlanguage**](productlanguage.md)-Eigenschaft aus der [Eigenschaften Tabelle](property-table.md).

## <a name="table-used-during-execution"></a>Während der Ausführung verwendete Tabelle

Die [Eigenschaften Tabelle](property-table.md) wird während der Ausführung verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eisverweis für Mergemodul](merge-module-ice-reference.md)
</dt> </dl>

 

 



