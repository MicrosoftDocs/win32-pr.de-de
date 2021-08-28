---
description: ICEM08 stellt sicher, dass ein Modul kein anderes Modul ausschließt, von dem es abhängig ist.
ms.assetid: 56d115b4-7410-4db2-a9af-bc6716f3358d
title: ICEM08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c953c40d29458613b0fc2027dd691adb672eb15
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884213"
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
| ModuleA. &lt; GUID&gt; | 1033           | ModuleB. &lt; GUID&gt; | 1033             | 1.0             |



 

[ModuleExclusion-Tabelle](moduleexclusion-table.md)



| ModuleID             | ModuleLanguage | ExcludedID           | ExcludedLanguage | ExcludedMinVersion | ExcludedMaxVersion |
|----------------------|----------------|----------------------|------------------|--------------------|--------------------|
| ModuleA. &lt; GUID&gt; | 1033           | ModuleB. &lt; GUID&gt; | 1033             |                    | 1.0                |



 

Um den Fehler zu beheben, entfernen Sie entweder die Abhängigkeit oder den Ausschluss. Wenn ModuleB eine Abhängigkeit (RequiredID) von ModuleA ist, können Sie sie nicht ausschließen (wie in der ExludedID -Spalte der ModuleExclusion-Tabelle gezeigt). Wenn Sie ModuleB ausschließen müssen, müssen Sie die Abhängigkeit von ModuleA davon entfernen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Merge Module ICE Reference](merge-module-ice-reference.md)
</dt> </dl>

 

 



