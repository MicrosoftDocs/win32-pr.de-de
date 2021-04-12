---
description: ICE69 prüft, ob alle Teil Zeichenfolgen der Form, die \[ \] innerhalb einer formatierten Zeichenfolge $componentkey, keine Querverweis Komponenten sind.
ms.assetid: 6ab8f3b7-19e9-46f3-b09e-36bdb43d6f55
title: ICE69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95bd00efc6b141bfa872470adcc9e88a63a2c52d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217654"
---
# <a name="ice69"></a>ICE69

ICE69 prüft, ob alle Teil Zeichenfolgen der Form, die \[ \] innerhalb einer [formatierten](formatted.md) Zeichenfolge $componentkey, keine Querverweis Komponenten sind. Ein Komponenten übergreifender Verweis tritt \[ auf, wenn die $componentkey- \] Eigenschaft einer formatierten Zeichenfolge auf eine andere Komponente als die in der Komponenten \_ Spalte der Tabellen gespeicherte Komponente verweist.

Probleme mit der Komponenten übergreifenden Referenzierung ergeben sich aus der Art und Weise, wie [formatierte](formatted.md) Zeichen folgen ausgewertet werden. Wenn die Komponente, auf die mit der \[ $componentkey \] -Eigenschaft verwiesen wird, bereits installiert ist und während der aktuellen Installation nicht geändert wird (z. b. Wenn Sie neu installiert, in die Quelle verschoben wird usw.), wird der Ausdruck \[ $componentkey \] NULL ausgewertet, da der Aktionszustand der Komponente in \[ $componentkey \] NULL ist. Ähnliche Probleme können während des Aktualisierungs-und Reparatur Vorgangs auftreten.

## <a name="result"></a>Ergebnis

ICE69 gibt einen Fehler zurück, wenn eine \[ $componentkey \] Teil Zeichenfolge innerhalb einer [formatierten](formatted.md) Zeichenfolge Querverweise auf eine Komponente eines anderen Features durchführt. ICE69 gibt eine Warnung zurück, wenn eine \[ $componentkey \] Teil Zeichenfolge innerhalb einer formatierten Zeichenfolge Querverweise auf eine Komponente in derselben Funktion durchführt. (Die Tabelle " [FeatureComponents](featurecomponents-table.md) " wird verwendet, um diese Zuordnung zu bestimmen. Es muss der gleichen Funktion für die Warnung zugeordnet werden. Verweise auf Komponenten in übergeordneten Funktionen oder Verweise auf Komponenten in untergeordneten Funktionen werden als Fehler betrachtet.)

ICE69 meldet einen Fehler, wenn die \[ \# \] Teil Zeichenfolge von filekey innerhalb einer [formatierten](formatted.md) Zeichenfolge auf eine Datei verweist, die nicht in der [Datei](file-table.md) Tabelle als zur selben Komponente gehörend angegeben ist.

## <a name="example"></a>Beispiel

ICE69 meldet Folgendes für die gezeigten Beispiele.

``` syntax
WARNING: "Mismatched component reference. Entry 'Test' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test'. Components are in the same feature."
ERROR: "Mismatched component reference. Entry 'Shortcut2' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test2'. Components are not in the same feature."
```

Um diesen Fehler zu beheben, führen Sie keine Querverweise für Komponenten aus. Ändern \[ Sie die $componentkey so, dass \] Sie der Komponente der Verknüpfung entspricht.

Verknüpfungs [Tabelle](shortcut-table.md) (partiell)



| Abkürzung  | Komponente\_ | Argument     |
|-----------|-------------|--------------|
| Test      | QuickTest   | -v \[ $Test\] |
| Shortcut2 | QuickTest   | \[$Test 2\]   |



 

Die [Verb](verb-table.md) -und [Erweiterungs](extension-table.md) Tabellen sind Sonderfälle, in denen die Verb-Tabelle auf eine Erweiterung verweist, die zu einer Komponente gehört. Eine Erweiterung kann jedoch mehreren Komponenten angehören, da der Primärschlüssel für die Erweiterungs Tabelle aus der Erweiterung und den Komponenten \_ Spalten besteht. Sie können logisch folgende Situation haben:

[Verb Tabelle](verb-table.md) (partiell)



| Durchwahl | Verb\_ | Argument                |
|-----------|--------|-------------------------|
| TST       | open   | -v \[ $COMP 1 \] \[ $COMP 2\] |



 

[Erweiterungs Tabelle](extension-table.md) (partiell)



| Durchwahl | Komponente\_ |
|-----------|-------------|
| TST       | comp1       |
| TST       | comp2       |



 

[FeatureComponents-Tabelle](featurecomponents-table.md)



| Funktion\_ | Komponente\_ |
|-----------|-------------|
| Feature1  | QuickTest   |
| Feature1  | Test        |
| Feature2  | Test2       |



 

In diesem Fall müssen Sie sicherstellen, dass mindestens eine der \[ $componentkey \] Eigenschaften einen nicht-NULL-Wert ergibt. Jede \[ $componentkey \] Eigenschaft in der Argument-Spalte der Verb-Tabelle ( \[ $COMP 1 \] und \[ $COMP 2 \] im obigen Beispiel) muss jedoch auf eine mögliche Komponente verweisen, die in der dem Verb zugeordneten Erweiterung enthalten ist. Ein Verweis wie \[ $Comp 3 \] würde zu einer Warnung aus ICE69 führen.

Die [AppID-Tabelle](appid-table.md) hat eine ähnliche Situation wie die Verb Tabelle. Die [Klassen Tabelle](class-table.md) wird als Komponenten Verweis verwendet. In diesem Fall wird die AppID-Tabelle auf die gleiche Weise überprüft wie die Verb-Extension Validierung (jetzt AppID-Class).

Die Argument-Spalte der Klassen Tabelle wird wie die [Verknüpfung](shortcut-table.md), die [Registrierung](registry-table.md)und ähnliche Tabellen überprüft.

## <a name="table-used-during-execution-only-if-found"></a>Während der Ausführung verwendete Tabelle (nur, wenn Sie gefunden wurde)

[INIFILE](inifile-table.md)

[Removeinifile](removeinifile-table.md)

[Registrierung](registry-table.md)

[Removeregistry](removeregistry-table.md)

[ServiceControl](servicecontrol-table.md)

[Serviceingestall](serviceinstall-table.md)

[Tastenkombination](shortcut-table.md)

[Verb](verb-table.md)

[Erweiterung](extension-table.md)

[Klasse](class-table.md)

[AppId](appid-table.md)

[Umgebung](environment-table.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



