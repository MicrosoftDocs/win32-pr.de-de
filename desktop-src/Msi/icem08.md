---
description: ICEM08 stellt sicher, dass ein Modul kein anderes Modul ausschließt, von dem es abhängig ist.
ms.assetid: 56d115b4-7410-4db2-a9af-bc6716f3358d
title: ICEM08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43f5d0076de382889e5fd3df8a03dddb51c6a73eb5a4f825068f6cd66ad24d07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811010"
---
# <a name="icem08"></a>ICEM08

ICEM08 stellt sicher, dass ein Modul kein anderes Modul ausschließt, von dem es abhängig ist.

## <a name="result"></a>Ergebnis

ICEM08 gibt einen Fehler aus, wenn ein Modul ein anderes Modul ausschließt, von dem es abhängt.

## <a name="example"></a>Beispiel

ICEM08 stellt die folgende Fehlermeldung für ein Modul mit den im Beispiel gezeigten Datenbankeinträgen zur Verfügung.

``` syntax
Error: This module requires module ModuleB.<GUID> (1033v1.0) but also 
lists it as an exclusion.
```

[ModuleDependency-Tabelle](moduledependency-table.md)



| ModuleID             | ModuleLanguage | RequiredID           | RequiredLanguage | RequiredVersion |
|----------------------|----------------|----------------------|------------------|-----------------|
| Modulea.<GUID> | 1033           | ModuleB.<GUID> | 1033             | 1.0             |



 

[ModuleExclusion-Tabelle](moduleexclusion-table.md)



| ModuleID             | ModuleLanguage | ExcludedID           | ExcludedLanguage | ExcludedMinVersion | ExcludedMaxVersion |
|----------------------|----------------|----------------------|------------------|--------------------|--------------------|
| Modulea.<GUID> | 1033           | ModuleB.<GUID> | 1033             |                    | 1.0                |



 

Um den Fehler zu beheben, entfernen Sie entweder die Abhängigkeit oder den Ausschluss. Wenn ModuleB eine Abhängigkeit (RequiredID) von ModuleA ist, können Sie sie nicht ausschließen (wie in der ExludedID -Spalte der ModuleExclusion-Tabelle gezeigt). Wenn Sie ModuleB ausschließen müssen, müssen Sie die Abhängigkeit von ModuleA davon entfernen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Merge Module ICE Reference](merge-module-ice-reference.md)
</dt> </dl>

 

 



