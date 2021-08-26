---
description: Eine Anwendung kann die MsiOpenDatabase-Funktion verwenden, um eine neue oder vorhandene Installationsdatenbank (.msi-Datei) oder ein Patchpaket (MSP-Datei) zu öffnen. Die Anwendung überprüft den Rückgabewert von MsiOpenDatabase, bevor das Datenbankhandle verwendet wird.
ms.assetid: 54a8d571-ebc3-42d5-bc34-8f29b245b4d8
title: Beispiel für eine Datenbank und einen Patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7de816e471bbc3df4ec2970202130dba79267a06cb872e74734de322cba2d68d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997030"
---
# <a name="a-database-and-patch-example"></a>Beispiel für eine Datenbank und einen Patch

Eine Anwendung kann die [**MsiOpenDatabase-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) verwenden, um eine neue oder vorhandene Installationsdatenbank (.msi-Datei) oder ein Patchpaket (MSP-Datei) zu öffnen. Die Anwendung überprüft den Rückgabewert von **MsiOpenDatabase,** bevor das Datenbankhandle verwendet wird.

In den folgenden Beispielen werden die in msi.h definierten **PMSIHANDLE-Typvariablen** verwendet. Es wird empfohlen, den **PMSIHANDLE-Typ** zu verwenden, da das Installationsprogramm **PMSIHANDLE-Objekte** schließt, wenn sie außerhalb des Gültigkeitsbereichs liegen, während Ihre Anwendung **MSIHANDLE-Objekte** schließen muss, indem [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle)aufgerufen wird. Weitere Informationen finden Sie im Abschnitt [Verwenden von PMSIHANDLE anstelle von HANDLE](windows-installer-best-practices.md) im Windows Installer Best [Practices](windows-installer-best-practices.md).

Im folgenden Beispiel wird eine Datenbank geöffnet, sample.msi, die nur zum Lesen verwendet werden kann. [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) ist nur erfolgreich, wenn sample.msi im Verzeichnis c: test vorhanden \\ ist. Bei Erfolg kann das zurückgegebene Datenbankhandle verwendet werden, um die Daten im Installationspaket mithilfe von [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) und [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa)abzufragen.


```C++
PMSIHANDLE hDbReadOnly = 0;
UINT uiStatus1 = MsiOpenDatabase(TEXT("c:\\test\\sample.msi"), MSIDBOPEN_READONLY, &hDbReadOnly);
if (ERROR_SUCCESS != uiStatus1)
{
    // process error
    return uiStatus1;
}
```



Im folgenden Beispiel wird die Datenbank zum Lesen und Schreiben geöffnet. Wenn die Anwendung [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)aufruft, werden alle an der Datenbank vorgenommenen Änderungen gespeichert. Wenn die Anwendung **MsiDatabaseCommit** nicht aufruft, werden keine Änderungen an der Datenbank vorgenommen.


```C++
PMSIHANDLE hDbTransact = 0;
UINT uiStatus2 = MsiOpenDatabase(TEXT("c:\\test\\example.msi"), MSIDBOPEN_TRANSACT, &hDbTransact);
if (ERROR_SUCCESS != uiStatus2)
{
    // process error
    return uiStatus2;
}
```



Im folgenden Beispiel wird eine vorhandene Datenbank text.msi und eine neue Datenbank erstellt, newtest.msi. Alle vorgenommenen Änderungen können in der neuen Datenbank gespeichert werden, indem [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)aufgerufen wird. Die vorhandene Datenbank, die im *szDatabasePath-Parameter* angegeben ist, bleibt unverändert.


```C++
PMSIHANDLE hDbOutput = 0;
UINT uiStatus3 = MsiOpenDatabase(TEXT("c:\\test\\test.msi"), TEXT("c:\\test\\newtest.msi"), &hDbOutput);
if (ERROR_SUCCESS != uiStatus3)
{
    // process error
    return uiStatus3;
}
```



Im folgenden Beispiel wird ein Windows Installer-Patchpaket (MSP-Datei) nur zum Lesen geöffnet. Das zurückgegebene Patchhandle kann verwendet werden, um die im Patchpaket enthaltenen Unterspeicher zu bestimmen und zu transformieren, indem Abfragen für die Tabellen [ \_ Streams](-streams-table.md) und [ \_ Storages](-storages-table.md) erfolgen.

**Windows Installer 2.0:** Wird nicht unterstützt. Ab Windows Installer 3.0 kann die Anwendung die [MsiPatchSequence-Tabelle](msipatchsequence-table.md) in einem Patchpaket abfragen, das die neuen Informationen zur Patchsequenzierung verwendet.


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



 

 



