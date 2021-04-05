---
description: Legen Sie die Codepage einer Datenbank vor dem Hinzufügen von Lokalisierungs Informationen immer fest.
ms.assetid: 0d8aee30-989a-4093-8718-1bb90029c0fb
title: Festlegen der Codepage einer Datenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ef04c2969d0933c4601bbca2f3897d86de43a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753008"
---
# <a name="setting-the-code-page-of-a-database"></a>Festlegen der Codepage einer Datenbank

Legen Sie die Codepage einer Datenbank vor dem Hinzufügen von Lokalisierungs Informationen immer fest. Das Festlegen der Codepage nach dem Eingeben von Daten in die Datenbank wird nicht empfohlen, da dadurch erweiterte Zeichen beschädigt werden könnten. Die Lokalisierung kann erheblich erleichtert werden, indem Sie mit einer Datenbank beginnen, die Code Page neutral ist. Weitere Informationen finden Sie unter [Erstellen einer Datenbank mit einer neutralen Codepage](creating-a-database-with-a-neutral-code-page.md). Sie können die aktuelle Codepage einer Datenbank festlegen, wie unter [bestimmen der Codepage einer Installations Datenbank](determining-an-installation-database-s-code-page.md)beschrieben. Eine Liste numerischer Codepages finden Sie [unter Lokalisieren der Fehler-und Aktions Text Tabellen](localizing-the-error-and-actiontext-tables.md) .

Sie können die Codepage einer leeren Datenbank oder eine Datenbank mit einer neutralen Codepage festlegen, indem Sie eine Textarchiv Datei mit einer nicht neutralen Codepage mit [**msidatabaseimport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)importieren. Dadurch wird die Codepage der Datenbank auf die Codepage der importierten Datei festgelegt. Alle Archivdateien, die anschließend in die Datenbank importiert werden, müssen dann die gleiche Codepage wie die erste Datei aufweisen. Wenn eine Textarchiv Datei aus einer Datenbank exportiert wird, ist die Codepage der Archivdatei mit der übergeordneten Datenbank identisch. Weitere Informationen finden Sie [unter Code Page Handling of importierten und exportierten Tabellen](code-page-handling-of-imported-and-exported-tables.md).

Die Codepage einer beliebigen Datenbank kann auf eine angegebene numerische Codepage festgelegt werden, indem [**msidatabaseimport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) verwendet wird, um eine Textarchiv Datei im folgenden Format zu importieren: zwei leere Zeilen; gefolgt von einer Zeile mit der numerischen Codepage, einem Tabstopp Trennzeichen und der exakten Zeichenfolge: \_ forcecodepage. Beachten Sie, dass bei Windows 2000 alle Zeichen folgen in der Datenbank in die Codepage von \_ forcecodepage übersetzt werden. Dies kann sinnvoll sein, wenn eine vorhandene Datenbank lokalisiert und alle nicht neutralen Zeichen folgen in die neue Codepage übersetzt werden. Dies verursacht jedoch einen Fehler, wenn die Datenbank nicht neutrale Zeichen folgen enthält, die nicht übersetzt werden müssen.

Das Hilfsprogramm WiLangId.vbs bietet ein Beispiel dafür, wie die Codepage eines Pakets mithilfe der [**Import-Methode**](database-import.md)festgelegt wird. Eine Kopie von WiLangId.vbs wird im Windows Installer SDK bereitgestellt. Mit diesem Hilfsprogramm können Sie die Sprachversionen ermitteln, die von der-Datenbank (Paket) unterstützt werden, die Sprache, die das Installationsprogramm für alle Zeichen folgen in der Benutzeroberfläche verwendet, die nicht in der Datenbank (Product) erstellt wurden, oder die einzelne ANSI-Codepage für den Zeichen folgen Pool (Codepage). Weitere Informationen zum Verwenden von WiLangId.vbs finden Sie auf der Hilfeseite: [Verwalten von Sprache und Codepage](manage-language-and-codepage.md).

Führen Sie WiLangId.vbs wie folgt aus, um die Werte von Product, Package und Codepage zu bestimmen.

**cscript-wilangid.vbs** *\[ Pfad zur \] Datenbank*

Führen Sie die folgende Befehlszeile aus, um die Codepage des Pakets festzulegen.

**cscript-wilangid.vbs** *\[ Pfad zum \]* **Codepage** - *\[ Wert \]* der Datenbank

Wenn Sie z. b. die Codepage von test.msi auf den numerischen ANSI-Code Page Wert 1252 festlegen möchten, führen Sie die folgende Befehlszeile aus.

**cscript wilangid.vbs c: \\ Temp \\test.msi Codepage 1252**

 

 



