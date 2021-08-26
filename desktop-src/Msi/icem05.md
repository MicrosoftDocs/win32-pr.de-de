---
description: ICEM05 überprüft, ob das Mergemodul den Komponenten im Modul ordnungsgemäß zugeordnet ist. Das falsche Zuordnen einer Komponente zu einem Modul führt dazu, dass die Komponente der Zieldatenbank falsch zugeordnet ist.
ms.assetid: 1bf4041e-b198-4897-8719-8505fd8180ec
title: ICEM05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee34dbc16b9cf3aeaa16aec9b5d62671cd51036c563bfb8561815ad3c21d0ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996780"
---
# <a name="icem05"></a>ICEM05

ICEM05 überprüft, ob das Mergemodul den Komponenten im Modul ordnungsgemäß zugeordnet ist. Das falsche Zuordnen einer Komponente zu einem Modul führt dazu, dass die Komponente der Zieldatenbank falsch zugeordnet ist.

Mergemodul-ICEs werden in einer Mergemodul-CUB-Datei namens Mergemod.cub und nicht in der CUB-Datei gespeichert, die die für die Paketvalidierung verwendeten ICEs enthält.

## <a name="result"></a>Ergebnis

ICEM05 gibt einen Fehler aus, wenn die Moduldatenbank Komponenten und das Modul falsch zuweist.

## <a name="example"></a>Beispiel

ICEM05 sendet die folgenden Fehlermeldungen für ein Modul, das die unten gezeigten Datenbankeinträge enthält.

``` syntax
The component Component2.OtherModule.GUID2.1033 in the 
ModuleComponents table does not belong to this Merge Module.
The component Component1.MyModule.GUID1.1033 in the ModuleComponents 
table is not listed in the Component table.
The component 'Component3' in the Component table is not listed in the 
ModuleComponents table.
```

[Tabelle "ModuleSignature"](modulesignature-table.md)



| ModuleID         | Sprache | Version |
|------------------|----------|---------|
| MyModule. *GUID1* | 1033     | 1.0     |



 

[**Tabelle "ModuleComponents"**](modulecomponents-table.md)



| Komponente  | ModuleID            | Sprache |
|------------|---------------------|----------|
| Component1 | MyModule. *GUID1*    | 1033     |
| Component2 | OtherModule. *GUID2* | 1033     |



 

[Komponententabelle](component-table.md) (teilweise)



| Komponente  | ComponentID |
|------------|-------------|
| Component3 | *GUID4*     |
| Component2 | *GUID5*     |



 

Das Mergemodul ICE meldet den ersten Fehler, da die Tabelle ModuleComponents versucht, eine Komponente einem anderen Modul zuzuordnen, das nicht das aktuelle Modul ist, das in der Tabelle ModuleSignature angegeben ist. Um dies zu beheben, ändern Sie die Spalten ModuleID und Language des ModuleComponents-Datensatzes für Component2 in die Spalten für das aktuelle Modul MyModule. *GUID1*.

Das Mergemodul ICE meldet den zweiten Fehler, da der erste Datensatz in der Tabelle ModuleComponents versucht, Component1 dem Modul zuzuordnen. Diese Komponente ist in der Komponententabelle des Mergemoduls nicht vorhanden. Ein Modul kann nur einer Komponente zugeordnet werden, die im Modul vorhanden ist. Um dies zu beheben, entfernen Sie den Datensatz für die nicht vorhandene Komponente.

Das Mergemodul ICE meldet den dritten Fehler, da das Modul versucht, Component3 zur Zieldatenbank hinzuzufügen. Diese Komponente wurde dem Modul in der Tabelle ModuleComponents nicht zugeordnet. Um diesen Fehler zu beheben, fügen Sie der Tabelle ModuleComponents einen Datensatz für Component3 hinzu.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz zum Mergemodul](merge-module-ice-reference.md)
</dt> </dl>

 

 



