---
description: ICEM08 stellt sicher, dass ein Modul kein anderes Modul ausschließt, von dem es abhängt.
ms.assetid: 56d115b4-7410-4db2-a9af-bc6716f3358d
title: ICEM08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9767c6748f5a21d83bddb3b5fe93a0a8d7ea67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216943"
---
# <a name="icem08"></a>ICEM08

ICEM08 stellt sicher, dass ein Modul kein anderes Modul ausschließt, von dem es abhängt.

## <a name="result"></a>Ergebnis

ICEM08 gibt einen Fehler aus, wenn ein Modul ein anderes Modul ausschließt, von dem es abhängt.

## <a name="example"></a>Beispiel

ICEM08 gibt die folgende Fehlermeldung für ein Modul mit den Datenbankeinträgen aus, die im Beispiel angezeigt werden.

``` syntax
Error: This module requires module ModuleB.<GUID> (1033v1.0) but also 
lists it as an exclusion.
```

[Moduledepenptabelle](moduledependency-table.md)



| ModuleID             | Modulelanguage | Requirements did           | Requirements-Sprache | RequiredVersion |
|----------------------|----------------|----------------------|------------------|-----------------|
| Modulea.<GUID> | 1033           | Moduleb.<GUID> | 1033             | 1.0             |



 

[Moduleausschluss-Tabelle](moduleexclusion-table.md)



| ModuleID             | Modulelanguage | Excludädid           | Excludecodlanguage | Excludedminversion | Excludedmaxversion |
|----------------------|----------------|----------------------|------------------|--------------------|--------------------|
| Modulea.<GUID> | 1033           | Moduleb.<GUID> | 1033             |                    | 1.0                |



 

Um den Fehler zu beheben, entfernen Sie entweder die Abhängigkeit oder den Ausschluss. Wenn moduleb eine Abhängigkeit (Requirements did) von modulea ist, können Sie es nicht ausschließen (wie in der Spalte exluentdid der Tabelle moduleausschluss dargestellt). Wenn Sie moduleb ausschließen müssen, müssen Sie die Abhängigkeit von modulea darauf entfernen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eisverweis für Mergemodul](merge-module-ice-reference.md)
</dt> </dl>

 

 



