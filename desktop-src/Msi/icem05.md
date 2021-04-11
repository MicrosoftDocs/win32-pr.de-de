---
description: ICEM05 überprüft, ob das Mergemodul den Komponenten im Modul ordnungsgemäß zugeordnet ist. Eine fehlerhafte Zuordnung einer Komponente zu einem Modul bewirkt, dass die Komponente fälschlicherweise der Zieldatenbank zugeordnet wird.
ms.assetid: 1bf4041e-b198-4897-8719-8505fd8180ec
title: ICEM05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e62ca481ef836c2675c381817fe2242e37384818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042148"
---
# <a name="icem05"></a>ICEM05

ICEM05 überprüft, ob das Mergemodul den Komponenten im Modul ordnungsgemäß zugeordnet ist. Eine fehlerhafte Zuordnung einer Komponente zu einem Modul bewirkt, dass die Komponente fälschlicherweise der Zieldatenbank zugeordnet wird.

Das Mergemodul "ICES" wird in der Datei "Merge Module. Cub" mit dem Namen "Mergemod. Cub" und nicht in der CUB-Datei gespeichert, die die für die Paketüberprüfung verwendeten Verb

## <a name="result"></a>Ergebnis

ICEM05 gibt einen Fehler aus, wenn die Modul Datenbank Komponenten und das Modul fälschlicherweise zuordnet.

## <a name="example"></a>Beispiel

ICEM05 gibt die folgenden Fehlermeldungen für ein Modul mit den unten gezeigten Datenbankeinträgen aus.

``` syntax
The component Component2.OtherModule.GUID2.1033 in the 
ModuleComponents table does not belong to this Merge Module.
The component Component1.MyModule.GUID1.1033 in the ModuleComponents 
table is not listed in the Component table.
The component 'Component3' in the Component table is not listed in the 
ModuleComponents table.
```

[ModuleSignature-Tabelle](modulesignature-table.md)



| ModuleID         | Sprache | Version |
|------------------|----------|---------|
| MyModule. *Guid1* | 1033     | 1.0     |



 

[**Modulecomponents-Tabelle**](modulecomponents-table.md)



| Komponente  | ModuleID            | Sprache |
|------------|---------------------|----------|
| Component1 | MyModule. *Guid1*    | 1033     |
| Component2 | Othermodule. *GUID2* | 1033     |



 

[Komponenten Tabelle](component-table.md) (partiell)



| Komponente  | ComponentID |
|------------|-------------|
| Component3 | *GUID4*     |
| Component2 | *GUID5*     |



 

Das Modul "Mergemodul" meldet den ersten Fehler, weil die modulecomponents-Tabelle versucht, eine Komponente einem anderen Modul zuzuordnen, das nicht das aktuelle Modul ist, das in der Tabelle "ModuleSignature" angegeben ist. Um dieses Problem zu beheben, ändern Sie die Spalten ModuleID und Sprache des Datensatzes modulecomponents für Component2 in den Wert für das aktuelle Modul MyModule. *Guid1*.

Das Modul "Mergemodul" gibt den zweiten Fehler an, da der erste Datensatz in der Tabelle "modulecomponents" versucht, dem Modul Component1 zuzuordnen. Diese Komponente ist nicht in der Komponenten Tabelle des Mergemoduls vorhanden. Ein Modul kann nur mit einer Komponente verknüpft werden, die im Modul vorhanden ist. Um dieses Problem zu beheben, entfernen Sie den Datensatz für die nicht vorhandene Komponente.

Das Modul "Mergemodul" meldet den dritten Fehler, da das Modul versucht, der Zieldatenbank Component3 hinzuzufügen. Diese Komponente wurde dem Modul in der Tabelle "modulecomponents" nicht zugeordnet. Fügen Sie der Tabelle modulecomponents einen Datensatz für Component3 hinzu, um diesen Fehler zu beheben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eisverweis für Mergemodul](merge-module-ice-reference.md)
</dt> </dl>

 

 



