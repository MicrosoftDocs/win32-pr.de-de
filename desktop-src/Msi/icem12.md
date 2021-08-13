---
description: ICEM12 überprüft, ob standard-Aktionen in einer ModuleSequence-Tabelle Sequenznummern und benutzerdefinierte Aktionen BaseAction- und After-Werte aufweisen.
ms.assetid: 1a168629-9865-4412-8317-8af8b9a7b8bd
title: ICEM12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53e6f83b9ffccf6595719815ec4bd44cc8ff3774b989b682751dd9be1bbe5f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634943"
---
# <a name="icem12"></a>ICEM12

ICEM12 überprüft, ob standard-Aktionen in einer ModuleSequence-Tabelle Sequenznummern und benutzerdefinierte Aktionen BaseAction- und After-Werte aufweisen.

Dieser ICEM ist in der Mergemod.cub-Datei verfügbar, die im Windows Installer 2.0 SDK und höher bereitgestellt wird. Weitere Informationen finden Sie unter [Windows SDK-Komponenten für Windows Installer-Entwickler.](platform-sdk-components-for-windows-installer-developers.md)

## <a name="result"></a>Ergebnis

ICEM12 gibt in den folgenden Fällen einen Fehler aus:

-   Das Modul enthält eine [Standardaktion](standard-actions.md) ohne Sequenznummer.
-   Es wird festgestellt, dass eine Standardaktion Werte enthält, die in die Felder BaseAction oder After der [Tabelle ModuleAdminUISequence,](moduleadminuisequence-table.md) [der Tabelle ModuleAdminExecuteSequence,](moduleadminexecutesequence-table.md)der Tabelle [ModuleAdvtExecuteSequence,](moduleadvtexecutesequence-table.md)der [Tabelle ModuleInstallUISequence](moduleinstalluisequence-table.md)oder der [Tabelle ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md)eingegeben wurden.
-   Das Modul enthält eine [benutzerdefinierte Aktion,](custom-actions.md) ohne dass Werte in die Felder Sequence, BaseAction oder After der [Tabelle ModuleAdminUISequence,](moduleadminuisequence-table.md)der [Tabelle ModuleAdminExecuteSequence,](moduleadminexecutesequence-table.md)der [Tabelle ModuleAdvtExecuteSequence,](moduleadvtexecutesequence-table.md)der [Tabelle ModuleInstallUISequence](moduleinstalluisequence-table.md)oder der [Tabelle ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md)eingegeben wurden.

ICEM12 gibt eine Warnung aus, wenn eine benutzerdefinierte Aktion gefunden wird, für die eine Sequenznummer angegeben ist, aber kein Wert in den Feldern BaseAction oder After vorhanden ist.

Beachten Sie, dass alle In der [Tabelle CustomAction](customaction-table.md) gefundenen Aktionen als benutzerdefinierte Aktionen betrachtet werden. Alle anderen Aktionen werden als Standardaktionen betrachtet.

## <a name="example"></a>Beispiel

ICEM12 sendet die folgenden Fehler- und Warnmeldungen für ein Modul, das die unten gezeigten Datenbankeinträge enthält:

``` syntax
Error. Custom actions should use the BaseAction and After fields and not use the 
Sequence field in the Module Sequence tables. The custom action 'Action1' uses the Sequence field 
and does not use the BaseAction and After fields in the ModuleInstallExecuteSequence table. 
    
Error. Custom actions should not leave the Sequence, BaseAction, and After fields 
of the Module Sequence tables all empty. The custom action 'Action3' leaves the Sequence, 
BaseAction, and After fields empty in the ModuleAdminExecuteSequence table.

Error. Standard actions should not use the BaseAction and After fields in Module 
Sequence tables. The standard action 'Action2' has a values entered in the BaseAction 
or After fields of the ModuleAdminExecuteSequence table.

Error. Standard actions must have a entry in the Sequence field of Module Sequence 
tables. The standard action 'Action2' does not have a Sequence value in the 
ModuleExecuteSequence table.
```

[CustomAction](customaction-table.md)



| Aktion  | type | `Source`  | Ziel  |
|---------|------|---------|---------|
| Action1 | 30   | source1 | target1 |
| Action3 | 30   | source3 | target3 |



 

[ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md)



| Aktion  | Sequenz | BaseAction | Danach | Bedingung |
|---------|----------|------------|-------|-----------|
| Action2 |          | Action1    | 1     | true      |
| Action3 |          |            |       | true      |



 

[ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md)



| Aktion  | Sequenz | BaseAction | Danach | Bedingung |
|---------|----------|------------|-------|-----------|
| Action1 | 1        |            |       | true      |



 

Versuchen Sie Folgendes, um diese Fehler zu beheben:

-   Entfernen Sie die Sequenznummer für die benutzerdefinierte Aktion Action1, und verwenden Sie stattdessen die Felder BaseAction und After.
-   Geben Sie Werte in die Felder Sequence, BaseAction oder After für die benutzerdefinierte Aktion Action3 ein. Lassen Sie die Felder BaseAction und After für die Standardaktion Action2 leer.
-   Lassen Sie das Feld Sequenz für die Standardaktion Action2 nicht leer.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz zum Mergemodul](merge-module-ice-reference.md)
</dt> </dl>

 

 



