---
description: Eine Anwendung kann die MsiOpenDatabase-Funktion verwenden, um eine neue oder vorhandene Installations Datenbank (MSI-Datei) oder ein Patchpaket (MSP-Datei) zu öffnen. Die Anwendung überprüft den Rückgabewert von MsiOpenDatabase, bevor Sie das Daten Bank Handle verwendet.
ms.assetid: 54a8d571-ebc3-42d5-bc34-8f29b245b4d8
title: Beispiel für eine Datenbank und ein Patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07ff5925fc409352b4c9ed8c1762ba1ad17b261f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349369"
---
# <a name="a-database-and-patch-example"></a>Beispiel für eine Datenbank und ein Patch

Eine Anwendung kann die [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) -Funktion verwenden, um eine neue oder vorhandene Installations Datenbank (MSI-Datei) oder ein Patchpaket (MSP-Datei) zu öffnen. Die Anwendung überprüft den Rückgabewert von **MsiOpenDatabase** , bevor Sie das Daten Bank Handle verwendet.

In den folgenden Beispielen werden die in MSI. h definierten **pmsihandle** -Typvariablen verwendet. Es wird empfohlen, den **pmsihandle** -Typ zu verwenden, da das Installationsprogramm **pmsihandle** -Objekte schließt, wenn Sie den Gültigkeitsbereich verlassen, während die Anwendung **msihandle** -Objekte durch Aufrufen von [**msiclosehandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle)schließen muss. Weitere Informationen finden Sie im Abschnitt [Verwenden von pmsihandle anstelle eines Handles](windows-installer-best-practices.md) in den [Windows Installer bewährten Methoden](windows-installer-best-practices.md).

Im folgenden Beispiel wird eine-Datenbank sample.msi zum Lesen geöffnet. [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) ist nur erfolgreich, wenn sample.msi im Verzeichnis c: Test vorhanden ist \\ . Bei erfolgreicher Ausführung kann das zurückgegebene Daten Bank Handle verwendet werden, um die Daten im Installationspaket mithilfe von " [**msidatabaseopenview**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) " und " [**msigetsummaryinformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa)" abzufragen.


```C++
PMSIHANDLE hDbReadOnly = 0;
UINT uiStatus1 = MsiOpenDatabase(TEXT("c:\\test\\sample.msi"), MSIDBOPEN_READONLY, &hDbReadOnly);
if (ERROR_SUCCESS != uiStatus1)
{
    // process error
    return uiStatus1;
}
```



Im folgenden Beispiel wird die Datenbank zum Lesen und Schreiben geöffnet. Wenn die Anwendung [**msidatabasecommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)aufruft, werden alle an der Datenbank vorgenommenen Änderungen gespeichert. Wenn die Anwendung nicht **msidatabasecommit** aufruft, werden keine Änderungen an der Datenbank vorgenommen.


```C++
PMSIHANDLE hDbTransact = 0;
UINT uiStatus2 = MsiOpenDatabase(TEXT("c:\\test\\example.msi"), MSIDBOPEN_TRANSACT, &hDbTransact);
if (ERROR_SUCCESS != uiStatus2)
{
    // process error
    return uiStatus2;
}
```



Im folgenden Beispiel wird eine vorhandene Datenbank, text.msi, erstellt und eine neue Datenbank erstellt newtest.msi. Alle Änderungen, die vorgenommen werden, können durch Aufrufen von [**msidatabasecommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)in der neuen Datenbank gespeichert werden. Die im *szdatabasepath* -Parameter angegebene vorhandene Datenbank ist unverändert.


```C++
PMSIHANDLE hDbOutput = 0;
UINT uiStatus3 = MsiOpenDatabase(TEXT("c:\\test\\test.msi"), TEXT("c:\\test\\newtest.msi"), &hDbOutput);
if (ERROR_SUCCESS != uiStatus3)
{
    // process error
    return uiStatus3;
}
```



Im folgenden Beispiel wird ein Windows Installer Patchpaket (MSP-Datei) nur zum Lesen geöffnet. Der zurückgegebene patchhandle kann verwendet werden, um die CAB-und Transformations-substorages zu ermitteln, die durch Abfragen der [ \_ Streams](-streams-table.md) -und [ \_ Storages](-storages-table.md) -Tabellen im Patchpaket enthalten sind.

**Windows Installer 2,0:** Nicht unterstützt. Ab Windows Installer 3,0 kann die Anwendung die [msipatchsequence-Tabelle](msipatchsequence-table.md) Abfragen, die in einem Patchpaket vorhanden ist, das die neuen patchsequenzierungs Informationen verwendet.


```C++
PMSIHANDLE hDbPatch = 0;
LPCTSTR szPersistMode = MSIDBOPEN_READONLY + MSIDBOPEN_PATCHFILE;
UINT uiStatus4 = MsiOpenDatabase(TEXT("c:\\test\\sample.msp"), szPersistMode, &hDbPatch);
if (ERROR_SUCCESS != uiStatus4)
{
    // process error
    return uiStatus4;
}
```



 

 



