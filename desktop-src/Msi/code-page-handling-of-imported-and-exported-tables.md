---
description: Sie können einer Installations Datenbank Lokalisierungs Informationen hinzufügen, indem Sie ASCII-Textarchiv Dateien mithilfe von "msidatabaseexport" und "msidatabaseimport" Importieren und exportieren.
ms.assetid: dc52313b-38e7-43cc-abfd-86966c836fce
title: Code Page Behandlung importierter und exportierter Tabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b090bead1fa35b451ed12e0e0da0143b98b8918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345164"
---
# <a name="code-page-handling-of-imported-and-exported-tables"></a>Code Page Behandlung importierter und exportierter Tabellen

Sie können einer Installations Datenbank Lokalisierungs Informationen hinzufügen, indem Sie ASCII-Textarchiv Dateien mithilfe von " [**msidatabaseexport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) " und " [**msidatabaseimport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)" Importieren und exportieren. Da der Daten Bank Zeichen folgen Pool eine ANSI-Codepage verwendet, verfügen sowohl die Datenbank als auch die exportierten [Text Archivdateien](text-archive-files.md) über Codepages.

Wenn eine [Text Archivdatei](text-archive-files.md) aus einer Datenbank exportiert wird, ist die Codepage der Archivdatei mit der übergeordneten Datenbank identisch. Eine Liste numerischer Codepages finden Sie unter [lokalisieren der Fehler-und Aktions Text Tabellen](localizing-the-error-and-actiontext-tables.md).

> [!Note]  
> Durch das Exportieren einer Tabelle in eine Textarchiv Datei werden die Steuerzeichen übersetzt, um Konflikte mit Datei Trennzeichen zu vermeiden.

 

## <a name="ascii-text-archive-files"></a>ASCII-Text Archivdateien

Die von [**msidatabaseexport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) exportierten ASCII- [Text Archivdateien](text-archive-files.md) werden im folgenden Format erläutert:

-   Die Namen der Tabellen Spalten werden in der ersten Zeile geschrieben.
-   Die Spalten Formate werden in der zweiten Zeile geschrieben.
-   Wenn die Tabelle nur ASCII-Daten enthält, ist die dritte Zeile der Textdatei der Tabellenname, gefolgt von einer Liste der Primärschlüssel.
-   Wenn die Tabelle nicht-ASCII-Daten enthält und die Datenbank mit einer numerischen Codepage versehen ist, wird die Code Page Nummer am Anfang der dritten Zeile angezeigt.
-   Wenn die Datenbank nicht-ASCII-Daten enthält, aber die Datenbank nicht mit der numerischen Codepage versehen ist, wird die aktuelle Systemcode Page-Nummer am Anfang der dritten Zeile geschrieben.
-   Die verbleibenden Zeilen der Textdatei sind die Daten in der angegebenen Codepage.
-   Wenn eine Tabelle Streams enthält, exportiert [**msidatabaseexport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) jeden Stream in der Tabelle in eine separate Datei.

### <a name="neutral-and-non-neutral-code-pages"></a>Neutrale und nicht neutrale Codepages

Sie können die Lokalisierung vereinfachen, indem Sie eine Datenbank mit einer neutralen Codepage starten:

-   Eine leere Datenbank verfügt über eine neutrale Codepage.
-   Eine Datenbank, die keine erweiterten Zeichen enthält, die erfordern, dass eine Codepage in ASCII dargestellt wird, verfügt über eine neutrale Codepage.

Weitere Informationen finden Sie unter [Erstellen einer Datenbank mit einer neutralen Codepage](creating-a-database-with-a-neutral-code-page.md).

Neutrale und nicht neutrale Codepages weisen die folgenden Eigenschaften auf:

-   Wenn eine [Text Archivdatei](text-archive-files.md) mit einer nicht neutralen Codepage in eine Datenbank mit einer anderen nicht neutralen Codepage importiert wird, gibt das Installationsprogramm einen Fehler zurück, wenn [**msidatabaseimport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) aufgerufen wird.
-   Eine [Text Archivdatei](text-archive-files.md) mit einer neutralen Codepage kann in eine Datenbank mit einer beliebigen Codepage importiert werden.
-   Eine [Text Archivdatei](text-archive-files.md) mit einer beliebigen Codepage kann in eine Datenbank mit einer neutralen Codepage importiert werden.
-   Wenn Sie eine [Text Archivdatei](text-archive-files.md) mit einer neutralen Codepage in eine Datenbank importieren, wird die Codepage der Datenbank auf die Codepage der Archivdatei festgelegt. Alle Archivdateien, die anschließend in die Datenbank importiert werden, müssen die gleiche Codepage wie die erste Datei aufweisen.

Weitere Informationen finden Sie unter [bestimmen der Codepage der Installations Datenbank](determining-an-installation-database-s-code-page.md) und [Festlegen der Codepage einer Datenbank](setting-the-code-page-of-a-database.md).

Die von [**msidatabaseexport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) exportierten [Text Archivdateien](text-archive-files.md) können mit Versionskontrollsystemen verwendet werden. Verwenden Sie die [Datenbankfunktionen](database-functions.md) oder einen Datenbanktabellen-Editor, um die Datenbank zu bearbeiten.

Sie können einer Installations Datenbank Lokalisierungs Informationen hinzufügen, indem Sie einen Datenbanktabellen-Editor oder die Windows Installer-API verwenden. Weitere Informationen finden Sie unter [Code Page Handling of Parameter Strings](code-page-handling-of-parameter-strings.md).

 

 



