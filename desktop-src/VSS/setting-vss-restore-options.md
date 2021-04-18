---
description: Mit Wiederherstellungsoptionen können Anforderer angepasste Wiederherstellungsoptionen an Writer übermitteln.
ms.assetid: 364550a1-070a-4f7e-bd62-84672959dc21
title: Festlegen der VSS-Wiederherstellungsoptionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c814ffb94f25229e7f3e17f592c631f13b6717e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347105"
---
# <a name="setting-vss-restore-options"></a>Festlegen der VSS-Wiederherstellungsoptionen

Mit Wiederherstellungsoptionen können Anforderer angepasste Wiederherstellungsoptionen an Writer übermitteln.

## <a name="restore-options"></a>Wiederherstellungsoptionen

Durch die Standardisierung des Formats der Wiederherstellungsoptionen können Writer und Anforderer gängige benutzerdefinierte Anforderungen verarbeiten. Wiederherstellungsoptionen werden von der anfordernden Person festgelegt, indem die [**IVssBackupComponents:: setrestoreoptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) -Methode bis zu einmal pro ausgewählter Sicherungs Komponente aufgerufen wird, bevor die [**IVssBackupComponents::P**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) -Methode zum erneuten Ausführen aufgerufen wird. Die Zeichenfolge, die im *wszrestoreoptions* -Parameter an die Methode "* **trestoreoptions** " übergeben wird, kann mehrere Werte enthalten, wie unten beschrieben.

## <a name="format"></a>Format

Das Format der Wiederherstellungsoptionen ist ein oder mehrere durch Trennzeichen getrennte Name-Wert-Paare, und der Name wird optional mit dem Namen der Unterkomponente, für die er gilt, als Präfix vorangestellt. Bei Komponentennamen und Optionsnamen wird die Groß-/Kleinschreibung nicht beachtet. Die Groß-/Kleinschreibung der Werte wird vom Writer festgelegt. Beispiel:

``` syntax
"Child1":"Option1"="Value1","Option2"="Value2","Child2\Grandchild3":"Option3"="Value3"
```

In diesem Beispiel gilt "Option1" nur für die Unterkomponente "child1" und deren Nachfolger, "option2" gilt für alle Komponenten und deren Nachfolger, und "Option3" gilt nur für die \\ unter Komponenten "child2 Grandchild3" und deren Nachfolger.

Die Methode "* [**trestoreoptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) " kann nur für Komponenten aufgerufen werden, die für die Sicherung ausgewählt werden können, während Nachfolger Knoten möglicherweise nicht für die Sicherung auswählbar sind. Sie können für die Wiederherstellung ausgewählt werden.

## <a name="common-restore-options"></a>Allgemeine Wiederherstellungsoptionen

Diese allgemeinen Wiederherstellungsoptionen wurden definiert, um die Interoperabilität zwischen Writern und Anforderern zu erhöhen.

-   Tärer

    Die "autoritative"-Option unterstützt mehrere "Item"-Werte, aber nur einen "All"-Wert.

    Diese gesamte Komponente ist autoritativ.

    ``` syntax
    "Authoritative"="All"
    ```

    Nur das angegebene Element ist autoritativ. Das Format des benannten Elements wird vom Writer definiert. Allgemeine Bezeichnungen sind " \* ", um alle Dateien anzugeben, "..." , um alle Dateien und Unterverzeichnisse der angegebenen Komponente anzugeben.

    ``` syntax
    "Authoritative"="Item:XXX"
    ```

-   Roll Forward

    Nachdem eine Datenbank wieder hergestellt wurde, führen Schreiber in der Regel einen Rollup durch Protokolle durch, um die Datenbank auf den neuesten Stand zu bringen Bei inkrementellen oder differenziellen Wiederherstellungen verwendet der Anforderer die [**IVssBackupComponents:: setadditionalrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) -Methode, um das Verhalten der Protokoll Behandlung teilweise zu steuern. diese Wiederherstellungsoption ermöglicht eine präzisetere Steuerung.

    Führen Sie kein Roll Through für Protokolle durch.

    ``` syntax
    "Roll Forward"="None"
    ```

    Durchlaufen Sie alle Protokolle.

    ``` syntax
    "Roll Forward"="All"
    ```

    Rollover der Protokolle bis zum angegebenen Punkt. Das Format des angegebenen Punkts wird vom Writer definiert.

    ``` syntax
    "Roll Forward"="Partial:XXX"
    ```

-   Name der neuen Komponente

    Ein Writer möchte möglicherweise eine Komponente in einem neuen Namen wiederherstellen. Beispielsweise die Wiederherstellung einer Datenbank unter einem anderen Namen, um ein einzelnes Element wiederherzustellen. Wenn Sie denselben Namen wiederherstellen, werden alle Daten, die wir empfehlen, dass Writer einen gültigen logischen Pfad und Komponentennamen als Wert dieser Optionen akzeptieren. Dies wird häufig mit einem [*gerichteten Ziel*](vssgloss-d.md)verwendet.

    ``` syntax
    "New Component Name"="Logical Path\Component Name"
    ```

 

 



