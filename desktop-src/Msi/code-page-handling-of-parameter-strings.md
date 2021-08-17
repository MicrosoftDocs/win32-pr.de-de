---
description: Sie können einer Installationsdatenbank Lokalisierungsinformationen hinzufügen, indem Sie einen Datenbanktabellen-Editor wie Orca verwenden, der mit dem Windows Installer SDK bereitgestellt wird, oder indem Sie die Datenbankfunktionen aus einer Anwendung aufrufen.
ms.assetid: cc1eb336-5dec-40cc-8aa5-564cd167855d
title: Codepagebehandlung von Parameterzeichenfolgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37555b905c60cb8f4727ccb723435d28b24d41d3aca1fc7026e34b799e25414a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328339"
---
# <a name="code-page-handling-of-parameter-strings"></a>Codepagebehandlung von Parameterzeichenfolgen

Sie können einer Installationsdatenbank Lokalisierungsinformationen hinzufügen, indem Sie einen Datenbanktabellen-Editor wie Orca verwenden, der mit dem Windows Installer SDK bereitgestellt wird, oder indem Sie die [Datenbankfunktionen](database-functions.md) aus einer Anwendung aufrufen. Achten Sie darauf, nur Zeichenfolgenparameter zu übergeben, die die Codepage der datenbank verwenden, die lokalisiert wird. Wenn ein Zeichenfolgenparameter Zeichen enthält, die nicht durch die Codepage der Datenbank dargestellt werden können, gibt der Installer beim Aufrufen von [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)einen Fehler zurück. Eine Liste der numerischen Codepages finden Sie unter [Lokalisieren der Fehler- und ActionText-Tabellen.](localizing-the-error-and-actiontext-tables.md)

Weitere Informationen finden Sie unter [Bestimmen der Codepage einer Installationsdatenbank.](determining-an-installation-database-s-code-page.md)

## <a name="adding-localization-information-to-a-database"></a>Hinzufügen von Lokalisierungsinformationen zu einer Datenbank

Wenn Sie einer Datenbank Lokalisierungsinformationen hinzufügen, muss die Codepage der Datenbank vom Betriebssystem unterstützt werden. Es muss nicht die aktuelle Codepage des Systems sein. [**IsValidCodePage**](/windows/desktop/api/winnls/nf-winnls-isvalidcodepage) muss **TRUE** für die Datenbankcodepage zurückgeben. Da das System ANSI-Zeichenfolgen in Unicode konvertiert, tritt ein Fehler auf, wenn die aktuelle Benutzercodepage nicht mit der Codepage der Datenbank identisch ist.

Durch Aufrufen der ANSI-Version der Windows Installer-API wird die lokalisierte Zeichenfolge mithilfe der aktuellen Systemcodepage in Unicode konvertiert. Wenn für die Datenbank ein Commit ausgeführt wird, wird die Unicode-Zeichenfolge mithilfe der Codepage der Datenbank in ANSI konvertiert. Wenn sich die aktuelle Systemcodepage von der Codepage der lokalisierten Zeichenfolge unterscheidet, kann das Ergebnis ein Datenverlust und eine falsche Zeichenfolgenkonvertierung sein.

Im folgenden Verfahren wird gezeigt, wie Sie die Lokalisierungsdaten speichern.

**So speichern Sie Lokalisierungsdaten**

1.  Legen Sie die Codepage der Datenbank auf die Codepage der lokalisierten Zeichenfolge fest.
2.  Konvertieren Sie die ANSI-Zeichenfolge mithilfe der [**MultiByteToWideChar-Funktion**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) in Unicode, und geben Sie die Codepage der lokalisierten Daten an.
3.  Rufen Sie die Unicode-Version der Windows Installer-API auf, indem Sie die Unicode-Zeichenfolge verwenden, um die lokalisierten Daten hinzuzufügen.
4.  Committen Sie die Lokalisierungsänderungen an der Datenbank mithilfe von [**MsiDatabaseCommit.**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)

Sie können einer Installationsdatenbank auch Lokalisierungsinformationen hinzufügen, indem Sie ASCII-Textarchivdateien importieren und exportieren. Weitere Informationen finden Sie unter [Codepagebehandlung von importierten und exportierten Tabellen.](code-page-handling-of-imported-and-exported-tables.md)

 

 
