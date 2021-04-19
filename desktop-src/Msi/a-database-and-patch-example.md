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
# <a name="a-database-and-patch-example"></a><span data-ttu-id="05070-103">Beispiel für eine Datenbank und ein Patch</span><span class="sxs-lookup"><span data-stu-id="05070-103">A Database and Patch Example</span></span>

<span data-ttu-id="05070-104">Eine Anwendung kann die [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) -Funktion verwenden, um eine neue oder vorhandene Installations Datenbank (MSI-Datei) oder ein Patchpaket (MSP-Datei) zu öffnen. Die Anwendung überprüft den Rückgabewert von **MsiOpenDatabase** , bevor Sie das Daten Bank Handle verwendet.</span><span class="sxs-lookup"><span data-stu-id="05070-104">An application can use the [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) function to open a new or existing installation database (.msi file) or patch package (.msp file.) The application checks the return value of **MsiOpenDatabase** before using the database handle.</span></span>

<span data-ttu-id="05070-105">In den folgenden Beispielen werden die in MSI. h definierten **pmsihandle** -Typvariablen verwendet.</span><span class="sxs-lookup"><span data-stu-id="05070-105">The following examples use the **PMSIHANDLE** type variables defined in msi.h.</span></span> <span data-ttu-id="05070-106">Es wird empfohlen, den **pmsihandle** -Typ zu verwenden, da das Installationsprogramm **pmsihandle** -Objekte schließt, wenn Sie den Gültigkeitsbereich verlassen, während die Anwendung **msihandle** -Objekte durch Aufrufen von [**msiclosehandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle)schließen muss.</span><span class="sxs-lookup"><span data-stu-id="05070-106">It is recommended to use the **PMSIHANDLE** type because the installer closes **PMSIHANDLE** objects as they go out of scope, whereas your application must close **MSIHANDLE** objects by calling [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle).</span></span> <span data-ttu-id="05070-107">Weitere Informationen finden Sie im Abschnitt [Verwenden von pmsihandle anstelle eines Handles](windows-installer-best-practices.md) in den [Windows Installer bewährten Methoden](windows-installer-best-practices.md).</span><span class="sxs-lookup"><span data-stu-id="05070-107">For more information see [Use PMSIHANDLE instead of HANDLE](windows-installer-best-practices.md) section in the [Windows Installer Best Practices](windows-installer-best-practices.md).</span></span>

<span data-ttu-id="05070-108">Im folgenden Beispiel wird eine-Datenbank sample.msi zum Lesen geöffnet.</span><span class="sxs-lookup"><span data-stu-id="05070-108">The following example opens a database, sample.msi, for reading only.</span></span> <span data-ttu-id="05070-109">[**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) ist nur erfolgreich, wenn sample.msi im Verzeichnis c: Test vorhanden ist \\ .</span><span class="sxs-lookup"><span data-stu-id="05070-109">[**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) succeeds only if sample.msi exists in the c:\\test directory.</span></span> <span data-ttu-id="05070-110">Bei erfolgreicher Ausführung kann das zurückgegebene Daten Bank Handle verwendet werden, um die Daten im Installationspaket mithilfe von " [**msidatabaseopenview**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) " und " [**msigetsummaryinformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa)" abzufragen.</span><span class="sxs-lookup"><span data-stu-id="05070-110">Upon success, the returned database handle can be used to query the data in the installation package using [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) and [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa).</span></span>


```C++
PMSIHANDLE hDbReadOnly = 0;
UINT uiStatus1 = MsiOpenDatabase(TEXT("c:\\test\\sample.msi"), MSIDBOPEN_READONLY, &hDbReadOnly);
if (ERROR_SUCCESS != uiStatus1)
{
    // process error
    return uiStatus1;
}
```



<span data-ttu-id="05070-111">Im folgenden Beispiel wird die Datenbank zum Lesen und Schreiben geöffnet.</span><span class="sxs-lookup"><span data-stu-id="05070-111">The following example opens the database for reading and writing.</span></span> <span data-ttu-id="05070-112">Wenn die Anwendung [**msidatabasecommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)aufruft, werden alle an der Datenbank vorgenommenen Änderungen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="05070-112">If the application calls [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit), all changes made to the database are saved.</span></span> <span data-ttu-id="05070-113">Wenn die Anwendung nicht **msidatabasecommit** aufruft, werden keine Änderungen an der Datenbank vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="05070-113">If the application does not call **MsiDatabaseCommit**, no changes are made to the database.</span></span>


```C++
PMSIHANDLE hDbTransact = 0;
UINT uiStatus2 = MsiOpenDatabase(TEXT("c:\\test\\example.msi"), MSIDBOPEN_TRANSACT, &hDbTransact);
if (ERROR_SUCCESS != uiStatus2)
{
    // process error
    return uiStatus2;
}
```



<span data-ttu-id="05070-114">Im folgenden Beispiel wird eine vorhandene Datenbank, text.msi, erstellt und eine neue Datenbank erstellt newtest.msi.</span><span class="sxs-lookup"><span data-stu-id="05070-114">The following example takes an existing database, text.msi, and creates a new database, newtest.msi.</span></span> <span data-ttu-id="05070-115">Alle Änderungen, die vorgenommen werden, können durch Aufrufen von [**msidatabasecommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)in der neuen Datenbank gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="05070-115">Any changes that are made can be saved in the new database by calling [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span></span> <span data-ttu-id="05070-116">Die im *szdatabasepath* -Parameter angegebene vorhandene Datenbank ist unverändert.</span><span class="sxs-lookup"><span data-stu-id="05070-116">The existing database specified in the *szDatabasePath* parameter is unchanged.</span></span>


```C++
PMSIHANDLE hDbOutput = 0;
UINT uiStatus3 = MsiOpenDatabase(TEXT("c:\\test\\test.msi"), TEXT("c:\\test\\newtest.msi"), &hDbOutput);
if (ERROR_SUCCESS != uiStatus3)
{
    // process error
    return uiStatus3;
}
```



<span data-ttu-id="05070-117">Im folgenden Beispiel wird ein Windows Installer Patchpaket (MSP-Datei) nur zum Lesen geöffnet.</span><span class="sxs-lookup"><span data-stu-id="05070-117">The following example opens a Windows Installer patch package (.msp file) for reading only.</span></span> <span data-ttu-id="05070-118">Der zurückgegebene patchhandle kann verwendet werden, um die CAB-und Transformations-substorages zu ermitteln, die durch Abfragen der [ \_ Streams](-streams-table.md) -und [ \_ Storages](-storages-table.md) -Tabellen im Patchpaket enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="05070-118">The returned patch handle can be used to determine the cabinets and transform substorages included in the patch package by queries on the [\_Streams](-streams-table.md) and [\_Storages](-storages-table.md) tables.</span></span>

<span data-ttu-id="05070-119">**Windows Installer 2,0:** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="05070-119">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="05070-120">Ab Windows Installer 3,0 kann die Anwendung die [msipatchsequence-Tabelle](msipatchsequence-table.md) Abfragen, die in einem Patchpaket vorhanden ist, das die neuen patchsequenzierungs Informationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="05070-120">Beginning with Windows Installer 3.0, the application can query the [MsiPatchSequence table](msipatchsequence-table.md) present in a patch package that uses the new patch sequencing information.</span></span>


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



 

 



