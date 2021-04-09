---
description: ICE52 prüft, ob private Eigenschaften in der AppSearch-Tabelle angezeigt werden. Siehe Informationen zu Eigenschaften.
ms.assetid: 18d1489e-666a-488d-ae12-5dbe60885a2e
title: ICE52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785dd468aaa637df02b9eb432dd77f9226d828a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867291"
---
# <a name="ice52"></a>ICE52

ICE52 prüft, ob private Eigenschaften in der [AppSearch-Tabelle](appsearch-table.md)angezeigt werden. Siehe [Informationen zu Eigenschaften](about-properties.md).

Bei Verwendung von Windows 2000 müssen alle Eigenschaften, die in der Eigenschafts Spalte der AppSearch-Tabelle festgelegt sind, öffentliche Eigenschaften sein.

## <a name="result"></a>Ergebnis

ICE52 gibt eine Warnung aus, wenn in der AppSearch-Tabelle eine private-Eigenschaft vorhanden ist.

## <a name="example"></a>Beispiel

ICE52 gibt die folgende Warnung für das gezeigte Beispiel aus.

``` syntax
Property 'Property2' in AppSearch row 'Property2'.'Signature2' 
    is not public. It should be all uppercase.
```

[AppSearch-Tabelle](appsearch-table.md)



| Eigenschaft  | Signatur  |
|-----------|------------|
| Eigenschaft1 | Signature1 |
| Eigenschaft2 | Signature2 |



 

Um diese Warnung zu beheben, ändern Sie die benutzerdefinierte öffentliche Eigenschaft: Eigenschaft2.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



