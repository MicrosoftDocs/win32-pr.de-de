---
description: Ein Mergemodul kann auf eine MSI-Datei angewendet werden, um der Installation Verzeichnisse hinzuzufügen, aber es kann keine vorhandenen Verzeichnisse ersetzen oder entfernen.
ms.assetid: 5b808aa2-b2b2-4703-bd57-0b5e1e73b306
title: Erstellen von mergemodulverzeichnistabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98332f2c0bda10a5cc076f0ec80df3bf4b2e05aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864456"
---
# <a name="authoring-merge-module-directory-tables"></a>Erstellen von mergemodulverzeichnistabellen

Ein Mergemodul kann auf eine MSI-Datei angewendet werden, um der Installation Verzeichnisse hinzuzufügen, aber es kann keine vorhandenen Verzeichnisse ersetzen oder entfernen. Die [Verzeichnis Tabelle](directory-table.md) gibt das Layout der Verzeichnisse an, die das Mergemodul für die Ziel Installation bereitstellt. Eine Verzeichnis Tabelle ist in jedem Mergemodul erforderlich.

Beachten Sie beim Erstellen der Verzeichnis Tabelle in einem Mergemodul die folgenden Richtlinien. Weitere Informationen finden Sie unter [Verzeichnis Tabelle](directory-table.md) und [Verwenden der Verzeichnis Tabelle](using-the-directory-table.md).

-   Die vom Mergemodul hinzugefügte Verzeichnisstruktur muss über ein einzelnes Stammverzeichnis verfügen. Der Stamm muss den Namen "TARGETDIR" haben. Der Benutzer kann den Wert von TARGETDIR während der Zusammenführung ändern, um anzugeben, wo die Verzeichnisstruktur des Moduls an die Verzeichnisstruktur des Ziels angefügt werden soll.
-   Die Zusammenführung von Modul Tabellen außer der Verzeichnis Tabelle darf nicht direkt auf die Verzeichnis Speicherorte auf TARGETDIR verweisen. Der Speicherort eines solchen Verweises ändert sich, wenn der Wert von TARGETDIR vom Benutzer geändert wird.
-   Die Tabellen im Mergemodul müssen auf den Speicherort eines untergeordneten Verzeichnisses von TARGETDIR oder auf ein anderes Verzeichnis in der Struktur des Mergemoduls verweisen. Führen Sie die folgenden Schritte aus, um TARGETDIR als übergeordnetes Element eines Verzeichnisses im Mergemodul anzugeben. Geben Sie das Verzeichnis in die Spalte Verzeichnis ein, und geben Sie TARGETDIR in die übergeordnete Spalte des Verzeichnisses ein \_ . Verwenden Sie die Notation "." in der Spalte "DefaultDir", um anzugeben, dass sich dieses Verzeichnis in "TARGETDIR" ohne ein Unterverzeichnis befindet. Weitere Informationen finden Sie unter [Verwenden der Verzeichnis Tabelle](using-the-directory-table.md).
-   Die Namen der vom Mergemodul hinzugefügten Verzeichnisse müssen die Benennungs Konventionen verwenden, die unter [Benennen von primär Schlüsseln in mergemoduldatenbanken](naming-primary-keys-in-merge-module-databases.md)beschrieben werden. Dies schließt Verzeichnisse ein, die durch Eigenschaften wie die [**System Folder**](systemfolder.md) -Eigenschaft und die [**ProgramFilesFolder**](programfilesfolder.md) -Eigenschaft vordefiniert sind.
-   Fügen Sie einen [*GUID*](g-gly.md) an jeden Eintrag in der Verzeichnis Tabelle an (außer TargetDir). Dies schließt Verzeichnis Tabelleneinträge ein, die Windows Installer [**SystemFolder**](systemfolder.md) -Eigenschaften angeben, z. b. System Folder. 00000000 \_ 0000 0000 \_ \_ 0000 \_ 000000000000. Die Bibliothek Mergemod.dll fügt benutzerdefinierte Aktionen hinzu, um die **System Folder** -Eigenschaft festzulegen.
-   Wenn ein vordefiniertes Verzeichnis in einem Mergemodul enthalten ist, fügt das Merge-Tool der Zieldatenbank automatisch einen [benutzerdefinierten Aktionstyp 51](custom-action-type-51.md) hinzu. Der Autor des Merge-Moduls muss sicherstellen, dass auch eine [CustomAction-Tabelle](customaction-table.md) enthalten ist. Die Tabelle "CustomAction" ist möglicherweise leer, aber diese Tabelle muss in der Zieldatenbank vorhanden sein, und es wird sichergestellt, dass die geänderten vordefinierten Verzeichnisse an die richtigen Speicherorte geschrieben werden. Wenn ein System Verzeichnis z. b. in einem Mergemodul enthalten ist, muss der Autor des Merge-Moduls sicherstellen, dass eine benutzerdefinierte Aktionstabelle vorhanden ist.

    Beachten Sie, dass der übereinstimmende Algorithmus für die Generierung dieser benutzerdefinierten Aktionen vom Typ 51 nur überprüft, ob der Verzeichnisname mit einer der vordefinierten [**SystemFolder**](systemfolder.md) -Eigenschaften beginnt. Er überprüft nicht, ob der Verzeichnisname genau der Verzeichnis Eigenschaft entspricht. Jedes Verzeichnis, das mit einem dieser Standardordner Namen beginnt, erhält eine benutzerdefinierte Aktion vom Typ 51, auch wenn der Rest des Namens keine GUID ist. Autoren müssen darauf achten, dass dies keine falsch positiven Übereinstimmungen und unbeabsichtigte Generierung von benutzerdefinierten Aktionen auf abgeleiteten primär Schlüsseln erzeugt, die mit einer der **SystemFolder** -Eigenschaften beginnen.

Im folgenden finden Sie ein Beispiel für eine Verzeichnis Tabelle in einem Mergemodul und die erwarteten aufgelösten Verzeichnisse.



| Verzeichnis                                              | Über \_ geordnetes Verzeichnis                                | DefaultDir  |
|--------------------------------------------------------|--------------------------------------------------|-------------|
| TARGETDIR                                              |                                                  | SourceDir   |
| Dir00. BC82E350 \_ C7FC \_ 11d1 \_ A848-006097abde17        | TARGETDIR                                        | .: MMM \_ Prog |
| System Folder. BC82E350 \_ C7FC \_ 11d1 \_ A848-006097abde17 | TARGETDIR                                        | MMM \_ sys    |
| Dir02. BC82E350 \_ C7FC \_ 11d1 \_ A848-006097abde17        | Dir00. BC82E350 \_ C7FC \_ 11d1 \_ A848 \_ 006097abde17 | MFC \_ ocx    |



 

Ein Mergemodul mit der obigen Verzeichnis Tabelle erwartet die folgende Verzeichnisstruktur.



| Verzeichnis                                              | Ziel                                     | `Source`                                               |
|--------------------------------------------------------|--------------------------------------------|------------------------------------------------------|
| Dir00. BC82E350 \_ C7FC \_ 11d1 \_ A848-006097abde17        | \[Installations Punkt des Mergemoduls\]\\         | \[Quellpunkt des Mergemoduls \] \\ mmm \_ Prog           |
| System Folder. BC82E350 \_ C7FC \_ 11d1 \_ A848-006097abde17 | \[Systemordner\]\\                         | \[Quellpunkt des Mergemoduls \] \\ mmm \_ sys            |
| Dir02. BC82E350 \_ C7FC \_ 11d1 \_ A848-006097abde17        | \[Installationspunkt des Mergemoduls \] \\ MFC \_ ocx | \[Quellpunkt des Merge-Moduls, \] \\ mmm- \_ \\ MFC \_ ocx |



 

 

 



