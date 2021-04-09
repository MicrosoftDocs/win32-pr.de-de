---
description: Die Windows Installer Datenbanktabellen können mithilfe von msidatabaseexport oder der Export-Methode des Datenbankobjekts in ASCII-Textdateien exportiert werden.
ms.assetid: 49210242-bd32-4e5c-b782-a132d670fdfe
title: Text Archivdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8baba814fd182a7da5e13fbb26eec257be96ab1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865744"
---
# <a name="text-archive-files"></a>Text Archivdateien

Die Windows Installer Datenbanktabellen können mithilfe von [**msidatabaseexport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) oder der [**Export**](database-export.md) -Methode des [**Daten Bank**](database-object.md) Objekts in ASCII-Textdateien exportiert werden. Die Informationen in diesen Textarchiv Dateien können dann mithilfe von [**msidatabaseimport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) oder der [Import](database-import.md) -Methode des **Daten Bank** Objekts wieder in eine Windows Installer Datenbank importiert werden.

Tools wie [msidb.exe](msidb-exe.md) können Textarchiv Dateien exportieren und importieren. [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md) zum Exportieren und Importieren von Textarchiv Dateien aus einer Datenbank finden Sie unter [Exportieren von Dateien](export-files.md) und [Importieren von Dateien](import-files.md) .

> [!Note]  
> Text Archivdateien sind nicht als Mittel zum Bearbeiten der Installations Datenbank vorgesehen. Zum Erstellen und Ändern eines Installationspakets sollten Sie ein Windows Installer Tabellen Bearbeitungs Tool verwenden, z. b. [Orca](orca-exe.md) oder ein Drittanbieter Tool.

 

Text Archivdateien können für die folgenden Zwecke verwendet werden.

-   Text Archivdateien können mit Versionskontrollsystemen verwendet werden.
-   Entfernen Sie Speicherplatz, und reduzieren Sie die endgültige Größe von MSI-Dateien. Weitere Informationen finden Sie [unter Reduzieren der Größe einer MSI-Datei](reducing-the-size-of-an--msi-file.md).
-   Zum Hinzufügen von Lokalisierungs Informationen zu einer Installations Datenbank. Weitere Informationen finden Sie unter [Code Page Handling of importierte and exportierte Tables](code-page-handling-of-imported-and-exported-tables.md).

-   , Um die Codepage einer Datenbank zu bestimmen. Weitere Informationen finden Sie unter [bestimmen der Codepage einer Installations Datenbank](determining-an-installation-database-s-code-page.md).
-   , Um die Codepage einer Datenbank festzulegen. Siehe [Festlegen der Codepage einer Datenbank](setting-the-code-page-of-a-database.md).
-   , Um den Grenzwert einer Daten Bank Spalte zu erhöhen. Exportieren Sie die Tabelle mithilfe von " [**msidatabaseexport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)", bearbeiten Sie die exportierte IDT-Datei, und importieren Sie dann die Tabelle mithilfe von " [**msidatabaseimport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)". Autoren können die Spaltendatentypen, die NULL-Zulässigkeit oder die Lokalisierungs Attribute von Spalten in Standard Tabellen nicht ändern. Siehe auch [Erstellen eines großen Pakets](authoring-a-large-package.md).

Auf den folgenden Seiten werden Textarchiv Seiten und deren Formate beschrieben.

-   [Archivdatei Format](archive-file-format.md)
-   [ASCII-Daten in Text Archivdateien](ascii-data-in-text-archive-files.md)
-   [\_Forcecodepage](-forcecodepage.md)
-   [\_SummaryInformation](-summaryinformation.md)

 

 



