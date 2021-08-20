---
description: Mit Wiederherstellungsoptionen können Anfordernde angepasste Wiederherstellungsoptionen an Writer übermitteln.
ms.assetid: 364550a1-070a-4f7e-bd62-84672959dc21
title: Festlegen von VSS-Wiederherstellungsoptionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58f3ca56a516148bcc11a12fc72aaa6941b0436236525c06c63142107bd18b59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121995"
---
# <a name="setting-vss-restore-options"></a>Festlegen von VSS-Wiederherstellungsoptionen

Mit Wiederherstellungsoptionen können Anfordernde angepasste Wiederherstellungsoptionen an Writer übermitteln.

## <a name="restore-options"></a>Wiederherstellungsoptionen

Durch das Standardisieren des Formats der Wiederherstellungsoptionen können Writer und Anfordernde allgemeine benutzerdefinierte Anforderungen verarbeiten. Wiederherstellungsoptionen werden vom Anfordernden festgelegt, indem die [**IVssBackupComponents::SetRestoreOptions-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) bis zu einmal pro ausgewählter Sicherungskomponente vor dem Aufruf der [**IVssBackupComponents::P reRestore-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) aufruft. Die im *wszRestoreOptions-Parameter* an die **SetRestoreOptions-Methode** übergebene Zeichenfolge kann mehrere Werte enthalten, wie unten beschrieben.

## <a name="format"></a>Format

Das Format der Wiederherstellungsoptionen ist mindestens ein durch Komma getrenntes Name/Wert-Paar, und dem Namen wird optional der Name der Unterkomponenten vorangestellt, für die er gilt. Bei den Komponentennamen und Optionsnamen wird die Groß-/Kleinschreibung nicht beachtet. Die Sensitivität der Werte wird vom Writer bestimmt. Beispiel:

``` syntax
"Child1":"Option1"="Value1","Option2"="Value2","Child2\Grandchild3":"Option3"="Value3"
```

In diesem Beispiel gilt "Option1" nur für die Unterkomponenten "Child1" und deren Nachfolger, "Option2" für alle Komponenten und deren Nachfolger, und "Option3" gilt nur für die Unterkomponenten "Child2 \\ Grandchild3" und deren Nachfolger.

Die [**SetRestoreOptions-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) kann nur für Komponenten aufgerufen werden, die für die Sicherung ausgewählt werden können, während nachfolgende Knoten möglicherweise nicht für die Sicherung ausgewählt werden können. Sie können jedoch für die Wiederherstellung ausgewählt werden.

## <a name="common-restore-options"></a>Allgemeine Wiederherstellungsoptionen

Diese allgemeinen Wiederherstellungsoptionen wurden definiert, um die Interoperabilität zwischen Writern und Anfordernden zu erhöhen.

-   Autoritativ

    Die Option "Autoritativ" unterstützt mehrere "Item"-Werte, aber nur einen "All"-Wert.

    Diese gesamte Komponente ist autoritativ.

    ``` syntax
    "Authoritative"="All"
    ```

    Nur das angegebene Element ist autoritativ. Das Format des benannten Elements wird vom Writer definiert. Allgemeine Bezeichnungen sind " \* " , um alle Dateien anzugeben, "..." , um alle Dateien und Unterverzeichnisse der angegebenen Komponente anzugeben.

    ``` syntax
    "Authoritative"="Item:XXX"
    ```

-   Roll Forward

    Nach der Wiederherstellung einer Datenbank führen Writer normalerweise einen Roll forward durch Protokolle durch, um die Datenbank auf den neuesten Stand zu bringen. Bei inkrementellen oder differenziellen Wiederherstellungen verwendet der Anfordernde die [**IVssBackupComponents::SetAdditionalRestores-Methode,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) um das Protokollbehandlungsverhalten teilweise zu steuern. Diese Wiederherstellungsoption ermöglicht eine präzisere Steuerung.

    Roll through logs (Protokolle nicht durchrollen).

    ``` syntax
    "Roll Forward"="None"
    ```

    Roll through all logs (Alle Protokolle werden durchrollt).

    ``` syntax
    "Roll Forward"="All"
    ```

    Roll through logs up to specified point (Protokolle bis zum angegebenen Punkt durchrollen). Das Format des angegebenen Punkts wird vom Writer definiert.

    ``` syntax
    "Roll Forward"="Partial:XXX"
    ```

-   Name der neuen Komponente

    Ein Writer möchte eine Komponente möglicherweise auf einen neuen Namen wiederherstellen. Beispielsweise das Wiederherstellen einer Datenbank unter einem anderen Namen, um ein einzelnes Element wiederherzustellen. Wiederherstellung unter demselben Namen würde alle Daten enthalten. Es wird empfohlen, dass Writer einen gültigen logischen Pfad und Komponentennamen als Wert dieser Optionen akzeptieren. Dies wird häufig mit einem gerichteten [*Ziel verwendet.*](vssgloss-d.md)

    ``` syntax
    "New Component Name"="Logical Path\Component Name"
    ```

 

 



