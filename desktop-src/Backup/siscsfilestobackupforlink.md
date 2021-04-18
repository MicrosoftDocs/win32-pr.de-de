---
title: Siscsfilestobackupforlink-Funktion (Sisbkup. h)
description: Gibt Informationen zurück, die die gemeinsamen Speicherdateien beschreiben, auf die der angegebene SIS-Link verweist.
ms.assetid: 0580c34e-195a-4a2c-893f-bc339dcc88d7
keywords:
- Siscsfilestobackupforlink-Funktions Sicherung
topic_type:
- apiref
api_name:
- SisCSFilesToBackupForLink
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27d4f52728d662f43efed85d662874bd4b008947
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340989"
---
# <a name="siscsfilestobackupforlink-function"></a><span data-ttu-id="ecbe0-104">Siscsfilestobackupforlink-Funktion</span><span class="sxs-lookup"><span data-stu-id="ecbe0-104">SisCSFilesToBackupForLink function</span></span>

<span data-ttu-id="ecbe0-105">Die **siscsfilestobackupforlink** -Funktion gibt Informationen zurück, die die gemeinsamen Speicherdateien beschreiben, auf die der angegebene SIS-Link verweist.</span><span class="sxs-lookup"><span data-stu-id="ecbe0-105">The **SisCSFilesToBackupForLink** function returns information describing the common-store files the specified SIS link points to.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecbe0-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ecbe0-106">Syntax</span></span>


```C++
BOOL SisCSFilesToBackupForLink(
  _In_  PVOID  sisBackupStructure,
  _In_  PVOID  reparseData,
  _In_  ULONG  reparseDataSize,
  _Out_ PVOID  thisFileContext,
  _Out_ PVOID  *matchingFileContext,
  _Out_ PULONG countOfCommonStoreFilesToBackUp,
  _Out_ PWCHAR **commonStoreFilesToBackUp
);
```



## <a name="parameters"></a><span data-ttu-id="ecbe0-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ecbe0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecbe0-108">*sisbackupstructure* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ecbe0-108">*sisBackupStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecbe0-109">Ein Zeiger auf die SIS-Sicherungs Struktur, die von [**siscreatebackupstructure**](siscreatebackupstructure.md)zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="ecbe0-109">Pointer to the SIS backup structure returned from [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span></span>

</dd> <dt>

<span data-ttu-id="ecbe0-110">*Analysedaten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ecbe0-110">*reparseData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecbe0-111">Zeiger auf den Inhalt des SIS-Analyse Punkts.</span><span class="sxs-lookup"><span data-stu-id="ecbe0-111">Pointer to the contents of the SIS reparse point.</span></span> <span data-ttu-id="ecbe0-112">Dieser Analyse Punkt enthält Daten, die einen SIS-Link beschreiben.</span><span class="sxs-lookup"><span data-stu-id="ecbe0-112">This reparse point contains data describing a SIS link.</span></span> <span data-ttu-id="ecbe0-113">Um die Analyse Punktdaten für eine Datei abzurufen, verwenden Sie den [**FSCTL \_ Get Analyse \_ \_ Point**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) -Steuerungs Code.</span><span class="sxs-lookup"><span data-stu-id="ecbe0-113">To retrieve the reparse point data for a file, use the [**FSCTL\_GET\_REPARSE\_POINT**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) control code.</span></span>

</dd> <dt>

<span data-ttu-id="ecbe0-114">*Analyse DataSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ecbe0-114">*reparseDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecbe0-115">Größe des Inhalts des SIS-Analyse Punkts, auf den von Analyse *Daten* verwiesen wird (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="ecbe0-115">Size of the contents of the SIS reparse point pointed to by *reparseData*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ecbe0-116">*thisfilecontext* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ecbe0-116">*thisFileContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ecbe0-117">Zeiger auf eine von der Sicherungs Anwendung bereitgestellte Kontext Zeichenfolge, die diese Funktion aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="ecbe0-117">Pointer to a context string supplied by the backup application calling this function.</span></span> <span data-ttu-id="ecbe0-118">Der Inhalt dieser Inhalts Zeichenfolge wird von dieser Sicherungs Anwendung vollständig bestimmt und nicht von der SIS-Sicherungs-API interpretiert.</span><span class="sxs-lookup"><span data-stu-id="ecbe0-118">The contents of this content string are entirely determined by this backup application and is not interpreted by the SIS Backup API.</span></span> <span data-ttu-id="ecbe0-119">Dieser Parameter ist optional. Wenn Sie nicht verwendet wird, legen Sie den Wert dieses Parameters auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="ecbe0-119">This parameter is optional; if not used, set the value of this parameter to **NULL**.</span></span> <span data-ttu-id="ecbe0-120">Der Wert dieses Parameters wird in diesem Fall nicht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="ecbe0-120">The value of this parameter will not be processed in this case.</span></span>

</dd> <dt>

<span data-ttu-id="ecbe0-121">*matchingfilecontext* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ecbe0-121">*matchingFileContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ecbe0-122">Doppelter indirekter Zeiger auf die Kontext Zeichenfolge des SIS-Links, der durch die Informationen identifiziert wird, die in den ersten vier Parametern dieser Funktion übermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="ecbe0-122">Doubly-indirect pointer to the context string of the SIS link identified by the information passed in the first four parameters of this function.</span></span> <span data-ttu-id="ecbe0-123">Dieser Parameter ist optional. Wenn keine Kontext Zeichenfolge als Wert des *thisfilecontext* -Parameters angegeben wird, legen Sie den Wert dieses Parameters auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="ecbe0-123">This parameter is optional; if a context string is not provided as the value of the *thisFileContext* parameter, set the value of this parameter to **NULL**.</span></span> <span data-ttu-id="ecbe0-124">Der Wert dieses Parameters wird in diesem Fall nicht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="ecbe0-124">The value of this parameter will not be processed in this case.</span></span>

</dd> <dt>

<span data-ttu-id="ecbe0-125">"count" für " *Anf. commonstorefilestobackup* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ecbe0-125">*countOfCommonStoreFilesToBackUp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ecbe0-126">Anzahl der Dateien, die im Parameter " *commonstorefilestobackup* " aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="ecbe0-126">Number of files listed in the *commonStoreFilesToBackUp* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ecbe0-127">*commonstorefilestobackup* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ecbe0-127">*commonStoreFilesToBackUp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ecbe0-128">Zeiger auf ein Array von Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="ecbe0-128">Pointer to an array of file names.</span></span> <span data-ttu-id="ecbe0-129">Diese Dateien müssen gleichzeitig und auf die gleiche Weise gesichert werden wie die von [**siscreatebackupstructure**](siscreatebackupstructure.md)angeforderten Dateien des Common Stores.</span><span class="sxs-lookup"><span data-stu-id="ecbe0-129">These files should be backed up at the same time and in the same manner as the common-store files requested by [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecbe0-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ecbe0-130">Return value</span></span>

<span data-ttu-id="ecbe0-131">Diese Funktion gibt **true** zurück, wenn Sie erfolgreich abgeschlossen wurde, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="ecbe0-131">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="ecbe0-132">Aufrufen von [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) zum Abrufen von weiteren Informationen über den Grund, warum der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="ecbe0-132">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecbe0-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ecbe0-133">Remarks</span></span>

<span data-ttu-id="ecbe0-134">Die Sicherungs Anwendung sollte diese Funktion für jede zu sichernde SIS-Linkdatei nur einmal aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="ecbe0-134">The backup application should call this function only once for each SIS link file being backed up.</span></span>

<span data-ttu-id="ecbe0-135">Die Sicherungs Anwendung kann einen SIS-Analyse Punkt anhand ihres Tags, e/a- \_ \_ Analyse Tags, identifizieren \_ .</span><span class="sxs-lookup"><span data-stu-id="ecbe0-135">The backup application can identify a SIS reparse point by its tag, IO\_REPARSE\_TAG\_SIS.</span></span> <span data-ttu-id="ecbe0-136">Dieses Tag wird in "Winnt. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="ecbe0-136">This tag is defined in Winnt.h.</span></span>

<span data-ttu-id="ecbe0-137">Wenn dieser Analyse Punkt, der durch den Wert des Parameters " *paramesedata* " identifiziert wird, die erste Instanz einer zu sichernden Datei beschreibt, gibt diese Funktion **null** als Wert des *matchingfilecontext* -Parameters zurück und initialisiert den Wert des *commonstorefilestobackup* -Arrays von Zeichen folgen mit den Namen der zu sichernden Datei im allgemeinen Speicher.</span><span class="sxs-lookup"><span data-stu-id="ecbe0-137">If this reparse point identified by the value of the *reparseData* parameter describes the first instance of a file to be backed up, this function will return **NULL** as the value of the *matchingFileContext* parameter, and initialize the value of the *commonStoreFilesToBackUp* array of strings with the names of the common-store file or files to be backed up.</span></span> <span data-ttu-id="ecbe0-138">Andernfalls legt diese Funktion den Wert des *matchingfilecontext* -Parameters auf die Kontext Zeichenfolge fest, die der ersten Instanz der angegebenen Datei entspricht, und legt den Wert des Parameters " *zähltofcommonstorefilestobackup* " auf "0" fest.</span><span class="sxs-lookup"><span data-stu-id="ecbe0-138">Otherwise, this function will set the value of the *matchingFileContext* parameter to the context string corresponding to the first instance of the specified file and set the value of the *countOfCommonStoreFilesToBackUp* parameter to 0.</span></span> <span data-ttu-id="ecbe0-139">Wenn mehrere Common-Store-Dateien vorhanden sind, die dem angegebenen Link entsprechen, entspricht der Wert des *thisfilecontext* -Parameters der Kontext Zeichenfolge, die der ersten Common-Store-Datei entspricht, die im-Array mit commonstorefilestobackup 0 zurückgegeben wird \[ \] .</span><span class="sxs-lookup"><span data-stu-id="ecbe0-139">If there are multiple common-store files corresponding to the specified link, the value of the *thisFileContext* parameter will be the context string corresponding to the first common-store file returned in the array that is, commonStoreFilesToBackUp\[0\].</span></span>

<span data-ttu-id="ecbe0-140">Die aktuelle Version dieser Funktion gibt höchstens eine Common-Store-Datei zurück. es ist jedoch möglich, dass in zukünftigen Versionen ein einzelner Link durch mehrere Dateien im allgemeinen Speicher gestützt wird, z. b. für jeden Stream in der Datei, damit die Sicherungs Anwendung mehrere Dateien in jedem aufrufungs Vorgang unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ecbe0-140">The current version of this function will return at most one common-store file, but it is possible that in future versions a single link may be backed by several common-store files for example, one for each stream in the file so your backup application should support multiple files in each call to this function.</span></span> <span data-ttu-id="ecbe0-141">In jedem Fall wird jede Common Store-Datei für jeden Sicherungs Durchlauf höchstens einmal zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ecbe0-141">In any case, each common-store file will be returned at most once for each backup pass.</span></span>

<span data-ttu-id="ecbe0-142">Die Sicherungs Anwendung sollte die Datei "Common-Store", die durch den Dateinamen oder die Dateinamen identifiziert wird, die im Parameter " *commonstorefilestobackup* " zurückgegeben werden, sichern oder wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="ecbe0-142">Your backup application should back up or restore the common-store file or files identified by the file name or file names returned in the *commonStoreFilesToBackUp* parameter.</span></span> <span data-ttu-id="ecbe0-143">Unabhängig davon, ob es eine entsprechende Datei mit dem gemeinsamen Speicher gibt, sollte die Sicherungs Anwendung die SIS-Verknüpfungs Datei wie auf dem Datenträger sichern, z. b. als Analyse Punkt und als sparsesdatei, und höchstwahrscheinlich ohne eingefüge Bereiche.</span><span class="sxs-lookup"><span data-stu-id="ecbe0-143">Regardless of whether there is a corresponding common-store file, your backup application should back up the SIS link file as it exists on the disk for example, as a reparse point and a sparse file, and most likely with no ranges filled in.</span></span> <span data-ttu-id="ecbe0-144">Die Sicherungs Anwendung kann die Datei oder Dateien des Common Stores sofort sichern oder wiederherstellen, die Sicherung verzögern oder Sie nach Bedarf miteinander vermischen.</span><span class="sxs-lookup"><span data-stu-id="ecbe0-144">Your backup application may back up or restore the common-store file or files immediately, postpone backing them up, or mix them together as necessary.</span></span>

<span data-ttu-id="ecbe0-145">Nachdem der Sicherungs Vorgang beendet wurde, müssen Sie die Zuordnung des vom *commonstorefilestobackup* -Array von Zeichen folgen verwendeten Speichers durch Aufrufen von [**sisfrealloeredmemory**](sisfreeallocatedmemory.md)aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="ecbe0-145">After the backup operation is complete, deallocate the memory used by the *commonStoreFilesToBackUp* array of strings by calling [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ecbe0-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ecbe0-146">Requirements</span></span>



| <span data-ttu-id="ecbe0-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ecbe0-147">Requirement</span></span> | <span data-ttu-id="ecbe0-148">Wert</span><span class="sxs-lookup"><span data-stu-id="ecbe0-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ecbe0-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ecbe0-149">Minimum supported client</span></span><br/> | <span data-ttu-id="ecbe0-150">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ecbe0-150">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ecbe0-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ecbe0-151">Minimum supported server</span></span><br/> | <span data-ttu-id="ecbe0-152">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ecbe0-152">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ecbe0-153">Header</span><span class="sxs-lookup"><span data-stu-id="ecbe0-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecbe0-154"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecbe0-154"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="ecbe0-155">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ecbe0-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="ecbe0-156"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ecbe0-156"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="ecbe0-157">DLL</span><span class="sxs-lookup"><span data-stu-id="ecbe0-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecbe0-158"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecbe0-158"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecbe0-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ecbe0-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecbe0-160">**Sisfrezuden Speicher**</span><span class="sxs-lookup"><span data-stu-id="ecbe0-160">**SisFreeAllocatedMemory**</span></span>](sisfreeallocatedmemory.md)
</dt> <dt>

[<span data-ttu-id="ecbe0-161">**Siscreatebackupstructure**</span><span class="sxs-lookup"><span data-stu-id="ecbe0-161">**SisCreateBackupStructure**</span></span>](siscreatebackupstructure.md)
</dt> </dl>

 

