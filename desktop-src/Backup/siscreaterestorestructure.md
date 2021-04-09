---
title: Siscreaterestorestruktur-Funktion (Sisbkup. h)
description: Erstellt basierend auf den angegebenen Informationen eine SIS-Wiederherstellungs Struktur.
ms.assetid: acdd4258-813d-42af-a2e1-e59a1426f86c
keywords:
- Siscreaterestorestruktur-Funktions Sicherung
topic_type:
- apiref
api_name:
- SisCreateRestoreStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b83ebcdd609b00fdec19666a6915926692a2048
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858761"
---
# <a name="siscreaterestorestructure-function"></a><span data-ttu-id="681f7-104">Siscreaterestorestruktur-Funktion</span><span class="sxs-lookup"><span data-stu-id="681f7-104">SisCreateRestoreStructure function</span></span>

<span data-ttu-id="681f7-105">Die **siscreaterestorestruktur** -Funktion erstellt basierend auf den angegebenen Informationen eine SIS-Wiederherstellungs Struktur.</span><span class="sxs-lookup"><span data-stu-id="681f7-105">The **SisCreateRestoreStructure** function creates a SIS restore structure based on the supplied information.</span></span>

## <a name="syntax"></a><span data-ttu-id="681f7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="681f7-106">Syntax</span></span>


```C++
BOOL SisCreateRestoreStructure(
  _In_  PWCHAR volumeRoot,
  _Out_ PVOID  *sisRestoreStructure,
  _Out_ PWCHAR *commonStoreRootPathname,
  _Out_ PULONG countOfCommonStoreFilesToRestore,
  _Out_ PWCHAR **commonStoreFilesToRestore
);
```



## <a name="parameters"></a><span data-ttu-id="681f7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="681f7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="681f7-108">*volumeroot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="681f7-108">*volumeRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="681f7-109">Der Dateiname des volumestamms ohne nachfolgenden umgekehrten Schrägstrich des zu sichernden Volumes.</span><span class="sxs-lookup"><span data-stu-id="681f7-109">File name of the volume root, without the trailing backslash, of the volume to be backed up.</span></span> <span data-ttu-id="681f7-110">Geben Sie z. b. "c:" und nicht "c:" an \\ .</span><span class="sxs-lookup"><span data-stu-id="681f7-110">For example, specify "C:" and not "C:\\".</span></span> <span data-ttu-id="681f7-111">Das Volume kann nicht das System-oder Start Volume sein.</span><span class="sxs-lookup"><span data-stu-id="681f7-111">The volume cannot be the system or boot volume.</span></span>

</dd> <dt>

<span data-ttu-id="681f7-112">*sisrestorestruktur* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="681f7-112">*sisRestoreStructure* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="681f7-113">Zurückgegebene SIS-Wiederherstellungs Struktur.</span><span class="sxs-lookup"><span data-stu-id="681f7-113">Returned SIS restore structure.</span></span> <span data-ttu-id="681f7-114">Diese Struktur sollte vom Aufrufer als nicht transparent behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="681f7-114">This structure should be treated as opaque by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="681f7-115">*commonstorerootpathname* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="681f7-115">*commonStoreRootPathname* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="681f7-116">Der voll qualifizierte Pfadname des allgemeinen Speicher des angegebenen Volumes.</span><span class="sxs-lookup"><span data-stu-id="681f7-116">Fully qualified path name of the specified volume's common store.</span></span> <span data-ttu-id="681f7-117">Beispiel: "c: \\ SIS Common Store".</span><span class="sxs-lookup"><span data-stu-id="681f7-117">For example, "c:\\SIS Common Store".</span></span>

</dd> <dt>

<span data-ttu-id="681f7-118">" *frajeficommonstorefilestorestore* \[ " vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="681f7-118">*countOfCommonStoreFilesToRestore* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="681f7-119">Anzahl der Dateien, die im *commonstorefilestorestore* -Parameter aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="681f7-119">Number of files listed in the *commonStoreFilesToRestore* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="681f7-120">*commonstorefilestorestore* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="681f7-120">*commonStoreFilesToRestore* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="681f7-121">Zeiger auf ein Array von Dateinamen, das die Liste der internen Dateien angibt, die von SIS zum Verwalten des angegebenen Volumes verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="681f7-121">Pointer to an array of file names that specifies the list of internal files used by SIS to manage the specified volume.</span></span> <span data-ttu-id="681f7-122">Diese Dateien müssen gleichzeitig und auf die gleiche Weise wieder hergestellt werden wie die von [**siscsfilestobackupforlink**](siscsfilestobackupforlink.md)angeforderten Dateien des Common Stores.</span><span class="sxs-lookup"><span data-stu-id="681f7-122">These files should be restored at the same time and in the same manner as the common-store files requested by [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="681f7-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="681f7-123">Return value</span></span>

<span data-ttu-id="681f7-124">Diese Funktion gibt **true** zurück, wenn Sie erfolgreich abgeschlossen wurde, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="681f7-124">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="681f7-125">Aufrufen von [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) zum Abrufen von weiteren Informationen über den Grund, warum der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="681f7-125">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="681f7-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="681f7-126">Remarks</span></span>

<span data-ttu-id="681f7-127">Diese Funktion legt die Wiederherstellungs Umgebung auf dem angegebenen Volume so fest, wie [**siscreatebackupstructure**](siscreatebackupstructure.md) die Sicherungs Umgebung auf dem angegebenen Volume festlegt.</span><span class="sxs-lookup"><span data-stu-id="681f7-127">This function establishes the restore environment on the specified volume in the way that [**SisCreateBackupStructure**](siscreatebackupstructure.md) establishes the backup environment on the specified volume.</span></span>

<span data-ttu-id="681f7-128">Beachten Sie, dass diese Funktion nicht notwendigerweise die Common-Store-Datei oder die Dateien identifiziert, die einem Satz von SIS-Links auf dem Sicherungsmedium entsprechen, wenn diese gemeinsamen Speicherdateien oder Dateien noch auf dem Datenträger vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="681f7-128">Note that this function will not necessarily identify the common-store file or files corresponding to a set of SIS links on the backup media if those common store file or files still exist on disk.</span></span> <span data-ttu-id="681f7-129">Der Inhalt des Datenstroms einer Datei der Common Store-Datei ändert sich nie, nachdem Sie erstellt wurde. wenn die Datei auf dem Datenträger bereits vorhanden ist, muss Sie daher nicht wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="681f7-129">The contents of a common-store file's data stream never change once it is created, so if the file already exists on the disk there is no need to restore it.</span></span>

<span data-ttu-id="681f7-130">Dateinamen im allgemeinen Speicher sind global eindeutig, um die Integrität des Wiederherstellungs Vorgangs zu gewährleisten, auch wenn er nicht auf dem gleichen SIS-fähigen Volume auftritt, auf das der Sicherungs Vorgang zugegriffen hat.</span><span class="sxs-lookup"><span data-stu-id="681f7-130">Common-store file names are globally unique to ensure the integrity of the restore operation even if it does not occur on the same SIS-enabled volume that the backup operation has accessed.</span></span>

<span data-ttu-id="681f7-131">Nachdem der Wiederherstellungs Vorgang beendet wurde, müssen Sie die Zuordnung des vom *commonstorefilestorestore* -Array von Zeichen folgen verwendeten Speichers durch Aufrufen von [**sisfrealloeredmemory**](sisfreeallocatedmemory.md)aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="681f7-131">After the restore operation is complete, deallocate the memory used by the *commonStoreFilesToRestore* array of strings by calling [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="681f7-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="681f7-132">Requirements</span></span>



| <span data-ttu-id="681f7-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="681f7-133">Requirement</span></span> | <span data-ttu-id="681f7-134">Wert</span><span class="sxs-lookup"><span data-stu-id="681f7-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="681f7-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="681f7-135">Minimum supported client</span></span><br/> | <span data-ttu-id="681f7-136">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="681f7-136">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="681f7-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="681f7-137">Minimum supported server</span></span><br/> | <span data-ttu-id="681f7-138">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="681f7-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="681f7-139">Header</span><span class="sxs-lookup"><span data-stu-id="681f7-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="681f7-140"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="681f7-140"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="681f7-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="681f7-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="681f7-142"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="681f7-142"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="681f7-143">DLL</span><span class="sxs-lookup"><span data-stu-id="681f7-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="681f7-144"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="681f7-144"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="681f7-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="681f7-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="681f7-146">**Siscreatebackupstructure**</span><span class="sxs-lookup"><span data-stu-id="681f7-146">**SisCreateBackupStructure**</span></span>](siscreatebackupstructure.md)
</dt> <dt>

[<span data-ttu-id="681f7-147">**Siscsfilestobackupforlink**</span><span class="sxs-lookup"><span data-stu-id="681f7-147">**SisCSFilesToBackupForLink**</span></span>](siscsfilestobackupforlink.md)
</dt> <dt>

[<span data-ttu-id="681f7-148">**Sisfrezuden Speicher**</span><span class="sxs-lookup"><span data-stu-id="681f7-148">**SisFreeAllocatedMemory**</span></span>](sisfreeallocatedmemory.md)
</dt> <dt>

[<span data-ttu-id="681f7-149">**Sisfrebackupstructure**</span><span class="sxs-lookup"><span data-stu-id="681f7-149">**SisFreeBackupStructure**</span></span>](sisfreebackupstructure.md)
</dt> </dl>

 

