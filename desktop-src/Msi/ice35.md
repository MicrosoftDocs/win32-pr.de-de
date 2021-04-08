---
description: ICE35 überprüft, ob Komponenten, die in einer CAB-Datei gespeicherte komprimierte Dateien enthalten, nicht aus der Quelle ausgeführt werden. Bei Windows Installer 2,0 oder höher wurde diese Einschränkung entfernt.
ms.assetid: b4df27e2-9790-4b18-a173-25fa8b0ecd4d
title: ICE35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea6a98079d3c57e0c796332cf0cd5f11045a07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960038"
---
# <a name="ice35"></a>ICE35

ICE35 überprüft, ob Komponenten, die in einer CAB- [Datei](cabinet-files.md) gespeicherte komprimierte Dateien enthalten, nicht aus der Quelle ausgeführt werden. Bei Windows Installer 2,0 oder höher wurde diese Einschränkung entfernt.

ICE35 fragt die CAB-Spalte der [Medien Tabelle](media-table.md) ab, um zu bestimmen, welche Dateien komprimiert und in einer CAB-Datei gespeichert werden. Die [Dateitabelle](file-table.md) wird abgefragt, um zu bestimmen, welche Komponenten diese Dateien enthalten. Zum Schluss überprüft er die [Komponenten Tabelle](component-table.md) , um zu bestimmen, ob die Bits aus der Quelle in der Spalte Attribute festgelegt sind.

## <a name="result"></a>Ergebnis

ICE35 gibt eine Fehlermeldung aus, wenn eine komprimierte Datei in einer CAB-Datei gespeichert ist, die zu einer Komponente gehört, in der das Bit msidbcomponentattributessourceonly in der Spalte Attribute der [Komponenten Tabelle](component-table.md)festgelegt ist. Bei Windows Installer 2,0 oder höher wird dies von einem Fehler in eine Warnmeldung geändert. Ein Paket, das nur Windows Installer 2,0 und höher unterstützt, verfügt über die PID- \_ Eigenschaft PageCount des Datenstroms für die Zusammenfassung, die auf einen Wert von mindestens 200 festgelegt ist.

ICE35 gibt eine Warnmeldung aus, wenn eine komprimierte Datei in einer CAB-Datei gespeichert ist, die zu einer Komponente gehört, in der die Spalte Attribute der [Komponenten Tabelle](component-table.md)in der Spalte Attribute festgelegt ist. Diese Warnmeldung wurde mit Windows Installer 2,0 und höher entfernt.

Wenn sich mehrere Dateien in einer-Komponente in einer CAB-Datei befinden, meldet ICE35 Fehler für jede Datei, für die das Run From Source-Bit festgelegt ist.

## <a name="example"></a>Beispiel

ICE35 meldet die folgenden Fehler und Warnungen für das Beispiel, das unter Verwendung einer früheren Version als Windows Installer Version 2,0 angezeigt wird.



| ICE35-Fehler                                                                                                | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fehler: die Komponente Component3 kann nicht nur aus der Quelle ausgeführt werden, da die zugehörige Mitglieds Datei "Datei3" komprimiert ist. | Es gibt eine komprimierte Datei, die in einer CAB-Datei gespeichert ist, und diese Datei gehört zu einer Komponente, in der das sourceOnly-Bit in der Spalte Attribute der [Komponenten Tabelle](component-table.md)festgelegt ist. Um diesen Fehler zu beheben, ändern Sie die unteren 2 Bits des Component2's Attribute-Werts in "00", d. h. nur lokal, oder entfernen Sie datei4 aus der CAB-Datei.<br/>                                                                                                                                                                         |
| Fehler: die Komponente Component3 kann nicht nur aus der Quelle ausgeführt werden, da die zugehörige Mitglieds Datei "Datei3" komprimiert ist. | Es gibt eine komprimierte Datei, die in einer CAB-Datei gespeichert ist, und diese Datei gehört zu einer Komponente, in der das sourceOnly-Bit in der Spalte Attribute der [Komponenten Tabelle](component-table.md)festgelegt ist. Da die Dateien in einer Komponente nicht alle aus denselben Medien stammen müssen, meldet ICE35 Fehler für jede Datei in der Komponente, die sich in einer CAB-Datei befindet.<br/> Um diesen Fehler zu beheben, ändern Sie die unteren 2 Bits des Component2's Attribute-Werts in "00", d. h. nur lokal, oder entfernen Sie datei4 aus der CAB-Datei.<br/> |



 

[Medien Tabelle](media-table.md) (partiell)



| DiskID | LastSequence | KEs   |
|--------|--------------|-----------|
| 1      | 2            |           |
| 2      | 4            | One.cab   |
| 3      | 5            | \#Two.cab |



 

[Dateitabelle](file-table.md) (partiell)



| File  | Komponente\_ | Sequenz |
|-------|-------------|----------|
| Datei1 | Component1  | 1        |
| Datei2 | Component2  | 2        |
| Datei3 | Component2  | 3        |
| Datei4 | Component3  | 4        |
| Datei5 | Component3  | 5        |



 

[Komponenten Tabelle](component-table.md) (partiell)



| Komponente  | Attribute |
|------------|------------|
| Component1 | 0          |
| Component2 | 2          |
| Component3 | 1          |



 

Verknüpfungs [Tabelle](shortcut-table.md) (partiell)



| Abkürzung  | Symbol\_ |
|-----------|--------|
| Shortcut1 | Icon2  |



 

Beachten Sie, dass Dateien auch als komprimiert gekennzeichnet werden können, indem Sie die Eigenschaft " [**Zusammenfassung der Wort Zählung**](word-count-summary.md) " des [Zusammenfassungs Datenstroms](summary-information-stream.md)verwenden

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 




