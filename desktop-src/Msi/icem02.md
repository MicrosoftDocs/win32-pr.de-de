---
description: ICEM02 überprüft, ob alle Modul Abhängigkeiten und-Ausschlüsse mit dem aktuellen Modul verknüpft sind.
ms.assetid: c7d77cb6-0ee6-4857-a749-7908e1c5fcda
title: ICEM02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9a976132dbfad42e95f4141bc00adb48a544c1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214954"
---
# <a name="icem02"></a>ICEM02

ICEM02 überprüft, ob alle Modul Abhängigkeiten und-Ausschlüsse mit dem aktuellen Modul verknüpft sind.

Das Mergemodul "ICES" wird in der Datei "Merge Module. Cub" mit dem Namen "Mergemod. Cub" und nicht in der CUB-Datei gespeichert, die die für die Paketüberprüfung verwendeten Verb

## <a name="result"></a>Ergebnis

ICEM02 sendet Fehlermeldungen, wenn die Modul Datenbank versucht, Abhängigkeiten oder Ausschlüsse anzugeben, die nicht mit dem aktuellen Modul in Beziehung stehen. ICEM02 gibt eine Fehlermeldung aus, wenn die Modul Datenbank versucht, das aktuelle Modul als abhängig oder als von sich selbst ausgeschlossen festzulegen.

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

[ModuleSignature-Tabelle](modulesignature-table.md)



| ModuleID         | Sprache | Version |
|------------------|----------|---------|
| MyModule. *Guid1* | 1033     | 1.0     |



 

[Moduledepenptabelle](moduledependency-table.md)



| ModuleID            | Modulelanguage | Requirements did          | Requirements-Sprache | RequiredVersion |
|---------------------|----------------|---------------------|------------------|-----------------|
| Othermodule. *GUID2* | 1033           | Othermodule. *GUID3* | 0                | 1.0             |
| MyModule. *Guid1*    | 1033           | MyModule. *Guid1*    | 1033             | 1.2             |



 

[Moduleausschluss-Tabelle](moduleexclusion-table.md) (partiell)



| ModuleID            | Modulelanguage | Excludädid          | Excludecodlanguage |
|---------------------|----------------|---------------------|------------------|
| Othermodule. *GUID2* | 1033           | Othermodule. *GUID3* | 0                |
| MyModule. *Guid1*    | 1033           | MyModule. *Guid1*    | 1033             |



 

Das Mergemodul Ice postet den ersten Fehler, da der der ersten Zeile in der Tabelle "moduledepend", die keine erforderliche Abhängigkeit für das aktuelle Modul angibt, das in der Tabelle "ModuleSignature" angegeben ist. Die Abhängigkeiten eines Moduls können nur in einer eigenen moduledependen-Tabelle angegeben werden. Wenn othermodule. *GUID3* ist für das aktuelle Modul erforderlich. ersetzen Sie die ersten beiden Spalten der Zeile durch die Daten aus der ModuleSignature-Tabelle. Wenn othermodule. *GUID3* ist für dieses Modul nicht erforderlich, löschen Sie diese Zeile.

Das Mergemodul Ice postet den zweiten Fehler, da ein Modul keine Abhängigkeit von sich selbst angeben kann.

Das Mergemodul Ice postet den dritten Fehler aufgrund der ersten Zeile in der Tabelle "moduleausschluss", die keinen erforderlichen Ausschluss für das aktuelle Modul angibt, das in der ModuleSignature-Tabelle angegeben ist. Die Ausschlüsse eines Moduls können nur in einer eigenen moduleausschluss-Tabelle angegeben werden. , Wenn das aktuelle Modul othermodule ausschließt. *GUID3* ersetzen Sie die ersten beiden Spalten der Zeile durch die Daten aus der ModuleSignature-Tabelle. , Wenn das aktuelle Modul nicht othermodule ausschließt. *GUID3* löschen Sie diese Zeile.

Das Mergemodul Ice postet den vierten Fehler, da ein Modul nicht angeben kann, dass es sich selbst ausschließt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eisverweis für Mergemodul](merge-module-ice-reference.md)
</dt> </dl>

 

 



