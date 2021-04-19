---
description: Die OpenDatabase-Methode des Installer-Objekts öffnet eine vorhandene Datenbank oder erstellt eine neue Datenbank und gibt ein Database-Objekt zurück. Es wird ein Fehler generiert, wenn das Database-Objekt nicht erfolgreich erstellt und geöffnet werden kann.
ms.assetid: a77b3954-db27-41a0-8f8b-2654766bde6a
title: Installer.OpenDatabase-Methode
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
ms.openlocfilehash: 897e683fd56ce3e7496dd945ee068a9e6f0c0f77
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107492269"
---
# <a name="installeropendatabase-method"></a><span data-ttu-id="13442-104">Installer.OpenDatabase-Methode</span><span class="sxs-lookup"><span data-stu-id="13442-104">Installer.OpenDatabase method</span></span>

<span data-ttu-id="13442-105">Die **OpenDatabase-Methode** des [**Installer-Objekts**](installer-object.md) öffnet eine vorhandene Datenbank oder erstellt eine neue Datenbank und gibt ein [**Database-Objekt**](database-object.md) zurück.</span><span class="sxs-lookup"><span data-stu-id="13442-105">The **OpenDatabase** method of the [**Installer**](installer-object.md) object opens an existing database or creates a new one, returning a [**Database**](database-object.md) object.</span></span> <span data-ttu-id="13442-106">Es wird ein Fehler generiert, wenn das **Database-Objekt** nicht erfolgreich erstellt und geöffnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="13442-106">It generates an error if the **Database** object cannot be successfully created and opened.</span></span>

## <a name="syntax"></a><span data-ttu-id="13442-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="13442-107">Syntax</span></span>


```JScript
Installer.OpenDatabase(
  name,
  openMode
)
```



## <a name="parameters"></a><span data-ttu-id="13442-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="13442-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13442-109">*name*</span><span class="sxs-lookup"><span data-stu-id="13442-109">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="13442-110">Erforderliche Zeichenfolge, die den Pfadnamen der Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="13442-110">Required string that contains the path name of the database.</span></span> <span data-ttu-id="13442-111">Wenn eine leere Zeichenfolge angegeben wird, wird eine temporäre Datenbank erstellt, die nicht beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="13442-111">If an empty string is supplied, a temporary database is created that is not persisted.</span></span>

</dd> <dt>

<span data-ttu-id="13442-112">*Openmode*</span><span class="sxs-lookup"><span data-stu-id="13442-112">*openMode*</span></span> 
</dt> <dd>

<span data-ttu-id="13442-113">Ein Parameter aus der folgenden Liste oder eine Zeichenfolge, die den Pfadnamen der neuen Ausgabedatenbankdatei enthält, in die beim Commit geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="13442-113">A parameter from the following list or a string that contains the path name of the new output database file that is to be written to upon commit.</span></span>



| <span data-ttu-id="13442-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="13442-114">Parameter</span></span>                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="13442-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="13442-115">Meaning</span></span>                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiOpenDatabaseModeReadOnly"></span><span id="msiopendatabasemodereadonly"></span><span id="MSIOPENDATABASEMODEREADONLY"></span><dl> <span data-ttu-id="13442-116"><dt>**msiOpenDatabaseModeReadOnly**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="13442-116"><dt>**msiOpenDatabaseModeReadOnly**</dt> <dt>0</dt></span></span> </dl>                 | <span data-ttu-id="13442-117">Öffnet eine schreibgeschützte Datenbank ohne permanente Änderungen.</span><span class="sxs-lookup"><span data-stu-id="13442-117">Opens a database read-only, no persistent changes.</span></span><br/>                                                                                                           |
| <span id="msiOpenDatabaseModeTransact"></span><span id="msiopendatabasemodetransact"></span><span id="MSIOPENDATABASEMODETRANSACT"></span><dl> <span data-ttu-id="13442-118"><dt>**msiOpenDatabaseModeTransact**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="13442-118"><dt>**msiOpenDatabaseModeTransact**</dt> <dt>1</dt></span></span> </dl>                 | <span data-ttu-id="13442-119">Öffnet eine Datenbank mit Lese-/Schreibzugriff im Transaktionsmodus.</span><span class="sxs-lookup"><span data-stu-id="13442-119">Opens a database read/write in transaction mode.</span></span><br/>                                                                                                             |
| <span id="msiOpenDatabaseModeDirect"></span><span id="msiopendatabasemodedirect"></span><span id="MSIOPENDATABASEMODEDIRECT"></span><dl> <span data-ttu-id="13442-120"><dt>**msiOpenDatabaseModeDirect**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="13442-120"><dt>**msiOpenDatabaseModeDirect**</dt> <dt>2</dt></span></span> </dl>                         | <span data-ttu-id="13442-121">Öffnet eine Datenbank mit direktem Lese-/Schreibzugriff ohne Transaktion.</span><span class="sxs-lookup"><span data-stu-id="13442-121">Opens a database direct read/write without transaction.</span></span><br/>                                                                                                      |
| <span id="msiOpenDatabaseModeCreate"></span><span id="msiopendatabasemodecreate"></span><span id="MSIOPENDATABASEMODECREATE"></span><dl> <span data-ttu-id="13442-122"><dt>**msiOpenDatabaseModeCreate**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="13442-122"><dt>**msiOpenDatabaseModeCreate**</dt> <dt>3</dt></span></span> </dl>                         | <span data-ttu-id="13442-123">Erstellt eine neue Datenbank im Transact-Modus mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="13442-123">Creates a new database, transact mode read/write.</span></span><br/>                                                                                                            |
| <span id="msiOpenDatabaseModeCreateDirect"></span><span id="msiopendatabasemodecreatedirect"></span><span id="MSIOPENDATABASEMODECREATEDIRECT"></span><dl> <span data-ttu-id="13442-124"><dt>**msiOpenDatabaseModeCreateDirect**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="13442-124"><dt>**msiOpenDatabaseModeCreateDirect**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="13442-125">Erstellt eine neue Datenbank mit Lese-/Schreibzugriff im direkten Modus.</span><span class="sxs-lookup"><span data-stu-id="13442-125">Creates a new database, direct mode read/write.</span></span><br/>                                                                                                              |
| <span id="msiOpenDatabaseModeListScript"></span><span id="msiopendatabasemodelistscript"></span><span id="MSIOPENDATABASEMODELISTSCRIPT"></span><dl> <span data-ttu-id="13442-126"><dt>**msiOpenDatabaseModeListScript**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="13442-126"><dt>**msiOpenDatabaseModeListScript**</dt> <dt>5</dt></span></span> </dl>         | <span data-ttu-id="13442-127">Öffnet eine Datenbank zum Anzeigen von Ankündigen von Skriptdateien, z. B. die von der [**CreateAdvertiseScript-Methode**](installer-createadvertisescript.md) generierten Dateien.</span><span class="sxs-lookup"><span data-stu-id="13442-127">Opens a database to view advertise script files, such as the files generated by the [**CreateAdvertiseScript**](installer-createadvertisescript.md) method.</span></span><br/> |
| <span id="msiOpenDatabaseModePatchFile"></span><span id="msiopendatabasemodepatchfile"></span><span id="MSIOPENDATABASEMODEPATCHFILE"></span><dl> <span data-ttu-id="13442-128"><dt>**msiOpenDatabaseModePatchFile**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="13442-128"><dt>**msiOpenDatabaseModePatchFile**</dt> <dt>32</dt></span></span> </dl>            | <span data-ttu-id="13442-129">Fügt dieses Flag hinzu, um eine Patchdatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="13442-129">Adds this flag to indicate a patch file.</span></span><br/>                                                                                                                     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13442-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13442-130">Return value</span></span>

<span data-ttu-id="13442-131">Ein [**Database-Objekt,**](database-object.md) das die vorhandene oder neue Installationsdatenbank darstellt, die geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="13442-131">A [**Database**](database-object.md) object that represents the existing or new installer database that was opened.</span></span>

## <a name="remarks"></a><span data-ttu-id="13442-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13442-132">Remarks</span></span>

<span data-ttu-id="13442-133">Wenn eine Datenbank als Ausgabe einer anderen Datenbank geöffnet wird, ist der Zusammenfassungsinformationsdatenstrom der Ausgabedatenbank tatsächlich eine schreibgeschützte Spiegelung der ursprünglichen Datenbank und kann daher nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="13442-133">When a database is opened as the output of another database, the summary information stream of the output database is actually a read-only mirror of the original database and thus cannot be changed.</span></span> <span data-ttu-id="13442-134">Darüber hinaus wird sie nicht in der Datenbank beibehalten.</span><span class="sxs-lookup"><span data-stu-id="13442-134">Additionally, it is not persisted with the database.</span></span> <span data-ttu-id="13442-135">Um die Zusammenfassungsinformationen für die Ausgabedatenbank zu erstellen oder zu ändern, müssen sie geschlossen und erneut geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="13442-135">To create or modify the summary information for the output database it must be closed and reopened.</span></span>

<span data-ttu-id="13442-136">Um Änderungen an einer Datenbank vorzunehmen und zu speichern, öffnen Sie zuerst die Datenbank in der Transaktion (msiOpenDatabaseModeTransact), erstellen (msiOpenDatabaseModeCreate oder msiOpenDatabaseModeCreateDirect) oder den direkten Modus (msiOpenDatabaseModeDirect).</span><span class="sxs-lookup"><span data-stu-id="13442-136">To make and save changes to a database first open the database in transaction (msiOpenDatabaseModeTransact), create (msiOpenDatabaseModeCreate or msiOpenDatabaseModeCreateDirect), or direct (msiOpenDatabaseModeDirect) mode.</span></span> <span data-ttu-id="13442-137">Rufen Sie nach dem Vornehmen der Änderungen immer die [**Commit-Methode**](database-commit.md) auf, bevor Sie das Datenbankhandle schließen.</span><span class="sxs-lookup"><span data-stu-id="13442-137">After making the changes, always call the [**Commit**](database-commit.md) method before closing the database handle.</span></span> <span data-ttu-id="13442-138">Die **Commit-Methode** leert alle Puffer.</span><span class="sxs-lookup"><span data-stu-id="13442-138">The **Commit** method flushes all buffers.</span></span>

<span data-ttu-id="13442-139">Rufen Sie immer die [**Commit-Methode**](database-commit.md) für eine Datenbank auf, die im direkten Modus geöffnet wurde (msiOpenDatabaseModeDirect oder msiOpenDatabaseModeCreateDirect), bevor Sie die Datenbank schließen.</span><span class="sxs-lookup"><span data-stu-id="13442-139">Always call the [**Commit**](database-commit.md) method on a database that has been opened in direct mode (msiOpenDatabaseModeDirect or msiOpenDatabaseModeCreateDirect) before closing the database.</span></span> <span data-ttu-id="13442-140">Wenn dies nicht geschieht, kann die Datenbank beschädigt werden.</span><span class="sxs-lookup"><span data-stu-id="13442-140">Failure to do this may corrupt the database.</span></span>

<span data-ttu-id="13442-141">Da die **OpenDatabase-Methode** den Datenbankzugriff initiiert, kann sie nicht mit einer ausgeführten Installation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="13442-141">Because the **OpenDatabase** method initiates database access, it cannot be used with a running installation.</span></span>

<span data-ttu-id="13442-142">Wenn die Methode fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**LastErrorRecord-Methode**](installer-lasterrorrecord.md) abrufen.</span><span class="sxs-lookup"><span data-stu-id="13442-142">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="13442-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13442-143">Requirements</span></span>



| <span data-ttu-id="13442-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13442-144">Requirement</span></span> | <span data-ttu-id="13442-145">Wert</span><span class="sxs-lookup"><span data-stu-id="13442-145">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13442-146">Version</span><span class="sxs-lookup"><span data-stu-id="13442-146">Version</span></span><br/> | <span data-ttu-id="13442-147">Windows Installer 5.0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="13442-147">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="13442-148">Windows Installer 4.0 oder Windows Installer 4.5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="13442-148">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="13442-149">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="13442-149">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="13442-150">DLL</span><span class="sxs-lookup"><span data-stu-id="13442-150">DLL</span></span><br/>     | <dl> <span data-ttu-id="13442-151"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13442-151"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="13442-152">IID</span><span class="sxs-lookup"><span data-stu-id="13442-152">IID</span></span><br/>     | <span data-ttu-id="13442-153">IID \_ IInstaller ist als 000C1090-0000-0000-C000-0000000000046 definiert.</span><span class="sxs-lookup"><span data-stu-id="13442-153">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




