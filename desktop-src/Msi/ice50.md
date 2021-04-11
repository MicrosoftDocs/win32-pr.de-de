---
description: ICE50 prüft, ob Verknüpfungs Symbole angegeben werden, damit Sie ordnungsgemäß angezeigt werden und der Erweiterung der Zieldatei entsprechen.
ms.assetid: 19288c87-fddb-46c9-8145-59e1b870a261
title: ICE50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de88dda0dd1cdd18a10a35c32ef612acb75c871e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960348"
---
# <a name="ice50"></a>ICE50

ICE50 prüft, ob Verknüpfungs Symbole angegeben werden, damit Sie ordnungsgemäß angezeigt werden und der Erweiterung der Zieldatei entsprechen.

## <a name="result"></a>Ergebnis

ICE50 gibt eine Fehlermeldung aus, wenn die Erweiterung der Symbol-und Zieldateien nicht entspricht. ICE50 gibt eine Warnung aus, wenn Symbole in Dateien gespeichert werden, die nicht über die Erweiterung ". exe" oder ". ico" verfügen.

## <a name="example"></a>Beispiel

ICE50 meldet den folgenden Fehler für das gezeigte Beispiel.



| ICE50-Fehler oder-Warnung                                                                                                              | BESCHREIBUNG                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Die Erweiterung des Symbols ' Icon2. dat ' für die Verknüpfung ' Shortcut2 ' stimmt nicht mit der Erweiterung der Schlüsseldatei für die Komponente ' Component2 ' identisch. | Wenn die Erweiterungen des Symbols und der Zieldatei nicht stimmen, verfügt die Verknüpfung nicht über das korrekte Kontextmenü, wenn die Komponente angekündigt wird. Benennen Sie das Symbol so um, dass es der Erweiterung der Zieldatei entspricht, um diesen Fehler zu beheben.<br/> |
| Die Erweiterung des Symbols ' Icon1.bat ' für die Verknüpfung ' Shortcut1 ' ist nicht ' exe ' oder ' ICO '. Das Symbol wird nicht ordnungsgemäß angezeigt.         | Nicht in allen Versionen der Shell werden Symbole korrekt angezeigt, die in Dateien gespeichert sind, die nicht über die Erweiterungen "exe" oder "ico" verfügen. Um diese Warnung zu beheben, benennen Sie das Symbol mit der Erweiterung "exe" oder "ico" um.<br/>                                      |



 

[Dateitabelle](file-table.md) (partiell)



| File  | FileName  |
|-------|-----------|
| Datei1 | File1.bat |
| Datei2 | File2.pl  |



 

[Funktions Tabelle](feature-table.md) (partiell)



| Funktion  |
|----------|
| Feature1 |



 

[Komponenten Tabelle](component-table.md) (partiell)



| Komponente  | KEYPATH |
|------------|---------|
| Component1 | Datei1   |
| Component2 | Datei2   |



 

[Symboltabelle](icon-table.md)



| Name      | Daten            |
|-----------|-----------------|
| Icon1.bat | \[Binärdaten\] |
| Icon2. dat | \[Binärdaten\] |



 

Verknüpfungs [Tabelle](shortcut-table.md) (partiell)



| Abkürzung  | Komponente  | Ziel   | Symbol\_    |
|-----------|------------|----------|-----------|
| Shortcut1 | Component1 | Feature1 | Icon1.bat |
| Shortcut2 | Component2 | Feature1 | Icon2. dat |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 




