---
description: ICEM02 überprüft, ob alle Modulabhängigkeiten und -ausschlüsse mit dem aktuellen Modul verknüpft sind.
ms.assetid: c7d77cb6-0ee6-4857-a749-7908e1c5fcda
title: ICEM02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 332ad83ba753984d752a78bebc19bc17e3b5d25ef8b580f9f105a9577d016318
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430820"
---
# <a name="icem02"></a>ICEM02

ICEM02 überprüft, ob alle Modulabhängigkeiten und -ausschlüsse mit dem aktuellen Modul verknüpft sind.

Mergemodul-ICEs werden in einer Mergemodul-CUB-Datei namens Mergemod.cub und nicht in der CUB-Datei gespeichert, die die für die Paketvalidierung verwendeten ICEs enthält.

## <a name="result"></a>Ergebnis

ICEM02 sendet Fehlermeldungen, wenn die Moduldatenbank versucht, Abhängigkeiten oder Ausschlüsse anzugeben, die sich nicht auf das aktuelle Modul beziehen. ICEM02 sendet eine Fehlermeldung, wenn die Moduldatenbank versucht, das aktuelle Modul als abhängig oder als ausgeschlossen anzugeben.

## <a name="example"></a>Beispiel

ICEM02 gibt die folgenden Fehlermeldungen für ein Modul mit den unten gezeigten Datenbankeinträgen aus.

``` syntax
The dependency OtherModule.GUID2.1033.OtherModule.GUID3.0 in the 
ModuleDependency table creates a dependency for an unrelated module. A 
module can only define dependencies for itself

This module is listed as depending on itself!

The exclusion OtherModule.GUID2.1033.OtherModule.GUID3.0 in the 
ModuleExclusion table creates an excluded module for an unrelated 
module. A module can only define exclusions for itself.

This module excludes itself from the target database!
```

[Tabelle "ModuleSignature"](modulesignature-table.md)



| ModuleID         | Sprache | Version |
|------------------|----------|---------|
| MyModule. *GUID1* | 1033     | 1.0     |



 

[Modulabhängigkeitstabelle](moduledependency-table.md)



| ModuleID            | ModuleLanguage | RequiredID          | RequiredLanguage | RequiredVersion |
|---------------------|----------------|---------------------|------------------|-----------------|
| OtherModule. *GUID2* | 1033           | OtherModule. *GUID3* | 0                | 1.0             |
| MyModule. *GUID1*    | 1033           | MyModule. *GUID1*    | 1033             | 1.2             |



 

[ModuleExclusion-Tabelle](moduleexclusion-table.md) (partiell)



| ModuleID            | ModuleLanguage | ExcludedID          | ExcludedLanguage |
|---------------------|----------------|---------------------|------------------|
| OtherModule. *GUID2* | 1033           | OtherModule. *GUID3* | 0                |
| MyModule. *GUID1*    | 1033           | MyModule. *GUID1*    | 1033             |



 

Das Mergemodul ICE sendet den ersten Fehler, da die der ersten Zeile in der Tabelle ModuleDependency keine erforderliche Abhängigkeit für das aktuelle Modul angibt, das in der Tabelle ModuleSignature angegeben ist. Die Abhängigkeiten eines Moduls können nur in einer eigenen ModuleDependency-Tabelle angegeben werden. Wenn OtherModule. *GUID3* ist für das aktuelle Modul erforderlich. Ersetzen Sie die ersten beiden Spalten der Zeile durch die Daten aus der Tabelle ModuleSignature. Wenn OtherModule. *GUID3* ist für dieses Modul nicht erforderlich. Löschen Sie diese Zeile.

Das Mergemodul ICE sendet den zweiten Fehler, da ein Modul keine Abhängigkeit von sich selbst angeben kann.

Das Mergemodul ICE sendet den dritten Fehler aufgrund der ersten Zeile in der Tabelle ModuleExclusion, die keinen erforderlichen Ausschluss für das aktuelle Modul angibt, das in der Tabelle ModuleSignature angegeben ist. Die Ausschlüsse eines Moduls können nur in einer eigenen ModuleExclusion-Tabelle angegeben werden. Wenn das aktuelle Modul OtherModule ausschließt. *GUID3*: Ersetzen Sie die ersten beiden Spalten der Zeile durch die Daten aus der Tabelle ModuleSignature. Wenn das aktuelle Modul OtherModule nicht ausschließt. *GUID3*, löschen Sie diese Zeile.

Das Mergemodul ICE sendet den vierten Fehler, da ein Modul nicht angeben kann, dass es sich selbst ausschließt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz zum Mergemodul](merge-module-ice-reference.md)
</dt> </dl>

 

 



