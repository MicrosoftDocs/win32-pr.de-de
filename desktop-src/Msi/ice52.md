---
description: ICE52 sucht in der Tabelle AppSearch nach privaten Eigenschaften. Weitere Informationen finden Sie unter Informationen zu Eigenschaften.
ms.assetid: 18d1489e-666a-488d-ae12-5dbe60885a2e
title: ICE52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96f514f38e44a802b092acff53ac14f10c5e5d32c03888b7d45540443d34be3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044040"
---
# <a name="ice52"></a>ICE52

ICE52 sucht in der [AppSearch-Tabelle](appsearch-table.md)nach privaten Eigenschaften. Weitere Informationen finden Sie unter [Informationen zu Eigenschaften.](about-properties.md)

Bei Verwendung von Windows 2000 müssen alle eigenschaften, die in der Property -Spalte der AppSearch-Tabelle festgelegt sind, öffentliche Eigenschaften sein.

## <a name="result"></a>Ergebnis

ICE52 gibt eine Warnung aus, wenn in der Tabelle AppSearch eine private Eigenschaft vorhanden ist.

## <a name="example"></a>Beispiel

ICE52 sendet die folgende Warnung für das gezeigte Beispiel.

``` syntax
Property 'Property2' in AppSearch row 'Property2'.'Signature2' 
    is not public. It should be all uppercase.
```

[AppSearch-Tabelle](appsearch-table.md)



| Eigenschaft  | Signatur  |
|-----------|------------|
| PROPERTY1 | Signatur1 |
| Property2 | Signature2 |



 

Ändern Sie zum Beheben dieser Warnung die benutzerdefinierte öffentliche Eigenschaft PROPERTY2.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



