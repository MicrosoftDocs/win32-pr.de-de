---
title: Sisrestoredlink-Funktion (Sisbkup. h)
description: Gibt die Namen der Datei des Common Stores oder der Dateien zurück, auf die der angegebene wiederhergestellte SIS-Link verweist.
ms.assetid: 4eefd975-6055-44c0-93ab-900638948f3e
keywords:
- Sisrestoredlink-Funktions Sicherung
topic_type:
- apiref
api_name:
- SisRestoredLink
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd539d1ad6c203441b2bcd469a7d8f2fe8bdfc7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949605"
---
# <a name="sisrestoredlink-function"></a><span data-ttu-id="274bd-104">Sisrestoredlink-Funktion</span><span class="sxs-lookup"><span data-stu-id="274bd-104">SisRestoredLink function</span></span>

<span data-ttu-id="274bd-105">Die **sisrestoredlink** -Funktion gibt die Namen der Datei (Common-Store) zurück, auf die durch den angegebenen wiederhergestellten SIS-Link verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="274bd-105">The **SisRestoredLink** function returns the names of the common-store file or files pointed to by the specified restored SIS link.</span></span>

## <a name="syntax"></a><span data-ttu-id="274bd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="274bd-106">Syntax</span></span>


```C++
BOOL SisRestoredLink(
  _In_  PVOID  sisRestoreStructure,
  _In_  PWCHAR restoredFileName,
  _In_  PVOID  reparseData,
  _In_  ULONG  reparseDataSize,
  _Out_ PULONG countOfCommonStoreFilesToRestore,
  _Out_ PWCHAR **commonStoreFilesToRestore
);
```



## <a name="parameters"></a><span data-ttu-id="274bd-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="274bd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="274bd-108">*sisrestorestruktur* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="274bd-108">*sisRestoreStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="274bd-109">Zeiger auf eine SIS-Wiederherstellungs Struktur, die von [**siscreaterestorestruktur**](siscreaterestorestructure.md)zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="274bd-109">Pointer to a SIS restore structure returned from [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span></span>

</dd> <dt>

<span data-ttu-id="274bd-110">*restoredfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="274bd-110">*restoredFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="274bd-111">Der voll qualifizierte Dateiname der wiederhergestellten SIS-Linkdatei.</span><span class="sxs-lookup"><span data-stu-id="274bd-111">Fully qualified file name of the restored SIS link file.</span></span>

</dd> <dt>

<span data-ttu-id="274bd-112">*Analysedaten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="274bd-112">*reparseData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="274bd-113">Zeiger auf den Inhalt des SIS-Analyse Punkts.</span><span class="sxs-lookup"><span data-stu-id="274bd-113">Pointer to the contents of the SIS reparse point.</span></span> <span data-ttu-id="274bd-114">Dieser Analyse Punkt enthält Daten, die den wiederhergestellten SIS-Link beschreiben.</span><span class="sxs-lookup"><span data-stu-id="274bd-114">This reparse point contains data describing the restored SIS link.</span></span> <span data-ttu-id="274bd-115">Um die Analyse Punktdaten für eine Datei abzurufen, verwenden Sie den [**FSCTL \_ Get Analyse \_ \_ Point**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) -Steuerungs Code.</span><span class="sxs-lookup"><span data-stu-id="274bd-115">To retrieve the reparse point data for a file, use the [**FSCTL\_GET\_REPARSE\_POINT**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) control code.</span></span>

</dd> <dt>

<span data-ttu-id="274bd-116">*Analyse DataSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="274bd-116">*reparseDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="274bd-117">Größe des Inhalts des SIS-Analyse Punkts, auf den von Analyse *Daten* verwiesen wird (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="274bd-117">Size of the contents of the SIS reparse point pointed to by *reparseData*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="274bd-118">" *frajeficommonstorefilestorestore* \[ " vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="274bd-118">*countOfCommonStoreFilesToRestore* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="274bd-119">Anzahl der Dateien, die im *commonstorefilestorestore* -Parameter aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="274bd-119">Number of files listed in the *commonStoreFilesToRestore* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="274bd-120">*commonstorefilestorestore* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="274bd-120">*commonStoreFilesToRestore* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="274bd-121">Zeiger auf ein Array von Dateinamen im allgemeinen Speicher.</span><span class="sxs-lookup"><span data-stu-id="274bd-121">Pointer to an array of common-store file names.</span></span> <span data-ttu-id="274bd-122">Diese Dateien müssen gleichzeitig und auf die gleiche Weise wieder hergestellt werden wie die von [**siscsfilestobackupforlink**](siscsfilestobackupforlink.md)angeforderten Dateien des Common Stores.</span><span class="sxs-lookup"><span data-stu-id="274bd-122">These files should be restored at the same time and in the same manner as the common-store files requested by [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).</span></span>

<span data-ttu-id="274bd-123">Wenn der Wert des Parameters " *thestofcommonstorefilestorestore* " nicht 0 ist, enthält der Wert des Parameters " *commonstorefilestorestore* " die Namen der Dateien, die als Ergebnis der Wiederherstellung des SIS-Links wieder hergestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="274bd-123">If the value of the *countOfCommonStoreFilesToRestore* parameter is not 0, the value of the *commonStoreFilesToRestore* parameter will contain the names of the common-store files to be restored as a result of restoring the SIS link.</span></span> <span data-ttu-id="274bd-124">Wenn der Wert 0 ist, wurden entweder die Dateien des Common Stores einmal zurückgegeben, oder Sie sind bereits auf dem Volume vorhanden.</span><span class="sxs-lookup"><span data-stu-id="274bd-124">If the value is 0, then either the common-store files have been returned once, or they are already present on the volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="274bd-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="274bd-125">Return value</span></span>

<span data-ttu-id="274bd-126">Diese Funktion gibt **true** zurück, wenn Sie erfolgreich abgeschlossen wurde, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="274bd-126">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="274bd-127">Aufrufen von [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) zum Abrufen von weiteren Informationen über den Grund, warum der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="274bd-127">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="274bd-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="274bd-128">Remarks</span></span>

<span data-ttu-id="274bd-129">Diese Funktion sollte für jeden SIS-Link aufgerufen werden, der wieder hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="274bd-129">You should call this function for each SIS link that has been restored.</span></span>

<span data-ttu-id="274bd-130">Diese Funktion gibt für jeden Wiederherstellungs Vorgang höchstens einmal jede Common-Store-Datei zurück. Jeder Versuch, zusätzliche SIS-Links wiederherzustellen, die dieselbe Common-Store-Datei sehen, führt nicht dazu, dass der Name der Common Store-Datei zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="274bd-130">This function will return each common-store file at most once for each restore operation; any attempt to restore additional SIS links that see the same common-store file will not result in that common-store file name being returned.</span></span>

<span data-ttu-id="274bd-131">Diese Funktion gibt keine Common-Store-Datei zurück, die während des Sicherungs Vorgangs nicht auch in einem aufzurufenden [**siscsfilestobackupforlink**](siscsfilestobackupforlink.md) -Vorgang zurückgegeben wurde. dabei wird davon ausgegangen, dass die auf dem Medium gespeicherten SIS-Analysedaten nicht beschädigt wurden.</span><span class="sxs-lookup"><span data-stu-id="274bd-131">This function will not return a common-store file that was not also returned in a call to [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md) during the backup operation, assuming that the SIS reparse data stored on the media has not been corrupted.</span></span>

<span data-ttu-id="274bd-132">Beim Wiederherstellen eines SIS-Links sollte der Wiederherstellungs Vorgang nur die entsprechende sparsedatei erstellen, zugeordnete Bereiche initialisieren und dann die SIS-Analysedaten genau so schreiben, wie Sie während des Sicherungs Vorgangs gelesen wurden.</span><span class="sxs-lookup"><span data-stu-id="274bd-132">When restoring a SIS link, your restore operation should create only the appropriate sparse file, initialize any allocated ranges, and then write the SIS reparse data exactly as it was read during the backup operation.</span></span> <span data-ttu-id="274bd-133">Es ist von entscheidender Bedeutung, dass der Wiederherstellungs Vorgang sparsesdateien mit nicht zugeordneten Bereichen anstelle von Dateien mit geringer Dichte (oder Dateien, die nicht mit geringer Dichte) initialisiert wurden, erstellt</span><span class="sxs-lookup"><span data-stu-id="274bd-133">It is crucial that your restore operation create sparse files with unallocated ranges rather than sparse files (or nonsparse files) initialized with zeroes.</span></span>

<span data-ttu-id="274bd-134">Beachten Sie, dass diese Funktion nicht notwendigerweise die Common-Store-Datei oder die Dateien identifiziert, die einem Satz von SIS-Links auf dem Sicherungsmedium entsprechen, wenn diese Datei oder Dateien auf dem Datenträger noch vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="274bd-134">Note that this function will not necessarily identify the common-store file or files corresponding to a set of SIS links on the backup media if those common-store file or files still exist on disk.</span></span> <span data-ttu-id="274bd-135">Der Inhalt des Datenstroms einer Datei der Common Store-Datei ändert sich nie, nachdem Sie erstellt wurde. wenn die Datei auf dem Datenträger bereits vorhanden ist, muss Sie daher nicht wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="274bd-135">The contents of a common-store file's data stream never changes once it is created, so if the file already exists on the disk there is no need to restore it.</span></span>

<span data-ttu-id="274bd-136">Dateinamen im allgemeinen Speicher sind global eindeutig, um die Integrität des Wiederherstellungs Vorgangs zu gewährleisten, auch wenn er nicht auf dem gleichen SIS-fähigen Volume auftritt, auf das der Sicherungs Vorgang zugegriffen hat.</span><span class="sxs-lookup"><span data-stu-id="274bd-136">Common-store file names are globally unique to ensure the integrity of the restore operation even if it does not occur on the same SIS-enabled volume that the backup operation has accessed.</span></span>

## <a name="requirements"></a><span data-ttu-id="274bd-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="274bd-137">Requirements</span></span>



| <span data-ttu-id="274bd-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="274bd-138">Requirement</span></span> | <span data-ttu-id="274bd-139">Wert</span><span class="sxs-lookup"><span data-stu-id="274bd-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="274bd-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="274bd-140">Minimum supported client</span></span><br/> | <span data-ttu-id="274bd-141">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="274bd-141">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="274bd-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="274bd-142">Minimum supported server</span></span><br/> | <span data-ttu-id="274bd-143">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="274bd-143">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="274bd-144">Header</span><span class="sxs-lookup"><span data-stu-id="274bd-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="274bd-145"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="274bd-145"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="274bd-146">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="274bd-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="274bd-147"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="274bd-147"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="274bd-148">DLL</span><span class="sxs-lookup"><span data-stu-id="274bd-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="274bd-149"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="274bd-149"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="274bd-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="274bd-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="274bd-151">**Siscreaterestorestruktur**</span><span class="sxs-lookup"><span data-stu-id="274bd-151">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> <dt>

[<span data-ttu-id="274bd-152">**Siscsfilestobackupforlink**</span><span class="sxs-lookup"><span data-stu-id="274bd-152">**SisCSFilesToBackupForLink**</span></span>](siscsfilestobackupforlink.md)
</dt> </dl>

 

