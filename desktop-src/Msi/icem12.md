---
description: ICEM12 überprüft, ob in einer modulesequence-Tabelle Standard Aktionen Sequenznummern aufweisen und benutzerdefinierte Aktionen baseaction-und After-Werte aufweisen.
ms.assetid: 1a168629-9865-4412-8317-8af8b9a7b8bd
title: ICEM12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b37cbff2e29a85dd50ef1f044a43fdb8e48ffdd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041870"
---
# <a name="icem12"></a>ICEM12

ICEM12 überprüft, ob in einer modulesequence-Tabelle Standard Aktionen Sequenznummern aufweisen und benutzerdefinierte Aktionen baseaction-und After-Werte aufweisen.

Dieses ICEM ist in der Datei "Mergemod. Cub" verfügbar, die im SDK für Windows Installer 2,0 und höher bereitgestellt wird. Weitere Informationen finden Sie unter [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md).

## <a name="result"></a>Ergebnis

ICEM12 gibt einen Fehler in den folgenden Fällen aus:

-   Es findet fest, dass das Modul eine [Standardaktion](standard-actions.md) ohne Sequenznummer enthält.
-   Es wird festgelegt, dass für eine Standardaktion Werte in den baseaction-oder After-Feldern der [moduleadminuisequence-Tabelle](moduleadminuisequence-table.md), [moduleadminexecutesequence-Tabelle](moduleadminexecutesequence-table.md), [moduleadvtexecutesequence](moduleadvtexecutesequence-table.md)-Tabelle, [moduleinstalluisequence](moduleinstalluisequence-table.md)-Tabelle oder [moduleinstallexecutesequence](moduleinstallexecutesequence-table.md)-Tabelle eingegeben werden.
-   Es findet das Modul, das eine [benutzerdefinierte Aktion](custom-actions.md) enthält, ohne dass Werte in die Reihenfolge, baseaction oder After-Felder der [moduleadminuisequence-Tabelle](moduleadminuisequence-table.md), [moduleadminexecutesequence](moduleadminexecutesequence-table.md)-Tabelle, [moduleadvtexecutesequence](moduleadvtexecutesequence-table.md)-Tabelle, [moduleinstalluisequence](moduleinstalluisequence-table.md)-Tabelle oder [moduleinstallexecutesequence](moduleinstallexecutesequence-table.md)-Tabelle

ICEM12 gibt eine Warnung aus, wenn eine benutzerdefinierte Aktion gefunden wird, für die eine Sequenznummer angegeben ist, in den Feldern baseaction oder After jedoch kein Wert.

Beachten Sie, dass alle in der [Tabelle CustomAction](customaction-table.md) gefundenen Aktionen als benutzerdefinierte Aktionen angesehen werden. Alle anderen Aktionen werden als Standard Aktionen behandelt.

## <a name="example"></a>Beispiel

ICEM12 veröffentlicht die folgenden Fehler-und Warnmeldungen für ein Modul, das die unten gezeigten Datenbankeinträge enthält:

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
| Action1 | 30   | Quelle1 | target1 |
| Action3 | 30   | source3 | target3 |



 

[Moduleadminexecutesequence](moduleadminexecutesequence-table.md)



| Aktion  | Sequenz | Baseaction | Nach | Bedingung |
|---------|----------|------------|-------|-----------|
| Action2 |          | Action1    | 1     | true      |
| Action3 |          |            |       | true      |



 

[Moduleinstallexecutesequence](moduleinstallexecutesequence-table.md)



| Aktion  | Sequenz | Baseaction | Nach | Bedingung |
|---------|----------|------------|-------|-----------|
| Action1 | 1        |            |       | true      |



 

Versuchen Sie Folgendes, um diese Fehler zu beheben:

-   Entfernen Sie die Sequenznummer für die benutzerdefinierte Aktion Action1, und verwenden Sie stattdessen die Felder baseaction und After.
-   Geben Sie Werte in die Felder Sequence, baseaction oder After für die benutzerdefinierte Aktion Action3 ein. Lassen Sie die Felder baseaction und After für Standardaktion Action2 leer.
-   Lassen Sie das Sequenz Feld für die Standardaktion Action2 nicht leer.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eisverweis für Mergemodul](merge-module-ice-reference.md)
</dt> </dl>

 

 



