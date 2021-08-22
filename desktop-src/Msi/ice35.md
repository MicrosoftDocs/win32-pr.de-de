---
description: ICE35 überprüft, ob Komponenten, die komprimierte Dateien enthalten, die in einer Schränkdatei gespeichert sind, nicht für die Ausführung aus der Quelle festgelegt sind. Mit Windows Installer 2.0 oder höher wurde diese Einschränkung entfernt.
ms.assetid: b4df27e2-9790-4b18-a173-25fa8b0ecd4d
title: ICE35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4ee42f97a049b165d41fef7391f0031836865dbf7bafec6b1b5e2fb868e75a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528560"
---
# <a name="ice35"></a>ICE35

ICE35 überprüft, ob Komponenten, die [](cabinet-files.md) komprimierte Dateien enthalten, die in einer Schränkdatei gespeichert sind, nicht für die Ausführung aus der Quelle festgelegt sind. Mit Windows Installer 2.0 oder höher wurde diese Einschränkung entfernt.

ICE35 fragt die Spalte "Cabinet" der [Media-Tabelle](media-table.md) ab, um zu bestimmen, welche Dateien komprimiert und in einer Schränkdatei gespeichert werden. Die Dateitabelle wird [abgefragt,](file-table.md) um zu bestimmen, welche Komponenten diese Dateien enthalten. Schließlich wird die [Component-Tabelle überprüft,](component-table.md) um zu bestimmen, ob die Run-from-Source-Bits in der Spalte Attribute festgelegt sind.

## <a name="result"></a>Ergebnis

ICE35 gibt eine Fehlermeldung aus, wenn eine komprimierte Datei in einer Schränkdatei gespeichert ist, die zu einer Komponente gehört, bei der das Bit msidbComponentAttributesSourceOnly in der Spalte Attribute der Component-Tabelle festgelegt [ist.](component-table.md) Mit Windows Installer 2.0 oder höher wird dies von einem Fehler in eine Warnmeldung geändert. Für ein Paket, das nur Windows Installer 2.0 und höher unterstützt, ist die EIGENSCHAFT PID PAGECOUNT des Zusammenfassungsinformationsstreams auf mindestens \_ 200 festgelegt.

ICE35 gibt eine Warnmeldung aus, wenn eine komprimierte Datei in einer Schränkdatei gespeichert ist, die zu einer Komponente gehört, bei der das bit msidbComponentAttributesOptional in der Spalte Attribute der Component-Tabelle festgelegt [ist.](component-table.md) Diese Warnmeldung wurde mit installationsprogramm Windows 2.0 und höher entfernt.

Wenn sich mehrere Dateien in einer Komponente in einer Schränkdatei befinden, meldet ICE35 Fehler für jede Datei, für die die Ausführung vom Quellbit festgelegt ist.

## <a name="example"></a>Beispiel

ICE35 meldet die folgenden Fehler und Warnungen für das Beispiel, das mit einer früheren Version als Windows Installer Version 2.0 angezeigt wird.



| ICE35-Fehler                                                                                                | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FEHLER: Komponente 3 kann nicht nur aus Quelle ausgeführt werden, da die Memberdatei "File3" komprimiert ist. | Es ist eine komprimierte Datei in einer Cabinet-Datei gespeichert, und diese Datei gehört zu einer Komponente, bei der das SourceOnly-Bit in der Spalte Attribute der [Component-Tabelle festgelegt ist.](component-table.md) Um diesen Fehler zu beheben, ändern Sie die unteren 2 Bits des Attributwerts von Component2 in "00", d. h. nur Lokal, oder entfernen Sie File4 aus der CAB-Datei.<br/>                                                                                                                                                                         |
| FEHLER: Komponente 3 kann nicht nur aus Quelle ausgeführt werden, da die Memberdatei "File3" komprimiert ist. | Es ist eine komprimierte Datei in einer Cabinet-Datei gespeichert, und diese Datei gehört zu einer Komponente, bei der das SourceOnly-Bit in der Spalte Attribute der [Component-Tabelle festgelegt ist.](component-table.md) Da die Dateien in einer Komponente nicht alle von denselben Medien stammen müssen, meldet ICE35 Fehler für jede Datei in der Komponente, die sich in einem Schränk befindet.<br/> Um diesen Fehler zu beheben, ändern Sie die unteren 2 Bits des Attributwerts von Component2 in "00", d. h. nur Lokal, oder entfernen Sie File4 aus der CAB-Datei.<br/> |



 

[Medientabelle](media-table.md) (partiell)



| DiskID | LastSequence | Kabinett   |
|--------|--------------|-----------|
| 1      | 2            |           |
| 2      | 4            | One.cab   |
| 3      | 5            | \#Two.cab |



 

[Dateitabelle](file-table.md) (partiell)



| Datei  | Komponente\_ | Sequenz |
|-------|-------------|----------|
| Datei1 | Komponente1  | 1        |
| Datei2 | Component2  | 2        |
| Datei3 | Component2  | 3        |
| Datei4 | Component3  | 4        |
| Datei5 | Component3  | 5        |



 

[Komponententabelle](component-table.md) (partiell)



| Komponente  | Attribute |
|------------|------------|
| Komponente1 | 0          |
| Component2 | 2          |
| Component3 | 1          |



 

[Verknüpfungstabelle](shortcut-table.md) (partiell)



| Verknüpfung  | Symbol\_ |
|-----------|--------|
| Shortcut1 | Symbol2  |



 

Beachten Sie, dass Dateien auch mithilfe der Eigenschaft Zusammenfassung der Wortanzahl des Datenstroms Zusammenfassungsinformationen als [komprimiert markiert werden können.](summary-information-stream.md) [](word-count-summary.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 




