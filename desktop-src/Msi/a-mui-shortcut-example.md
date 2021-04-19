---
description: In diesem Abschnitt wird beschrieben, wie Sie der Windows Installer Verknüpfungs Tabelle Ressourcen Zeichenfolgen zur Verwendung mit mehrsprachigen Benutzeroberflächen (MUI) hinzufügen.
ms.assetid: f521cfb8-32a8-4b62-b258-5b99cc3e0416
title: Beispiel für eine MUI-Verknüpfung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0392713c1eaedabaa989baecd79478a9b329e955
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362427"
---
# <a name="a-mui-shortcut-example"></a>Beispiel für eine MUI-Verknüpfung

In diesem Abschnitt wird beschrieben, wie Sie [der Windows Installer](shortcut-table.md) Verknüpfungs Tabelle Ressourcen Zeichenfolgen zur Verwendung mit mehrsprachigen Benutzeroberflächen (MUI) hinzufügen.

**Windows Installer 2,0 und Windows Installer 3,0:** Nicht unterstützt. Für dieses Beispiel ist Windows Installer 4,0 erforderlich.

Weitere Informationen zum Entwickeln von MUI-fähigen Anwendungen finden Sie in der Dokumentation für die [mehrsprachige Benutzeroberfläche (MUI)](/windows/desktop/Intl/multilingual-user-interface) .

So fügen Sie die von den mehrsprachigen Windows Vista-Benutzeroberflächen verwendeten Ressourcen Zeichenfolgen zu einem Windows Installer Paket hinzu:

1.  Fügen Sie der [Dateitabelle](file-table.md)die Informationen für alle sprach neutralen Dateien und Sprachdateien hinzu. Beispielsweise können die Dateien aus sprach neutralen Dateien (msimsg.dll) und Sprachdateien für Englisch (msimsgen.dll. MUI), Japanisch (msimsgja.dll. MUI) und Chinesisch (msimsgcs.dll. MUI) bestehen. Jede Datei kann zu einer anderen Komponente gehören. Jede Datei kann sowohl einen langen als auch einen kurzen Dateinamen haben. Im Fall dieses Beispiels können der [Dateitabelle](file-table.md)die folgenden Informationen hinzugefügt werden.

    [Dateitabelle](file-table.md) (partiell)

    

    | File        | Komponente\_     | FileName                     |
    |-------------|-----------------|------------------------------|
    | msimsgmuija | msimsg \_ MUI \_ Ja | msimsgja.dll\|msimsg.dll. MUI |
    | msimsgmuics | msimsg- \_ MUI- \_ CS | msimsgcs.dll\|msimsg.dll. MUI |
    | msimsgmuien | msimsg- \_ MUI \_ | msimsgen.dll\|msimsg.dll. MUI |
    | msimsgdll   | Msimsg          | msimsg.dll                   |

    

     

2.  Fügen Sie der Komponenten [Tabelle](component-table.md) Informationen für diese Komponenten hinzu. Jede Komponente verfügt über einen eindeutigen GUID-Bezeichner, der in das Feld "ComponentId" der Komponenten Tabelle eingegeben werden sollte. Die Datei, die zur Komponente gehört, kann als KEYPATH für diese Komponente fungieren. Das Verzeichnis, das die einzelnen Komponenten enthält, kann im Verzeichnis \_ Feld angegeben werden. Die folgenden Informationen können der Component-Tabelle hinzugefügt werden.

    [Komponenten Tabelle](component-table.md) (partiell)

    

    | Komponente       | Verzeichnis\_   | KEYPATH     |
    |-----------------|---------------|-------------|
    | msimsg \_ MUI \_ Ja | Muifolder- \_ Ja | msimsgmuija |
    | msimsg- \_ MUI- \_ CS | Muifolder- \_ CS | msimsgmuics |
    | msimsg- \_ MUI \_ | Muifolder \_ | msimsgmuien |
    | Msimsg          | Muifolder     | msimsgdll   |

    

     

3.  Bearbeiten Sie die [Verzeichnis](directory-table.md) Tabelle so, dass die Komponenten in den richtigen Verzeichnissen installiert werden. Stellen Sie sicher, dass Sie Informationen zu dem Verzeichnis einschließen, in dem die Verknüpfung installiert wird. Die folgenden Informationen können z. b. zur Verzeichnis Tabelle eines Pakets hinzugefügt werden, mit dem die Komponenten installiert werden, sowie eine Verknüpfung im Desktop Folder-Verzeichnis.

    [Verzeichnis Tabelle](directory-table.md) (partiell)

    

    | Verzeichnis     | Über \_ geordnetes Verzeichnis | DefaultDir |
    |---------------|-------------------|------------|
    | TARGETDIR     |                   | SourceDir  |
    | Msitest       | TARGETDIR         | Msitest:.  |
    | Muifolder     | Msitest           | MUI        |
    | Muifolder- \_ CS | Muifolder         | cs-CZ      |
    | Muifolder \_ | Muifolder         | de-DE      |
    | Muifolder- \_ Ja | Muifolder         | ja-JP      |
    | DesktopFolder | TARGETDIR         | .          |

    

     

4.  Fügen Sie der Verknüpfungs Tabelle für [jede Verknüpfung eine](shortcut-table.md) Zeile hinzu. Beispielsweise könnte die Verknüpfungs Tabelle die folgenden Informationen für zwei Verknüpfungen, Quick1 und Quick2, enthalten [, die im](shortcut-table.md) Verzeichnis directoryfolder installiert sind. Jede Verknüpfung gehört zu der Funktion, die im Zielfeld angegeben ist. Das der Verknüpfung zugeordnete Symbol kann im Symbol \_ Feld und in der [Symbol](icon-table.md) Tabelle angegeben werden.

    Verknüpfungs [Tabelle](shortcut-table.md) (partiell)

    

    | Abkürzung | Verzeichnis\_   | Komponente\_ | Ziel               | Symbol             |
    |----------|---------------|-------------|----------------------|------------------|
    | Quick1   | DesktopFolder | Msimsg      | FeatureChild1 \_ lokal | HelpFileIcon.exe |
    | Quick2   | DesktopFolder | Msimsg      | FeatureChild1 \_ lokal | HelpFileIcon.exe |

    

     

5.  Fügen Sie der [featuretabellentabelle](feature-table.md) Informationen für die Funktion hinzu, zu der die Verknüpfung gehört. Wenn die Verknüpfung aktiviert ist, überprüft das Installationsprogramm, ob alle Komponenten, die zu dieser Funktion gehören, installiert sind, bevor die Schlüsseldatei der in der Spalte Komponente der Verknüpfungs Tabelle angegebenen Komponente gestartet wird \_ . [](shortcut-table.md) Im Fall dieses Beispiels können der Tabelle Funktions Tabelle für das lokale Feature FeatureParent1 die folgenden Informationen hinzugefügt werden \_ .

    [Funktions Tabelle](feature-table.md) (partiell)

    

    | Funktion               | Über \_ geordnetes Element       | Titel                 | Attribute |
    |-----------------------|-----------------------|-----------------------|------------|
    | FeatureParent1 \_ lokal |                       | FeatureParent1 \_ lokal | 16         |
    | FeatureChild1 \_ lokal  | FeatureParent1 \_ lokal | FeatureParent1 \_ lokal | 0          |

    

     

6.  Fügen Sie für jede neue Verknüpfung die Informationen der Ressourcen Zeichenfolge zu den Feldern displayresourcedll, displayresourceid, descriptionresourcedll und descriptionresourceid der Verknüpfungs [Tabelle](shortcut-table.md)hinzu. Die Felder displayresourcedll und descriptionresourcedll enthalten die Ressourcen Zeichenfolge im Format der [formatierten](formatted.md) Zeichenfolge. Die formatierte Zeichenfolge kann die \[ \# *filekey* - \] Konvention des [formatierten](formatted.md) Formats verwenden. Fügen Sie die Anzeige-und Beschreibungs Indizes für die Ressourcen Zeichenfolgen in den Feldern displayresourceid und descriptionresourceid hinzu.

    Verknüpfungs [Tabelle](shortcut-table.md) (partiell)

    

    | Abkürzung | Displayresourcedll | Displayresourceid | Deskriptionresourcedll | Deskriptionresourceid |
    |----------|--------------------|-------------------|------------------------|-----------------------|
    | Quick1   | \[\#msimsgdll\]    | 36                | \[\#msimsgdll\]        | 37                    |
    | Quick2   | \[\#msimsgdll\]    | 38                | \[\#msimsgdll\]        | 39                    |

    

     

7.  Nachdem Sie das Paket installiert haben, testen Sie, um sicherzustellen, dass die mehrsprachige Benutzeroberfläche erwartungsgemäß funktioniert.

 

 
