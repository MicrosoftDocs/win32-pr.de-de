---
description: Sie können einer Installationsdatenbank Lokalisierungsinformationen hinzufügen, indem Sie ASCII-Textarchivdateien mithilfe von MsiDatabaseExport und MsiDatabaseImport importieren und exportieren.
ms.assetid: dc52313b-38e7-43cc-abfd-86966c836fce
title: Codepagebehandlung von importierten und exportierten Tabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f9a64617ccfda25380076d62e6dd4ad8c18c55f68afd0236b3258638c899f29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066000"
---
# <a name="code-page-handling-of-imported-and-exported-tables"></a>Codepagebehandlung von importierten und exportierten Tabellen

Sie können einer Installationsdatenbank Lokalisierungsinformationen hinzufügen, indem Sie ASCII-Textarchivdateien mithilfe von [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) und [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)importieren und exportieren. Da der Datenbankzeichenfolgenpool eine ANSI-Codepage verwendet, verfügen sowohl die Datenbank als auch die exportierten [Textarchivdateien](text-archive-files.md) über Codepages.

Wenn eine [Textarchivdatei](text-archive-files.md) aus einer Datenbank exportiert wird, entspricht die Codepage der Archivdatei der übergeordneten Datenbank. Eine Liste der numerischen Codepages finden Sie unter [Lokalisieren der Fehler- und ActionText-Tabellen.](localizing-the-error-and-actiontext-tables.md)

> [!Note]  
> Beim Exportieren einer Tabelle in eine Textarchivdatei werden die Steuerzeichen übersetzt, um Konflikte mit Dateitrennzeichen zu vermeiden.

 

## <a name="ascii-text-archive-files"></a>ASCII-Textarchivdateien

Die von [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) exportierten [ASCII-Textarchivdateien](text-archive-files.md) werden im folgenden Format erläutert:

-   Die Namen der Tabellenspalten werden in der ersten Zeile geschrieben.
-   Die Spaltenformate werden in der zweiten Zeile geschrieben.
-   Wenn die Tabelle nur ASCII-Daten enthält, ist die dritte Zeile der Textdatei der Tabellenname gefolgt von einer Liste der Primärschlüssel.
-   Wenn die Tabelle Nicht-ASCII-Daten enthält und die Datenbank mit einer numerischen Codepage gestempelt wird, wird die Nummer der Codepage am Anfang der dritten Zeile angezeigt.
-   Wenn die Datenbank Nicht-ASCII-Daten enthält, die Datenbank jedoch nicht mit der numerischen Codepage gestempelt wird, wird die aktuelle Systemcodepagenummer am Anfang der dritten Zeile geschrieben.
-   Die verbleibenden Zeilen der Textdatei sind die Daten auf der angegebenen Codepage.
-   Wenn eine Tabelle Streams enthält, exportiert [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) jeden Stream in der Tabelle in eine separate Datei.

### <a name="neutral-and-non-neutral-code-pages"></a>Neutrale und nicht neutrale Codepages

Sie können die Lokalisierung vereinfachen, indem Sie mit einer Datenbank beginnen, die über eine neutrale Codepage verfügt:

-   Eine leere Datenbank verfügt über eine neutrale Codepage.
-   Eine Datenbank, die keine erweiterten Zeichen enthält, für die eine Codepage im ASCII-Format dargestellt werden muss, verfügt über eine neutrale Codepage.

Weitere Informationen finden Sie unter [Erstellen einer Datenbank mit einer neutralen Codepage.](creating-a-database-with-a-neutral-code-page.md)

Neutrale und nicht neutrale Codepages weisen die folgenden Merkmale auf:

-   Wenn eine [Textarchivdatei](text-archive-files.md) mit einer nicht neutralen Codepage in eine Datenbank importiert wird, die über eine andere nicht neutrale Codepage verfügt, gibt der Installer einen Fehler zurück, wenn [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) aufgerufen wird.
-   Eine [Textarchivdatei](text-archive-files.md) mit einer neutralen Codepage kann in eine Datenbank importiert werden, die über eine beliebige Codepage verfügt.
-   Eine [Textarchivdatei](text-archive-files.md) mit einer beliebigen Codepage kann in eine Datenbank importiert werden, die über eine neutrale Codepage verfügt.
-   Beim Importieren einer [Textarchivdatei](text-archive-files.md) in eine Datenbank mit einer neutralen Codepage wird die Codepage der Datenbank auf die Archivdatei-Codepage festgelegt. Alle Archivdateien, die anschließend in die Datenbank importiert werden, müssen die gleiche Codepage wie die erste Datei aufweisen.

Weitere Informationen finden Sie unter [Determining an Installation Database Code Page (Bestimmen einer Installationsdatenbank-Codepage)](determining-an-installation-database-s-code-page.md) und [Setting the Code Page of a Database (Festlegen der Codepage einer Datenbank).](setting-the-code-page-of-a-database.md)

Die von [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) exportierten [Textarchivdateien](text-archive-files.md) können mit Versionskontrollsystemen verwendet werden. Verwenden Sie [database Functions](database-functions.md) oder einen Datenbanktabellen-Editor, um die Datenbank zu bearbeiten.

Sie können einer Installationsdatenbank Lokalisierungsinformationen hinzufügen, indem Sie einen Datenbanktabellen-Editor oder die Windows Installer-API verwenden. Weitere Informationen finden Sie unter [Codepagebehandlung von Parameterzeichenfolgen.](code-page-handling-of-parameter-strings.md)

 

 



