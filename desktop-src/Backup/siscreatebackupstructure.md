---
title: Siscreatebackupstructure-Funktion (Sisbkup. h)
description: Erstellt basierend auf den angegebenen Informationen eine SIS-Sicherungs Struktur.
ms.assetid: a8c48961-fa24-4eb6-92cd-1b9bc83cec41
keywords:
- Siscreatebackupstructure-Funktions Sicherung
topic_type:
- apiref
api_name:
- SisCreateBackupStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad432095f9d264e124df1d84070056fc827c625e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475927"
---
# <a name="siscreatebackupstructure-function"></a><span data-ttu-id="45ad5-104">Siscreatebackupstructure-Funktion</span><span class="sxs-lookup"><span data-stu-id="45ad5-104">SisCreateBackupStructure function</span></span>

<span data-ttu-id="45ad5-105">Die Funktion **siscreatebackupstructure** erstellt basierend auf den angegebenen Informationen eine SIS-Sicherungs Struktur.</span><span class="sxs-lookup"><span data-stu-id="45ad5-105">The **SisCreateBackupStructure** function creates a SIS backup structure based on the supplied information.</span></span>

## <a name="syntax"></a><span data-ttu-id="45ad5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="45ad5-106">Syntax</span></span>


```C++
BOOL SisCreateBackupStructure(
  _In_  PWCHAR volumeRoot,
  _Out_ PVOID  *sisBackupStructure,
  _Out_ PWCHAR *commonStoreRootPathname,
  _Out_ PULONG countOfCommonStoreFilesToBackUp,
  _Out_ PWCHAR **commonStoreFilesToBackUp
);
```



## <a name="parameters"></a><span data-ttu-id="45ad5-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="45ad5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45ad5-108">*volumeroot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="45ad5-108">*volumeRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45ad5-109">Der Dateiname des volumestamms ohne nachfolgenden umgekehrten Schrägstrich des zu sichernden Volumes.</span><span class="sxs-lookup"><span data-stu-id="45ad5-109">File name of the volume root, without the trailing backslash, of the volume to be backed up.</span></span> <span data-ttu-id="45ad5-110">Geben Sie z. b. "c:" und nicht "c:" an \\ .</span><span class="sxs-lookup"><span data-stu-id="45ad5-110">For example, specify "C:" and not "C:\\".</span></span>

</dd> <dt>

<span data-ttu-id="45ad5-111">*sisbackupstructure* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="45ad5-111">*sisBackupStructure* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45ad5-112">SIS-Sicherungs Struktur zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="45ad5-112">Returned SIS backup structure.</span></span>

</dd> <dt>

<span data-ttu-id="45ad5-113">*commonstorerootpathname* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="45ad5-113">*commonStoreRootPathname* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45ad5-114">Der voll qualifizierte Pfadname des allgemeinen Speicher des angegebenen Volumes.</span><span class="sxs-lookup"><span data-stu-id="45ad5-114">Fully qualified path name of the specified volume's common store.</span></span> <span data-ttu-id="45ad5-115">Beispiel: "c: \\ SIS Common Store".</span><span class="sxs-lookup"><span data-stu-id="45ad5-115">For example, "c:\\SIS Common Store".</span></span>

</dd> <dt>

<span data-ttu-id="45ad5-116">"count" für " *Anf. commonstorefilestobackup* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="45ad5-116">*countOfCommonStoreFilesToBackUp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45ad5-117">Anzahl der Dateien, die im Parameter " *commonstorefilestobackup* " aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="45ad5-117">Number of files listed in the *commonStoreFilesToBackUp* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="45ad5-118">*commonstorefilestobackup* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="45ad5-118">*commonStoreFilesToBackUp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45ad5-119">Zeiger auf ein Array von Dateinamen, das eine Liste interner Dateien angibt, die von SIS zum Verwalten des angegebenen Volumes verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="45ad5-119">Pointer to an array of file names that specifies a list of internal files used by SIS to manage the specified volume.</span></span> <span data-ttu-id="45ad5-120">Diese Dateien müssen gleichzeitig und auf die gleiche Weise gesichert werden wie die von [ **siscsfilestobackupforlink** angeforderten Dateien des Common Stores.](siscsfilestobackupforlink.md)</span><span class="sxs-lookup"><span data-stu-id="45ad5-120">These files should be backed up at the same time and in the same manner as the common-store files requested by [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45ad5-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="45ad5-121">Return value</span></span>

<span data-ttu-id="45ad5-122">Diese Funktion gibt **true** zurück, wenn Sie erfolgreich abgeschlossen wurde, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="45ad5-122">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="45ad5-123">Aufrufen von [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) zum Abrufen von weiteren Informationen über den Grund, warum der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="45ad5-123">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="45ad5-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="45ad5-124">Remarks</span></span>

<span data-ttu-id="45ad5-125">Diese Funktion erstellt eine SIS-Sicherungs Struktur, die von der SIS Backup-API verwendet wird, um eine Liste der Datei Verknüpfungen auf dem Volume und die ursprünglichen Dateien, auf die die Verknüpfungen verweisen, zu erstellen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="45ad5-125">This function creates a SIS backup structure, which is used by the SIS backup API to create and maintain a list of the file links on the volume and the original files the links point to.</span></span> <span data-ttu-id="45ad5-126">Diese Funktion sollte nur einmal für jedes zu sichernde SIS-fähige Volume aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="45ad5-126">This function should be called only once for each SIS-enabled volume being backed up.</span></span> <span data-ttu-id="45ad5-127">Alle Dateien innerhalb des angegebenen Volumes sollten als Dateien für den gemeinsamen Speicher behandelt und nur gesichert werden, wenn SIS angibt, dass dies der Fall sein sollte.</span><span class="sxs-lookup"><span data-stu-id="45ad5-127">All files within the specified volume should be treated as common-store files and backed up only if SIS indicates that they should.</span></span>

<span data-ttu-id="45ad5-128">Die Parameter " *thestof commonstorefilestobackup* " und " *commonstorefilestobackup* " geben eine Liste der Dateien zurück, die unabhängig von den gesicherten Links gesichert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="45ad5-128">The *countOfCommonStoreFilesToBackUp* and *commonStoreFilesToBackUp* parameters together return a list of files that must be backed up regardless of which links are backed up.</span></span>

<span data-ttu-id="45ad5-129">Wenn der Wert für " *Anf commonstorefilestobackup* " 0 ist, kann " *commonstorefilestobackup* " ein **null** -Zeiger sein.</span><span class="sxs-lookup"><span data-stu-id="45ad5-129">If *countOfCommonStoreFilesToBackUp* is 0, *commonStoreFilesToBackUp* may be a **NULL** pointer.</span></span> <span data-ttu-id="45ad5-130">Der Wert des *commonstorefilestobackup* -Parameters sollte ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="45ad5-130">The value of the *commonStoreFilesToBackUp* parameter should be ignored.</span></span>

<span data-ttu-id="45ad5-131">Nachdem der Sicherungs Vorgang beendet wurde, müssen Sie die Zuordnung des vom *commonstorefilestobackup* -Array von Zeichen folgen verwendeten Speichers durch Aufrufen von [**sisfrealloeredmemory**](sisfreeallocatedmemory.md)aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="45ad5-131">After the backup operation is complete, deallocate the memory used by the *commonStoreFilesToBackUp* array of strings by calling [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="45ad5-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="45ad5-132">Requirements</span></span>



| <span data-ttu-id="45ad5-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="45ad5-133">Requirement</span></span> | <span data-ttu-id="45ad5-134">Wert</span><span class="sxs-lookup"><span data-stu-id="45ad5-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="45ad5-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="45ad5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="45ad5-136">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="45ad5-136">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="45ad5-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="45ad5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="45ad5-138">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="45ad5-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="45ad5-139">Header</span><span class="sxs-lookup"><span data-stu-id="45ad5-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="45ad5-140"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="45ad5-140"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="45ad5-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="45ad5-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="45ad5-142"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="45ad5-142"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="45ad5-143">DLL</span><span class="sxs-lookup"><span data-stu-id="45ad5-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45ad5-144"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45ad5-144"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45ad5-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45ad5-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45ad5-146">**Siscreaterestorestruktur**</span><span class="sxs-lookup"><span data-stu-id="45ad5-146">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> <dt>

[<span data-ttu-id="45ad5-147">**Siscsfilestobackupforlink**</span><span class="sxs-lookup"><span data-stu-id="45ad5-147">**SisCSFilesToBackupForLink**</span></span>](siscsfilestobackupforlink.md)
</dt> <dt>

[<span data-ttu-id="45ad5-148">**Sisfrezuden Speicher**</span><span class="sxs-lookup"><span data-stu-id="45ad5-148">**SisFreeAllocatedMemory**</span></span>](sisfreeallocatedmemory.md)
</dt> </dl>

 

