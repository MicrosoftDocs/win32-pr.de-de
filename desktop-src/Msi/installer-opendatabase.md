---
description: Die OpenDatabase-Methode des Installer-Objekts öffnet eine vorhandene Datenbank oder erstellt eine neue Datenbank, die ein Datenbankobjekt zurückgibt. Es wird ein Fehler generiert, wenn das Datenbankobjekt nicht erfolgreich erstellt und geöffnet werden kann.
ms.assetid: a77b3954-db27-41a0-8f8b-2654766bde6a
title: Installer. OpenDatabase-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenDatabase
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 13256f0bbe2d5adad61c46ea091e8207f1a9351b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358226"
---
# <a name="installeropendatabase-method"></a><span data-ttu-id="619d0-104">Installer. OpenDatabase-Methode</span><span class="sxs-lookup"><span data-stu-id="619d0-104">Installer.OpenDatabase method</span></span>

<span data-ttu-id="619d0-105">Die **OpenDatabase** -Methode des [**Installer**](installer-object.md) -Objekts öffnet eine vorhandene Datenbank oder erstellt eine neue Datenbank, die ein [**Daten Bank**](database-object.md) Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="619d0-105">The **OpenDatabase** method of the [**Installer**](installer-object.md) object opens an existing database or creates a new one, returning a [**Database**](database-object.md) object.</span></span> <span data-ttu-id="619d0-106">Es wird ein Fehler generiert, wenn das **Daten Bank** Objekt nicht erfolgreich erstellt und geöffnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="619d0-106">It generates an error if the **Database** object cannot be successfully created and opened.</span></span>

## <a name="syntax"></a><span data-ttu-id="619d0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="619d0-107">Syntax</span></span>


```JScript
Installer.OpenDatabase(
  name,
  openMode
)
```



## <a name="parameters"></a><span data-ttu-id="619d0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="619d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="619d0-109">*name*</span><span class="sxs-lookup"><span data-stu-id="619d0-109">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="619d0-110">Erforderliche Zeichenfolge, die den Pfadnamen der Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="619d0-110">Required string that contains the path name of the database.</span></span> <span data-ttu-id="619d0-111">Wenn eine leere Zeichenfolge angegeben wird, wird eine temporäre Datenbank erstellt, die nicht persistent gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="619d0-111">If an empty string is supplied, a temporary database is created that is not persisted.</span></span>

</dd> <dt>

<span data-ttu-id="619d0-112">*openMode*</span><span class="sxs-lookup"><span data-stu-id="619d0-112">*openMode*</span></span> 
</dt> <dd>

<span data-ttu-id="619d0-113">Ein Parameter aus der folgenden Liste oder eine Zeichenfolge, die den Pfadnamen der neuen Ausgabedaten Bank Datei enthält, in die nach dem Commit geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="619d0-113">A parameter from the following list or a string that contains the path name of the new output database file that is to be written to upon commit.</span></span>



| <span data-ttu-id="619d0-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="619d0-114">Parameter</span></span>                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="619d0-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="619d0-115">Meaning</span></span>                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiOpenDatabaseModeReadOnly"></span><span id="msiopendatabasemodereadonly"></span><span id="MSIOPENDATABASEMODEREADONLY"></span><dl> <span data-ttu-id="619d0-116"><dt>**msiopendatabasemodereadonly**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="619d0-116"><dt>**msiOpenDatabaseModeReadOnly**</dt> <dt>0</dt></span></span> </dl>                 | <span data-ttu-id="619d0-117">Öffnet eine schreibgeschützte Datenbank, keine persistenten Änderungen.</span><span class="sxs-lookup"><span data-stu-id="619d0-117">Opens a database read-only, no persistent changes.</span></span><br/>                                                                                                           |
| <span id="msiOpenDatabaseModeTransact"></span><span id="msiopendatabasemodetransact"></span><span id="MSIOPENDATABASEMODETRANSACT"></span><dl> <span data-ttu-id="619d0-118"><dt>**msiopendatabasemodebug**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="619d0-118"><dt>**msiOpenDatabaseModeTransact**</dt> <dt>1</dt></span></span> </dl>                 | <span data-ttu-id="619d0-119">Öffnet einen Lese-/Schreibmodus für die Datenbank im Transaktionsmodus.</span><span class="sxs-lookup"><span data-stu-id="619d0-119">Opens a database read/write in transaction mode.</span></span><br/>                                                                                                             |
| <span id="msiOpenDatabaseModeDirect"></span><span id="msiopendatabasemodedirect"></span><span id="MSIOPENDATABASEMODEDIRECT"></span><dl> <span data-ttu-id="619d0-120"><dt>**msiopendatabasemodebug**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="619d0-120"><dt>**msiOpenDatabaseModeDirect**</dt> <dt>2</dt></span></span> </dl>                         | <span data-ttu-id="619d0-121">Öffnet einen direkten Lese-/Schreibzugriff für die Datenbank ohne Transaktion.</span><span class="sxs-lookup"><span data-stu-id="619d0-121">Opens a database direct read/write without transaction.</span></span><br/>                                                                                                      |
| <span id="msiOpenDatabaseModeCreate"></span><span id="msiopendatabasemodecreate"></span><span id="MSIOPENDATABASEMODECREATE"></span><dl> <span data-ttu-id="619d0-122"><dt>**msiopendatabasemode Create**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="619d0-122"><dt>**msiOpenDatabaseModeCreate**</dt> <dt>3</dt></span></span> </dl>                         | <span data-ttu-id="619d0-123">Erstellt eine neue Datenbank mit Lese-/Schreibzugriff im Transact-Modus.</span><span class="sxs-lookup"><span data-stu-id="619d0-123">Creates a new database, transact mode read/write.</span></span><br/>                                                                                                            |
| <span id="msiOpenDatabaseModeCreateDirect"></span><span id="msiopendatabasemodecreatedirect"></span><span id="MSIOPENDATABASEMODECREATEDIRECT"></span><dl> <span data-ttu-id="619d0-124"><dt>**msiopendatabasemodekreatedirect**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="619d0-124"><dt>**msiOpenDatabaseModeCreateDirect**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="619d0-125">Erstellt eine neue Datenbank mit Lese-/Schreibzugriff im direkten Modus.</span><span class="sxs-lookup"><span data-stu-id="619d0-125">Creates a new database, direct mode read/write.</span></span><br/>                                                                                                              |
| <span id="msiOpenDatabaseModeListScript"></span><span id="msiopendatabasemodelistscript"></span><span id="MSIOPENDATABASEMODELISTSCRIPT"></span><dl> <span data-ttu-id="619d0-126"><dt>**msiopendatabasemodelistscript**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="619d0-126"><dt>**msiOpenDatabaseModeListScript**</dt> <dt>5</dt></span></span> </dl>         | <span data-ttu-id="619d0-127">Öffnet eine Datenbank, um Ankündigungs Skriptdateien anzuzeigen, wie z. b. die Dateien [**, die von der Methode**](installer-createadvertisescript.md) "Methode" generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="619d0-127">Opens a database to view advertise script files, such as the files generated by the [**CreateAdvertiseScript**](installer-createadvertisescript.md) method.</span></span><br/> |
| <span id="msiOpenDatabaseModePatchFile"></span><span id="msiopendatabasemodepatchfile"></span><span id="MSIOPENDATABASEMODEPATCHFILE"></span><dl> <span data-ttu-id="619d0-128"><dt>**msiopendatabasemodepatchfile**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="619d0-128"><dt>**msiOpenDatabaseModePatchFile**</dt> <dt>32</dt></span></span> </dl>            | <span data-ttu-id="619d0-129">Fügt dieses Flag hinzu, um eine Patchdatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="619d0-129">Adds this flag to indicate a patch file.</span></span><br/>                                                                                                                     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="619d0-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="619d0-130">Return value</span></span>

<span data-ttu-id="619d0-131">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="619d0-131">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="619d0-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="619d0-132">Remarks</span></span>

<span data-ttu-id="619d0-133">Wenn eine Datenbank als Ausgabe einer anderen Datenbank geöffnet wird, ist der Zusammenfassungs Datenstrom der Ausgabedatenbank tatsächlich eine schreibgeschützte Spiegelung der ursprünglichen Datenbank und kann daher nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="619d0-133">When a database is opened as the output of another database, the summary information stream of the output database is actually a read-only mirror of the original database and thus cannot be changed.</span></span> <span data-ttu-id="619d0-134">Außerdem wird Sie nicht in der Datenbank gespeichert.</span><span class="sxs-lookup"><span data-stu-id="619d0-134">Additionally, it is not persisted with the database.</span></span> <span data-ttu-id="619d0-135">Um die zusammenfassenden Informationen für die Ausgabedatenbank zu erstellen oder zu ändern, muss sie geschlossen und erneut geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="619d0-135">To create or modify the summary information for the output database it must be closed and reopened.</span></span>

<span data-ttu-id="619d0-136">Zum Erstellen und Speichern von Änderungen an einer Datenbank öffnen Sie zunächst die Datenbank in der Transaktion (msiopendatabasemodetransact), Create (msiopendatabasemodecreate oder msiopendatabasemodekreatedirect) oder Direct (msiopendatabasemodedirect)-Modus.</span><span class="sxs-lookup"><span data-stu-id="619d0-136">To make and save changes to a database first open the database in transaction (msiOpenDatabaseModeTransact), create (msiOpenDatabaseModeCreate or msiOpenDatabaseModeCreateDirect), or direct (msiOpenDatabaseModeDirect) mode.</span></span> <span data-ttu-id="619d0-137">Nachdem Sie die Änderungen vorgenommen haben, sollten Sie vor dem Schließen des Daten Bank Handles immer die [**Commit**](database-commit.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="619d0-137">After making the changes, always call the [**Commit**](database-commit.md) method before closing the database handle.</span></span> <span data-ttu-id="619d0-138">Die **Commit** -Methode leert alle Puffer.</span><span class="sxs-lookup"><span data-stu-id="619d0-138">The **Commit** method flushes all buffers.</span></span>

<span data-ttu-id="619d0-139">Aufrufen Sie immer die [**Commit**](database-commit.md) -Methode für eine Datenbank, die im direkten Modus (msiopendatabasemodedirect oder msiopendatabasemodecreatedirect) geöffnet wurde, bevor Sie die Datenbank schließen.</span><span class="sxs-lookup"><span data-stu-id="619d0-139">Always call the [**Commit**](database-commit.md) method on a database that has been opened in direct mode (msiOpenDatabaseModeDirect or msiOpenDatabaseModeCreateDirect) before closing the database.</span></span> <span data-ttu-id="619d0-140">Wenn dies nicht möglich ist, kann die Datenbank beschädigt werden.</span><span class="sxs-lookup"><span data-stu-id="619d0-140">Failure to do this may corrupt the database.</span></span>

<span data-ttu-id="619d0-141">Da die **OpenDatabase** -Methode den Datenbankzugriff initiiert, kann Sie nicht mit einer laufenden Installation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="619d0-141">Because the **OpenDatabase** method initiates database access, it cannot be used with a running installation.</span></span>

<span data-ttu-id="619d0-142">Wenn die Methode fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="619d0-142">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="619d0-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="619d0-143">Requirements</span></span>



| <span data-ttu-id="619d0-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="619d0-144">Requirement</span></span> | <span data-ttu-id="619d0-145">Wert</span><span class="sxs-lookup"><span data-stu-id="619d0-145">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="619d0-146">Version</span><span class="sxs-lookup"><span data-stu-id="619d0-146">Version</span></span><br/> | <span data-ttu-id="619d0-147">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="619d0-147">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="619d0-148">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="619d0-148">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="619d0-149">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="619d0-149">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="619d0-150">DLL</span><span class="sxs-lookup"><span data-stu-id="619d0-150">DLL</span></span><br/>     | <dl> <span data-ttu-id="619d0-151"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="619d0-151"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="619d0-152">IID</span><span class="sxs-lookup"><span data-stu-id="619d0-152">IID</span></span><br/>     | <span data-ttu-id="619d0-153">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="619d0-153">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




