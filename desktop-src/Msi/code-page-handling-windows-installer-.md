---
description: Der Windows Installer speichert alle Daten Bank Zeichenfolgen in einem einzelnen freigegebenen Zeichen folgen Pool, um die Größe der Datenbank zu reduzieren und die Leistung zu verbessern. Eine Liste numerischer Codepages finden Sie unter Lokalisieren der Fehler-und Aktions Text Tabellen.
ms.assetid: 5d413fb7-99da-49f3-ace3-ec285df2e634
title: Code Page Behandlung (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6db2788a1bfc6bdb49ec1402d5bba8a1a2594b30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343354"
---
# <a name="code-page-handling-windows-installer"></a>Code Page Behandlung (Windows Installer)

Der Windows Installer speichert alle Daten Bank Zeichenfolgen in einem einzelnen freigegebenen Zeichen folgen Pool, um die Größe der Datenbank zu reduzieren und die Leistung zu verbessern. Eine Liste numerischer Codepages finden Sie unter [lokalisieren der Fehler-und Aktions Text Tabellen](localizing-the-error-and-actiontext-tables.md).

Weitere Informationen finden Sie unter [bestimmen der Codepage einer Installations Datenbank](determining-an-installation-database-s-code-page.md).

Windows Installer verwendet [**IsValidCodePage**](/windows/desktop/api/winnls/nf-winnls-isvalidcodepage) , um zu bestimmen, ob die Codepage gültig ist.

### <a name="localizing-a-windows-installer-package"></a>Lokalisieren eines Windows Installer Pakets

Wenn Sie ein Windows Installer Paket lokalisieren, kann es u. u. das Ändern von Informationen in Datenbanktabellen, das Exportieren der Tabellen in ANSI-Textarchiv Dateien und das anschließende Importieren der Archivdateien in die zu Lokalisier Ende Datenbank einschließen. Sie können einer Datenbank auch Lokalisierungs Änderungen hinzufügen, indem Sie einen Datenbanktabellen-Editor oder die [Datenbankfunktionen](database-functions.md)verwenden. Es ist wichtig, die Codepage der Datenbank festzulegen, die lokalisiert wird, bevor Sie Lokalisierungs Änderungen an der Datenbank vornehmen. Legen Sie die Codepage der Datenbank nach dem Lokalisieren der Datenbank nicht fest, da dadurch erweiterte Zeichen beschädigt werden können. Weitere Informationen finden Sie unter [Festlegen der Codepage einer Datenbank](setting-the-code-page-of-a-database.md).

Die empfohlene Vorgehensweise für die Verarbeitung von Codepages besteht darin, eine neutrale Datenbank zu erstellen, die nur Zeichen enthält, die in eine beliebige Codepage übersetzt werden können. Weitere Informationen finden Sie unter [Erstellen einer Datenbank mit einer neutralen Codepage](creating-a-database-with-a-neutral-code-page.md).

Wenn Sie Lokalisierungs Informationen zu Datenbankarchiv Dateien hinzufügen, können Sie mithilfe von [**msidatabaseexport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) Tabellen aus einer Datenbank exportieren, die Lokalisierungs Änderungen an ANSI-Textarchiv Dateien enthält, und diese dann in die Datenbank importieren, die mit [**msidatabaseimport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)lokalisiert wird. Die Codepage einer exportierten Archivdatei ist immer identisch mit der übergeordneten Datenbank. Die Codepages einer importierten Datei und der Datenbank, die die Datei empfängt, müssen identisch sein, oder mindestens eine der beiden Codepages muss neutral sein. Weitere Informationen finden Sie unter [Code Page Handling of importierte and exportierte Tables](code-page-handling-of-imported-and-exported-tables.md).

Wenn Sie Lokalisierungs Informationen mit einem Text-Editor hinzufügen oder die [Datenbankfunktionen](database-functions.md) darauf achten, nur Zeichen folgen Parameter an die Windows Installer-API zu übergeben, die die Codepage der zu lokalisierenden Datenbank verwendet. Wenn ein Zeichen folgen Parameter Zeichen enthält, die nicht von der Codepage der Datenbank dargestellt werden, tritt ein Fehler auf, wenn [**msidatabasecommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)aufgerufen wird. Weitere Informationen finden Sie unter [Code Page Handling of Parameter Strings](code-page-handling-of-parameter-strings.md).

Wenn ein Paket verwendet wird, um mehrere Sprachversionen eines Produkts zu installieren, kann die Transformation, die zum Lokalisieren von Zeichen folgen verwendet wird, auch die Codepage der Datenbank ändern.

 

 
