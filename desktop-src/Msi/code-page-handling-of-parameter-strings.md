---
description: Sie können einer Installations Datenbank Lokalisierungs Informationen hinzufügen, indem Sie einen Datenbanktabellen-Editor wie z. b. Orca verwenden, der mit dem Windows Installer SDK bereitgestellt wird, oder indem Sie die Datenbankfunktionen einer Anwendung aufrufen.
ms.assetid: cc1eb336-5dec-40cc-8aa5-564cd167855d
title: Code Page Behandlung von Parameter Zeichenfolgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a52872472d5509e1abdf35aa12be5afb6a8d13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214863"
---
# <a name="code-page-handling-of-parameter-strings"></a>Code Page Behandlung von Parameter Zeichenfolgen

Sie können einer Installations Datenbank Lokalisierungs Informationen hinzufügen, indem Sie einen Datenbanktabellen-Editor wie z. b. Orca verwenden, der mit dem Windows Installer SDK bereitgestellt wird, oder indem Sie die [Datenbankfunktionen](database-functions.md) einer Anwendung aufrufen. Achten Sie darauf, nur Zeichen folgen Parameter zu übergeben, die die Codepage der Datenbank verwenden, die lokalisiert wird. Wenn ein Zeichen folgen Parameter Zeichen enthält, die von der Codepage der Datenbank nicht dargestellt werden können, gibt das Installationsprogramm einen Fehler zurück, wenn [**msidatabaseimport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)aufgerufen wird. Eine Liste numerischer Codepages finden Sie unter [lokalisieren der Fehler-und Aktions Text Tabellen](localizing-the-error-and-actiontext-tables.md).

Weitere Informationen finden Sie unter [bestimmen der Codepage einer Installations Datenbank](determining-an-installation-database-s-code-page.md).

## <a name="adding-localization-information-to-a-database"></a>Hinzufügen von Lokalisierungs Informationen zu einer Datenbank

Wenn Sie einer Datenbank Lokalisierungs Informationen hinzufügen, muss die Codepage der Datenbank vom Betriebssystem unterstützt werden. Es muss sich nicht um die aktuelle Codepage des Systems handeln. [**IsValidCodePage**](/windows/desktop/api/winnls/nf-winnls-isvalidcodepage) muss für die Daten Bank Codepage **true** zurückgeben. Da ANSI-Zeichen folgen vom System in Unicode konvertiert werden, ist ein Fehler aufgetreten, wenn die Codepage des aktuellen Benutzers nicht mit der Daten Bank Codepage übereinstimmt.

Wenn Sie die ANSI-Version der Windows Installer-API aufrufen, wird die lokalisierte Zeichenfolge mithilfe der aktuellen System Codepage in Unicode konvertiert. Wenn für die Datenbank ein Commit ausgeführt wird, wird die Unicode-Zeichenfolge mithilfe der Codepage der Datenbank in ANSI konvertiert. Wenn die aktuelle System Codepage von der Codepage der lokalisierten Zeichenfolge abweicht, kann das Ergebnis ein Datenverlust und eine falsche Zeichen folgen Konvertierung sein.

Im folgenden Verfahren wird gezeigt, wie die Lokalisierungsdaten gespeichert werden.

**So speichern Sie Lokalisierungsdaten**

1.  Legen Sie die Codepage der Datenbank auf die Codepage der lokalisierten Zeichenfolge fest.
2.  Konvertieren Sie die ANSI-Zeichenfolge in Unicode, indem Sie die [**multibytedewidechar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) -Funktion verwenden, und geben Sie die Codepage der lokalisierten Daten an.
3.  Verwenden Sie die Unicode-Version der Windows Installer-API, um die lokalisierten Daten mit der Unicode-Zeichenfolge hinzuzufügen.
4.  Übertragen Sie die Lokalisierungs Änderungen mithilfe von [**msidatabasecommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)in der Datenbank.

Sie können einer Installations Datenbank auch Lokalisierungs Informationen hinzufügen, indem Sie ASCII-Textarchiv Dateien importieren und exportieren. Weitere Informationen finden Sie unter [Code Page Handling of importierte and exportierte Tables](code-page-handling-of-imported-and-exported-tables.md).

 

 
