---
description: Ein Mergemodul kann auf eine .msi angewendet werden, um der Installation Verzeichnisse hinzuzufügen. Vorhandene Verzeichnisse können jedoch nicht ersetzt oder entfernt werden.
ms.assetid: 5b808aa2-b2b2-4703-bd57-0b5e1e73b306
title: Erstellen von Verzeichnistabellen für Mergemodule
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f90768dff191b729d482f8ddd58a821a6ed440e79fcd1453ff412aaf7b8a76fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086270"
---
# <a name="authoring-merge-module-directory-tables"></a>Erstellen von Verzeichnistabellen für Mergemodule

Ein Mergemodul kann auf eine .msi angewendet werden, um der Installation Verzeichnisse hinzuzufügen. Vorhandene Verzeichnisse können jedoch nicht ersetzt oder entfernt werden. Die [Tabelle Directory gibt](directory-table.md) das Layout der Verzeichnisse an, die das Mergemodul für die Zielinstallation angibt. In jedem Mergemodul ist eine Verzeichnistabelle erforderlich.

Befolgen Sie die folgenden Richtlinien, wenn Sie die Verzeichnistabelle in einem Mergemodul erstellen. Weitere Informationen finden Sie unter [Verzeichnistabelle und](directory-table.md) [Verwenden der Verzeichnistabelle](using-the-directory-table.md).

-   Die vom Mergemodul hinzugefügte Verzeichnisstruktur muss über ein einzelnes Stammverzeichnis verfügen. Der Stamm muss TARGETDIR heißen. Der Benutzer kann den Wert von TARGETDIR während der Zusammenführung ändern, um anzugeben, wo die Verzeichnisstruktur des Moduls an die Verzeichnisstruktur des Ziels angefügt werden soll.
-   Andere Modultabellen als die Directory-Tabelle dürfen nicht direkt auf Verzeichnispfade in TARGETDIR verweisen. Der Speicherort eines solchen Verweises ändert sich, wenn der Wert von TARGETDIR vom Benutzer geändert wird.
-   Die Tabellen im Mergemodul müssen auf den Speicherort eines untergeordneten Verzeichnisses von TARGETDIR oder auf ein anderes Verzeichnis in der Struktur des Mergemoduls verweisen. Gehen Sie wie folgt vor, um TARGETDIR als übergeordnetes Element eines Verzeichnisses im Mergemodul anzugeben. Geben Sie das Verzeichnis in die Spalte Verzeichnis ein, und geben Sie TARGETDIR in die Spalte Directory \_ Parent (Übergeordnetes Verzeichnis) ein. Verwenden Sie die Notation "." in der Spalte DefaultDir, um anzugeben, dass sich dieses Verzeichnis in TARGETDIR ohne Unterverzeichnis befindet. Weitere Informationen finden Sie unter [Verwenden der Verzeichnistabelle](using-the-directory-table.md).
-   Die Namen von Verzeichnissen, die vom Mergemodul hinzugefügt werden, müssen die Namenskonventionen verwenden, die unter Naming Primary Keys in Merge Module Databases (Benennen von [Primärschlüsseln in Mergemoduldatenbanken) beschrieben sind.](naming-primary-keys-in-merge-module-databases.md) Dies schließt Verzeichnisse ein, die durch Eigenschaften wie die [**SystemFolder-Eigenschaft**](systemfolder.md) und [**die ProgramFilesFolder-Eigenschaft vordefiniert**](programfilesfolder.md) sind.
-   Fügen Sie [*jedem Eintrag*](g-gly.md) in der Directory-Tabelle (mit Ausnahme von TARGETDIR) eine GUID an. Dies schließt Verzeichnistabelleneinträge ein, die Windows Installer [**SystemFolder-Eigenschaften**](systemfolder.md) angeben, z.B. SystemFolder.00000000 \_ 0000 \_ 0000 \_ 0000 \_ 00000000000. Die Bibliotheksbibliothek Mergemod.dll benutzerdefinierte Aktionen zum Festlegen der **SystemFolder-Eigenschaft** hinzu.
-   Wenn ein vordefiniertes Verzeichnis in einem Mergemodul enthalten ist, fügt das Mergetool der Zieldatenbank automatisch einen benutzerdefinierten Aktionstyp [51](custom-action-type-51.md) hinzu. Der Erautor des Mergemoduls muss sicherstellen, dass auch [eine CustomAction-Tabelle](customaction-table.md) enthalten ist. Die CustomAction-Tabelle ist möglicherweise leer, aber diese Tabelle muss in der Zieldatenbank vorhanden sein und stellt sicher, dass die geänderten vordefinierten Verzeichnisse an die richtigen Speicherorte geschrieben werden. Wenn beispielsweise ein Systemverzeichnis in einem Mergemodul enthalten ist, muss der Erautor des Mergemoduls sicherstellen, dass eine Tabelle für benutzerdefinierte Aktionen vorhanden ist.

    Beachten Sie, dass der übereinstimmende Algorithmus für die Generierung dieser benutzerdefinierten Aktionen vom Typ 51 nur überprüft, ob der Verzeichnisname mit einer der vordefinierten [**SystemFolder-Eigenschaften**](systemfolder.md) beginnt. Es wird nicht überprüft, ob der Verzeichnisname genau der Verzeichniseigenschaft entspricht. Jedes Verzeichnis, das mit einem dieser Standardordnernamen beginnt, erhält eine benutzerdefinierte Aktion vom Typ 51, auch wenn der Rest des Namens keine GUID ist. Autoren müssen darauf achten, dass dies keine falsch positiven Übereinstimmungen und unbeabsichtigte benutzerdefinierte Aktionsgenerierung für abgeleitete Primärschlüssel generiert, die mit einer der **SystemFolder-Eigenschaften** beginnen.

Im Folgenden finden Sie ein Beispiel für eine Directory-Tabelle in einem Mergemodul und die erwarteten aufgelösten Verzeichnisse.



| Verzeichnis                                              | Übergeordnetes Verzeichnis \_                                | DefaultDir  |
|--------------------------------------------------------|--------------------------------------------------|-------------|
| Targetdir                                              |                                                  | SourceDir   |
| Dir00.BC82E350 \_ C7FC \_ 11d1 \_ A848-006097ABDE17        | Targetdir                                        | .:MMM \_ Prog |
| SystemFolder.BC82E350 \_ C7FC \_ 11d1 \_ A848-006097ABDE17 | Targetdir                                        | MMM \_ Sys    |
| Dir02.BC82E350 \_ C7FC \_ 11d1 \_ A848-006097ABDE17        | Dir00.BC82E350 \_ C7FC \_ 11d1 \_ A848 \_ 006097ABDE17 | MFC \_ OCX    |



 

Es wird erwartet, dass ein Mergemodul mit der obigen Directory-Tabelle die folgende Verzeichnisstruktur zur Folge hat.



| Verzeichnis                                              | Ziel                                     | `Source`                                               |
|--------------------------------------------------------|--------------------------------------------|------------------------------------------------------|
| Dir00.BC82E350 \_ C7FC \_ 11d1 \_ A848-006097ABDE17        | \[Merge Module es Install Point (Installationspunkt des Mergemoduls)\]\\         | \[MMM Prog des \] \\ Quellpunkts des \_ Mergemoduls           |
| SystemFolder.BC82E350 \_ C7FC \_ 11d1 \_ A848-006097ABDE17 | \[SystemFolder\]\\                         | \[Mmm Sys des Quellpunkts \] \\ des \_ Mergemoduls            |
| Dir02.BC82E350 \_ C7FC \_ 11d1 \_ A848-006097ABDE17        | \[Install Point \] \\ MFC OCX des \_ Mergemoduls | \[Merge Module es Source Point \] \\ MMM \_ Prog \\ MFC \_ OCX |



 

 

 



