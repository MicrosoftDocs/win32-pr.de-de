---
description: Legen Sie immer die Codepage einer Datenbank fest, bevor Sie Lokalisierungsinformationen hinzufügen.
ms.assetid: 0d8aee30-989a-4093-8718-1bb90029c0fb
title: Festlegen der Codepage einer Datenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c9ac1840b624b821dff6a85bee94607cd9568dcd6bb9b01025cb02f87c5c39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628540"
---
# <a name="setting-the-code-page-of-a-database"></a>Festlegen der Codepage einer Datenbank

Legen Sie immer die Codepage einer Datenbank fest, bevor Sie Lokalisierungsinformationen hinzufügen. Der Versuch, die Codepage nach dem Eingeben von Daten in die Datenbank zu festlegen, wird nicht empfohlen, da dadurch erweiterte Zeichen beschädigt werden könnten. Die Lokalisierung kann stark vereinfacht werden, indem mit einer Datenbank gestartet wird, die codepageneutral ist. Weitere Informationen finden Sie unter [Erstellen einer Datenbank mit einer neutralen Codepage.](creating-a-database-with-a-neutral-code-page.md) Sie können die aktuelle Codepage einer Datenbank ermitteln, wie unter Bestimmen der Codepage [einer Installationsdatenbank beschrieben.](determining-an-installation-database-s-code-page.md) Eine [Liste der numerischen Codepages](localizing-the-error-and-actiontext-tables.md) finden Sie unter Lokalisieren der Fehler- und Aktionstexttabellen.

Sie können die Codepage einer leeren Datenbank oder einer Datenbank mit einer neutralen Codepage festlegen, indem Sie eine Textarchivdatei mit einer nicht neutralen Codepage mit [**MsiDatabaseImport importieren.**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) Dadurch wird die Codepage der Datenbank auf die Codepage der importierten Datei geändert. Alle Archivdateien, die anschließend in die Datenbank importiert werden, müssen dann dieselbe Codepage wie die erste Datei haben. Wenn eine Textarchivdatei aus einer Datenbank exportiert wird, ist die Codepage der Archivdatei mit der übergeordneten Datenbank identisch. Weitere Informationen [finden Sie unter Codepagebehandlung für importierte und exportierte Tabellen.](code-page-handling-of-imported-and-exported-tables.md)

Die Codepage einer beliebigen Datenbank kann mit [**msiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) auf eine angegebene numerische Codepage festgelegt werden, um eine Textarchivdatei im folgenden Format zu importieren: zwei leere Zeilen; gefolgt von einer Zeile, die die numerische Codepage, ein Tabstopptrennzeichen und die genaue Zeichenfolge enthält: \_ ForceCodepage. Beachten Sie, dass Windows 2000 alle Zeichenfolgen in der Datenbank in die Codepage von \_ ForceCodepage übersetzt. Dies kann beim Lokalisieren einer vorhandenen Datenbank und beim Übersetzen aller nicht neutralen Zeichenfolgen in die neue Codepage vorgesehen sein. Dies führt jedoch zu einem Fehler, wenn die Datenbank nicht neutrale Zeichenfolgen enthält, die nicht übersetzt werden sollen.

Das Hilfsprogramm WiLangId.vbs ein Beispiel dafür, wie die Codepage eines Pakets mithilfe der [**Import-Methode festgelegt wird.**](database-import.md) Eine Kopie der WiLangId.vbs wird im Windows Installer SDK bereitgestellt. Mit diesem Hilfsprogramm können Sie die Sprachversionen bestimmen, die von der Datenbank unterstützt werden (Paket), die Sprache, die das Installationsprogramm für alle Zeichenfolgen auf der Benutzeroberfläche verwendet, die nicht in der Datenbank erstellt wurden (Produkt) oder die einzelne ANSI-Codepage für den Zeichenfolgenpool (Codepage). Informationen zur Verwendung von WiLangId.vbs hilfeseite: Manage Language and Codepage (Verwalten [von Sprache und Codepage).](manage-language-and-codepage.md)

Um die Werte von Product, Package und Codepage zu bestimmen, führen Sie WiLangId.vbs wie folgt aus.

**cscript wilangid.vbs** *\[ Pfad zur \] Datenbank*

Führen Sie zum Festlegen der Codepage des Pakets die folgende Befehlszeile aus.

**cscript wilangid.vbs** *\[ zum Codepage-Wert \]* **der** *\[ Datenbank \]*

Führen Sie beispielsweise die folgende Befehlszeile aus, um die Codepage von test.msi auf den numerischen ANSI-Codepagewert 1252 zu setzen.

**cscript wilangid.vbs c: \\ temp \\test.msi Codepage 1252**

 

 



