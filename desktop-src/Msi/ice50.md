---
description: ICE50 überprüft, ob Verknüpfungssymbole angegeben sind, damit sie ordnungsgemäß angezeigt werden und mit der Erweiterung der Zieldatei übereinstimmen.
ms.assetid: 19288c87-fddb-46c9-8145-59e1b870a261
title: ICE50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b9dd81c84c52738ee58c023ba5727cd6d5766bf7c40db97b6459483d7f53d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635151"
---
# <a name="ice50"></a>ICE50

ICE50 überprüft, ob Verknüpfungssymbole angegeben sind, damit sie ordnungsgemäß angezeigt werden und mit der Erweiterung der Zieldatei übereinstimmen.

## <a name="result"></a>Ergebnis

ICE50 gibt eine Fehlermeldung aus, wenn die Erweiterung des Symbols und der Zieldateien nicht übereinstimmen. ICE50 gibt eine Warnung aus, wenn Symbole in Dateien gespeichert werden, die keine .exe oder ICO-Erweiterung haben.

## <a name="example"></a>Beispiel

ICE50 meldet den folgenden Fehler für das gezeigte Beispiel.



| ICE50-Fehler oder -Warnung                                                                                                              | Beschreibung                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Die Erweiterung des Symbols "Icon2.dat" für die Verknüpfung "Shortcut2" passt nicht zur Erweiterung der Schlüsseldatei für die Komponente "Component2". | Wenn die Erweiterungen des Symbols und der Zieldatei nicht übereinstimmen, hat die Verknüpfung nicht das richtige Kontextmenü, wenn die Komponente angekündigt wird. Um diesen Fehler zu beheben, benennen Sie das Symbol so um, dass es mit der Erweiterung der Zieldatei übereinstimmen soll.<br/> |
| Die Erweiterung des Symbols "Icon1.bat" für die Verknüpfung "Shortcut1" ist nicht "exe" oder "ico". Das Symbol wird nicht ordnungsgemäß angezeigt.         | Nicht in allen Versionen der Shell werden Symbole ordnungsgemäß angezeigt, die in Dateien gespeichert sind, die keine Erweiterungen von "exe" oder "ico" haben. Um diese Warnung zu beheben, benennen Sie das Symbol mit der Erweiterung "exe" oder "ico" um.<br/>                                      |



 

[Dateitabelle](file-table.md) (partiell)



| Datei  | FileName  |
|-------|-----------|
| Datei1 | File1.bat |
| Datei2 | File2.pl  |



 

[Featuretabelle](feature-table.md) (partiell)



| Komponente  |
|----------|
| Feature1 |



 

[Komponententabelle](component-table.md) (partiell)



| Komponente  | KeyPath |
|------------|---------|
| Komponente1 | Datei1   |
| Component2 | Datei2   |



 

[Symboltabelle](icon-table.md)



| Name      | Daten            |
|-----------|-----------------|
| Icon1.bat | \[Binärdaten\] |
| Icon2.dat | \[Binärdaten\] |



 

[Verknüpfungstabelle](shortcut-table.md) (partiell)



| Verknüpfung  | Komponente  | Ziel   | Symbol\_    |
|-----------|------------|----------|-----------|
| Shortcut1 | Komponente1 | Feature1 | Icon1.bat |
| Shortcut2 | Component2 | Feature1 | Icon2.dat |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 




