---
description: ICE69 überprüft, ob alle Teilzeichenfolgen des Formulars $componentkey formatierten Zeichenfolgen keine \[ \] Querverweise auf Komponenten enthalten.
ms.assetid: 6ab8f3b7-19e9-46f3-b09e-36bdb43d6f55
title: ICE69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 183a62989ff39387639af1a9e1feeeddc3e0567f28915ca3857ba6dd5f58f68c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043940"
---
# <a name="ice69"></a>ICE69

ICE69 überprüft, ob alle Teilzeichenfolgen des Formulars $componentkey formatierten Zeichenfolgen keine \[ \] Querverweiskomponenten [](formatted.md) enthalten. Ein komponentenübergreifender Verweis tritt auf, wenn die $componentkey-Eigenschaft einer formatierten Zeichenfolge auf eine andere Komponente verweist als die Komponente, die in der Spalte Komponente ihrer Tabellen \[ \] gespeichert \_ ist.

Probleme mit komponentenübergreifenden Verweisen treten auf, wenn [formatierte Zeichenfolgen](formatted.md) ausgewertet werden. Wenn die Komponente, auf die mit der $componentkey-Eigenschaft verwiesen wird, bereits installiert ist und während der aktuellen Installation nicht geändert wird (z. B. neu installiert, in die Quelle verschoben usw.), wird der Ausdruck $componentkey als NULL ausgewertet, da der Aktionszustand der Komponente \[ \] in $componentkey NULL \[ \] \[ \] ist. Ähnliche Probleme können bei Upgrade- und Reparaturvorgängen auftreten.

## <a name="result"></a>Ergebnis

ICE69 gibt einen Fehler zurück, wenn $componentkey teilzeichenfolge innerhalb einer formatierten Zeichenfolge quer auf eine Komponente in einem \[ \] anderen Feature verweist. [](formatted.md) ICE69 gibt eine Warnung zurück, wenn $componentkey teilzeichenfolge innerhalb einer formatierten Zeichenfolge querverweist auf eine Komponente \[ \] im gleichen Feature. (Die [Tabelle FeatureComponents](featurecomponents-table.md) wird verwendet, um diese Zuordnung zu bestimmen. Sie muss demselben Feature für die Warnung zuordnen. Das Verweisen auf Komponenten in übergeordneten Features oder das Verweisen auf Komponenten in untergeordneten Features wird als Fehler betrachtet.)

ICE69 meldet einen Fehler, wenn die FileKey-Teilzeichenfolge innerhalb einer formatierten Zeichenfolge auf eine Datei verweist, die in der Tabelle File nicht als zur gleichen Komponente \[ \# \] gehörend angegeben ist. [](formatted.md) [](file-table.md)

## <a name="example"></a>Beispiel

ICE69 meldet für die gezeigten Beispiele Folgendes.

``` syntax
WARNING: "Mismatched component reference. Entry 'Test' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test'. Components are in the same feature."
ERROR: "Mismatched component reference. Entry 'Shortcut2' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test2'. Components are not in the same feature."
```

Um diesen Fehler zu beheben, verweisen Sie nicht auf Komponenten. Ändern Sie \[ die \] $componentkey, damit sie mit der Komponente der Verknüpfung übereinstimmen.

[Verknüpfungstabelle](shortcut-table.md) (partiell)



| Verknüpfung  | Komponente\_ | Argument     |
|-----------|-------------|--------------|
| Test      | Quicktest   | -v \[ $Test\] |
| Shortcut2 | Quicktest   | \[$Test 2\]   |



 

Die [Verb-](verb-table.md) [und Erweiterungstabellen](extension-table.md) sind Sonderfälle, in denen die Verbtabelle auf eine Erweiterung verweist, die zu einer Komponente gehört. Eine Erweiterung kann jedoch zu mehreren Komponenten gehören, da der Primärschlüssel für die Erweiterungstabelle aus den Spalten Erweiterung und Komponente \_ besteht. Die folgende Situation kann logisch sein.

[Verbtabelle](verb-table.md) (partiell)



| Durchwahl | Verb\_ | Argument                |
|-----------|--------|-------------------------|
| Tst       | öffnen   | -v \[ $comp 1 \] \[ $comp 2\] |



 

[Erweiterungstabelle](extension-table.md) (partiell)



| Durchwahl | Komponente\_ |
|-----------|-------------|
| Tst       | comp1       |
| Tst       | comp2       |



 

[FeatureComponents-Tabelle](featurecomponents-table.md)



| Komponente\_ | Komponente\_ |
|-----------|-------------|
| Feature1  | Quicktest   |
| Feature1  | Test        |
| Feature2  | Test2       |



 

In diesem Fall müssen Sie sicherstellen, dass mindestens eine der $componentkey-Eigenschaften zu einem Wert ausgewertet wird, der \[ \] nicht NULL ist. Allerdings muss jede $componentkey-Eigenschaft in der Argument -Spalte der \[ \] Verbtabelle ( \[ $comp 1 und \] \[ $comp 2 im obigen \] Beispiel) auf eine mögliche Komponente verweisen, die in der erweiterung enthalten ist, die dem Verb zugeordnet ist. Ein Verweis wie \[ $comp 3 \] würde zu einer Warnung von ICE69 führen.

Die [AppId-Tabelle](appid-table.md) hat eine ähnliche Situation wie die Verb-Tabelle. Für den [Komponentenverweis wird die Tabelle Class](class-table.md) verwendet. In diesem Fall wird die AppId-Tabelle auf die gleiche Weise wie die Verb-Extension (jetzt AppId-Class) überprüft.

Die Argument -Spalte der Klassentabelle wird wie die [Tabellen Shortcut,](shortcut-table.md) [Registry](registry-table.md)und ähnliche überprüft.

## <a name="table-used-during-execution-only-if-found"></a>Während der Ausführung verwendete Tabelle (nur bei Gefunden)

[IniFile](inifile-table.md)

[RemoveIniFile](removeinifile-table.md)

[Registrierung](registry-table.md)

[RemoveRegistry](removeregistry-table.md)

[ServiceControl](servicecontrol-table.md)

[ServiceInstall](serviceinstall-table.md)

[Tastenkombination](shortcut-table.md)

[Verb](verb-table.md)

[Erweiterung](extension-table.md)

[Klasse](class-table.md)

[AppId](appid-table.md)

[Umgebung](environment-table.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



