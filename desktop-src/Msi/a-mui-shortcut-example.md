---
description: In diesem Abschnitt wird beschrieben, wie Sie der Windows Installer-Verknüpfungstabelle Ressourcenzeichenfolgen für die Verwendung mit mehrsprachigen Benutzeroberflächen (MULTILINGUAL) hinzufügen.
ms.assetid: f521cfb8-32a8-4b62-b258-5b99cc3e0416
title: Beispiel für eine SHORTCUT-Verknüpfung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b38f674a63e854fbcd4439229c5aded5b0efe6cfc17d3e475f8a52f30db949
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640287"
---
# <a name="a-mui-shortcut-example"></a>Beispiel für eine SHORTCUT-Verknüpfung

In diesem Abschnitt wird beschrieben, wie Sie der Windows [Installer-Verknüpfungstabelle](shortcut-table.md) Ressourcenzeichenfolgen für die Verwendung mit mehrsprachigen Benutzeroberflächen (MULTILINGUAL) hinzufügen.

**Windows Installer 2.0 und Windows Installer 3.0:** Nicht unterstützt. Dieses Beispiel erfordert Windows Installer 4.0.

Informationen zum [Entwickeln von ANWENDUNGEN, die FÜR DIE -Anwendung aktiviert](/windows/desktop/Intl/multilingual-user-interface) sind, finden Sie in der DOKUMENTATION zum mehrsprachige Benutzeroberfläche ().

So fügen Sie die ressourcenzeichenfolgen, die von Windows Vista Multilingual User Interfaces verwendet werden, einem Windows Installer-Paket hinzu:

1.  Fügen Sie der Dateitabelle die Informationen für alle sprachneutralen Dateien und [Sprachdateien hinzu.](file-table.md) Die Dateien können z. B. aus einer sprachneutralen Datei (msimsg.dll) und Sprachdateien für Englisch (msimsgen.dll.soll), Japanisch (msimsgja.dll.soll) und Chinesisch (msimsgcs.dll.soll enthalten sein). Jede Datei kann zu einer anderen Komponente gehören. Jede Datei kann sowohl einen langen als auch einen kurzen Dateinamen haben. Im Fall dieses Beispiels können der Dateitabelle die folgenden [Informationen hinzugefügt werden.](file-table.md)

    [Dateitabelle](file-table.md) (partiell)

    

    | Datei        | Komponente\_     | FileName                     |
    |-------------|-----------------|------------------------------|
    | msimsgmusprogramms | \_MSIMSG-MSI-JA \_ | msimsgja.dll\|msimsg.dll.soll |
    | msimsgmuics | MSIMSG \_ MUI \_ CS | msimsgcs.dll\|msimsg.dll.soll |
    | msimsgmuien | MSIMSG \_ MSIMSG MSI \_ EN | msimsgen.dll\|msimsg.dll.soll |
    | msimsgdll   | MSIMSG          | msimsg.dll                   |

    

     

2.  Fügen Sie der [Component-Tabelle Informationen für](component-table.md) diese Komponenten hinzu. Jede Komponente verfügt über einen eindeutigen GUID-Bezeichner, der in das Feld ComponentId der Tabelle Component eingegeben werden soll. Die Datei, die zur Komponente gehört, kann als KeyPath für diese Komponente dienen. Das Verzeichnis, das die einzelnen Komponenten enthält, kann im Feld Verzeichnis angegeben \_ werden. Die folgenden Informationen können der Component-Tabelle hinzugefügt werden.

    [Komponententabelle](component-table.md) (partiell)

    

    | Komponente       | Verzeichnis\_   | KeyPath     |
    |-----------------|---------------|-------------|
    | \_MSIMSG-MSI-JA \_ | VERBINDEOrdner \_ JA | msimsgmusprogramms |
    | MSIMSG \_ MUI \_ CS | VERBINDer \_ CS | msimsgmuics |
    | MSIMSG \_ MSIMSG MSI \_ EN | VERBINDEOrdner \_ EN | msimsgmuien |
    | MSIMSG          | BAUFolder     | msimsgdll   |

    

     

3.  Bearbeiten Sie [die Directory-Tabelle,](directory-table.md) damit die Komponenten in den richtigen Verzeichnissen installiert werden. Stellen Sie sicher, dass Sie Informationen zu dem Verzeichnis hinzufügen, in dem die Verknüpfung installiert wird. Beispielsweise können der Verzeichnistabelle eines Pakets, das die Komponenten installiert, und einer Verknüpfung im Verzeichnis DesktopFolder die folgenden Informationen hinzugefügt werden.

    [Verzeichnistabelle](directory-table.md) (partiell)

    

    | Verzeichnis     | Übergeordnetes Verzeichnis \_ | DefaultDir |
    |---------------|-------------------|------------|
    | Targetdir     |                   | SourceDir  |
    | MsiTest       | Targetdir         | MsiTest:  |
    | BAUFolder     | MsiTest           | Mui        |
    | VERBINDer \_ CS | BAUFolder         | cs-CZ      |
    | VERBINDEOrdner \_ EN | BAUFolder         | en-US      |
    | VERBINDEOrdner \_ JA | BAUFolder         | ja-JP      |
    | DesktopFolder | Targetdir         | .          |

    

     

4.  Fügen Sie der Verknüpfungstabelle [für jede Verknüpfung](shortcut-table.md) eine Zeile hinzu. Die [Verknüpfungstabelle](shortcut-table.md) kann beispielsweise die folgenden Informationen für die beiden Tastenkombinationen Quick1 und Quick2 enthalten, die im Verzeichnis DirectoryFolder installiert sind. Jede Verknüpfung gehört zu dem Feature, das im Feld Ziel angegeben ist. Das symbol, das der Verknüpfung zugeordnet ist, kann im Feld Symbol und in \_ der Tabelle Symbol [angegeben](icon-table.md) werden.

    [Verknüpfungstabelle](shortcut-table.md) (partiell)

    

    | Verknüpfung | Verzeichnis\_   | Komponente\_ | Ziel               | Symbol             |
    |----------|---------------|-------------|----------------------|------------------|
    | Quick1   | DesktopFolder | MSIMSG      | FeatureChild1 \_ Local | HelpFileIcon.exe |
    | Quick2   | DesktopFolder | MSIMSG      | FeatureChild1 \_ Local | HelpFileIcon.exe |

    

     

5.  Fügen Sie der Tabelle ["Featuretabelle" Informationen](feature-table.md) für die Verknüpfung feature owns hinzu. Wenn die Verknüpfung aktiviert ist, überprüft das Installationsprogramm, ob alle Komponenten, die zu diesem Feature gehören, installiert sind, bevor die Schlüsseldatei der Komponente gestartet wird, die in der Spalte Komponente der Verknüpfungstabelle \_ [angegeben](shortcut-table.md) ist. Im Fall dieses Beispiels können der Tabelle Feature Table für das FeatureParent1 Local-Feature die folgenden \_ Informationen hinzugefügt werden.

    [Featuretabelle](feature-table.md) (partiell)

    

    | Komponente               | Übergeordnetes \_ Feature       | Titel                 | Attribute |
    |-----------------------|-----------------------|-----------------------|------------|
    | FeatureParent1 \_ Lokal |                       | FeatureParent1 \_ Lokal | 16         |
    | FeatureChild1 \_ Local  | FeatureParent1 \_ Lokal | FeatureParent1 \_ Lokal | 0          |

    

     

6.  Fügen Sie für jede neue Verknüpfung die Ressourcenzeichenfolgeninformationen den Feldern DisplayResourceDLL, DisplayResourceId, DescriptionResourceDLL und DescriptionResourceId der [Verknüpfungstabelle hinzu.](shortcut-table.md) Die Felder DisplayResourceDLL und DescriptionResourceDLL enthalten die Ressourcenzeichenfolge im [formatierten](formatted.md) Zeichenfolgenformat. Die formatierte Zeichenfolge kann die \[ \# *Dateischlüsselkonvention* \] des [formatierten Formats](formatted.md) verwenden. Fügen Sie die Anzeige- und Beschreibungsindizes für die Ressourcenzeichenfolgen in den Feldern DisplayResourceId und DescriptionResourceId hinzu.

    [Verknüpfungstabelle](shortcut-table.md) (partiell)

    

    | Verknüpfung | DisplayResourceDLL | DisplayResourceId | DescriptionResourceDLL | DescriptionResourceId |
    |----------|--------------------|-------------------|------------------------|-----------------------|
    | Quick1   | \[\#msimsgdll\]    | 36                | \[\#msimsgdll\]        | 37                    |
    | Quick2   | \[\#msimsgdll\]    | 38                | \[\#msimsgdll\]        | 39                    |

    

     

7.  Testen Sie nach der Installation des Pakets, um sicherzustellen, dass mehrsprachige Benutzeroberfläche wie erwartet funktioniert.

 

 
