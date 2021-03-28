---
description: Bestimmt, ob die Shell einen Ordner im Synchronisierungs Stamm eines cloudanbieters verschieben, kopieren, löschen oder umbenennen darf.
title: IStorageProviderCopyHook::CopyCallback
ms.topic: reference
ms.date: 11/11/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- IStorageProviderCopyHook::CopyCallback
api_type:
- COM
api_location:
- shobjidl.h
ms.openlocfilehash: c7df9296f2261e3907702067ca36265095102f34
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104995238"
---
# <a name="istorageprovidercopyhookcopycallback-method"></a><span data-ttu-id="5ad16-103">Istorageprovidercopyhook:: copycallback-Methode</span><span class="sxs-lookup"><span data-stu-id="5ad16-103">IStorageProviderCopyHook::CopyCallback method</span></span>

<span data-ttu-id="5ad16-104">Bestimmt, ob die Shell einen Ordner im Synchronisierungs Stamm eines cloudanbieters verschieben, kopieren, löschen oder umbenennen darf.</span><span class="sxs-lookup"><span data-stu-id="5ad16-104">Determines whether the Shell will be allowed to move, copy, delete, or rename a folder in a cloud provider's sync root.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ad16-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ad16-105">Syntax</span></span>

```C++
HRESULT CopyCallback( 
    HWND hwnd,
    UINT operation,
    UINT flags,
    LPCWSTR srcFile,
    DWORD srcAttribs,
    LPCWSTR destFile,
    DWORD destAttribs,
    UINT* result
);
```

## <a name="parameters"></a><span data-ttu-id="5ad16-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ad16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ad16-107">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ad16-107">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ad16-108">Ein Handle für das Fenster, das der Kopier-Hook-Handler als übergeordnetes Element für alle Benutzeroberflächen Elemente verwenden soll, die der Handler möglicherweise anzeigen muss.</span><span class="sxs-lookup"><span data-stu-id="5ad16-108">A handle to the window that the copy hook handler should use as the parent for any user interface elements the handler may need to display.</span></span> <span data-ttu-id="5ad16-109">Wenn **FOF_SILENT** im- *Vorgang* angegeben wird, sollte die-Methode diesen Parameter ignorieren.</span><span class="sxs-lookup"><span data-stu-id="5ad16-109">If **FOF_SILENT** is specified in *operation*, the method should ignore this parameter.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="5ad16-110">*Vorgang* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ad16-110">*operation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ad16-111">Der auszuführende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="5ad16-111">The operation to perform.</span></span> <span data-ttu-id="5ad16-112">Dieser Parameter kann einer der Werte sein, die unter dem **wfunc** -Member der [shatleopstruct](/windows/win32/api/shellapi/ns-shellapi-shfileopstructa) -Struktur aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="5ad16-112">This parameter can be one of the values listed under the **wFunc** member of the [SHFILEOPSTRUCT](/windows/win32/api/shellapi/ns-shellapi-shfileopstructa) structure.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="5ad16-113">*Flags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ad16-113">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ad16-114">Die Flags, die den Vorgang steuern.</span><span class="sxs-lookup"><span data-stu-id="5ad16-114">The flags that control the operation.</span></span> <span data-ttu-id="5ad16-115">Bei diesem Parameter kann es sich um einen oder mehrere der Werte handeln, die unter dem *fFlags* -Member der [shatleopstruct](/windows/desktop/api/shellapi/ns-shellapi-shfileopstructa) -Struktur aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="5ad16-115">This parameter can be one or more of the values listed under the *fFlags* member of the [SHFILEOPSTRUCT](/windows/desktop/api/shellapi/ns-shellapi-shfileopstructa) structure.</span></span>

<span data-ttu-id="5ad16-116">Bei druckerkopierhooks ist dieser Wert einer der folgenden Werte, die in "shellapi. h" definiert sind.</span><span class="sxs-lookup"><span data-stu-id="5ad16-116">For printer copy hooks, this value is one of the following values defined in shellapi.h.</span></span>

| <span data-ttu-id="5ad16-117">Wert</span><span class="sxs-lookup"><span data-stu-id="5ad16-117">Value</span></span>       | <span data-ttu-id="5ad16-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5ad16-118">Description</span></span> |
|-------------|------------|
|  <span data-ttu-id="5ad16-119">**PO_DELETE**</span><span class="sxs-lookup"><span data-stu-id="5ad16-119">**PO_DELETE**</span></span>      | <span data-ttu-id="5ad16-120">Ein Drucker wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="5ad16-120">A printer is being deleted.</span></span> <span data-ttu-id="5ad16-121">Der *srcfile* -Parameter verweist auf den vollständigen Pfad zum angegebenen Drucker.</span><span class="sxs-lookup"><span data-stu-id="5ad16-121">The *srcFile* parameter points to the full path to the specified printer.</span></span>           |
|  <span data-ttu-id="5ad16-122">**PO_RENAME**</span><span class="sxs-lookup"><span data-stu-id="5ad16-122">**PO_RENAME**</span></span>       | <span data-ttu-id="5ad16-123">Ein Drucker wird umbenannt.</span><span class="sxs-lookup"><span data-stu-id="5ad16-123">A printer is being renamed.</span></span> <span data-ttu-id="5ad16-124">Der *srcfile* -Parameter verweist auf den neuen Namen des Druckers.</span><span class="sxs-lookup"><span data-stu-id="5ad16-124">The *srcFile* parameter points to the printer's new name.</span></span> <span data-ttu-id="5ad16-125">Der *destfile* -Parameter verweist auf den alten Namen.</span><span class="sxs-lookup"><span data-stu-id="5ad16-125">The *destFile* parameter points to the old name.</span></span>           |
| <span data-ttu-id="5ad16-126">**PO_PORTCHANGE**</span><span class="sxs-lookup"><span data-stu-id="5ad16-126">**PO_PORTCHANGE**</span></span>    | <span data-ttu-id="5ad16-127">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5ad16-127">Not supported.</span></span> <span data-ttu-id="5ad16-128">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5ad16-128">Do not use.</span></span>          |
| <span data-ttu-id="5ad16-129">**PO_REN_PORT**</span><span class="sxs-lookup"><span data-stu-id="5ad16-129">**PO_REN_PORT**</span></span>    | <span data-ttu-id="5ad16-130">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5ad16-130">Not supported.</span></span> <span data-ttu-id="5ad16-131">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5ad16-131">Do not use.</span></span>           |

</dd> </dl>

<dl> <dt>

<span data-ttu-id="5ad16-132">*srcfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ad16-132">*srcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ad16-133">Ein Zeiger auf eine Zeichenfolge, die den Namen des Quell Ordners enthält.</span><span class="sxs-lookup"><span data-stu-id="5ad16-133">A pointer to a string that contains the name of the source folder.</span></span>

</dd> </dl>

<span data-ttu-id="5ad16-134">*srcatcher* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ad16-134">*srcAttribs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ad16-135">Die Attribute des Quell Ordners.</span><span class="sxs-lookup"><span data-stu-id="5ad16-135">The attributes of the source folder.</span></span> <span data-ttu-id="5ad16-136">Dieser Parameter kann eine Kombination aus beliebigen dateiattributflags (FILE_ATTRIBUTE_ \*) sein, die in den Header Dateien definiert sind.</span><span class="sxs-lookup"><span data-stu-id="5ad16-136">This parameter can be a combination of any of the file attribute flags (FILE_ATTRIBUTE_\*) defined in the header files.</span></span> <span data-ttu-id="5ad16-137">Siehe [Datei Attribut Konstanten](../fileio/file-attribute-constants.md).</span><span class="sxs-lookup"><span data-stu-id="5ad16-137">See [File Attribute Constants](../fileio/file-attribute-constants.md).</span></span>

</dd> </dl>

<span data-ttu-id="5ad16-138">*destfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ad16-138">*destFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ad16-139">Ein Zeiger auf eine Zeichenfolge, die den Namen des Ziel Ordners enthält.</span><span class="sxs-lookup"><span data-stu-id="5ad16-139">A pointer to a string that contains the name of the destination folder.</span></span>

</dd> </dl>

<span data-ttu-id="5ad16-140">"out"  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ad16-140">*destAttribs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ad16-141">Die Attribute des Ziel Ordners.</span><span class="sxs-lookup"><span data-stu-id="5ad16-141">The attributes of the destination folder.</span></span> <span data-ttu-id="5ad16-142">Dieser Parameter kann eine Kombination aus beliebigen dateiattributflags (FILE_ATTRIBUTE_ \*) sein, die in den Header Dateien definiert sind.</span><span class="sxs-lookup"><span data-stu-id="5ad16-142">This parameter can be a combination of any of the file attribute flags (FILE_ATTRIBUTE_\*) defined in the header files.</span></span> <span data-ttu-id="5ad16-143">Siehe [Datei Attribut Konstanten](../fileio/file-attribute-constants.md).</span><span class="sxs-lookup"><span data-stu-id="5ad16-143">See [File Attribute Constants](../fileio/file-attribute-constants.md).</span></span>

</dd> </dl>

<span data-ttu-id="5ad16-144">*Ergebnis* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5ad16-144">*result* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ad16-145">Der ganzzahlige Wert, der angibt, ob die Shell den Vorgang ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="5ad16-145">The integer value that indicates whether the Shell should perform the operation.</span></span> <span data-ttu-id="5ad16-146">Einer der folgenden:</span><span class="sxs-lookup"><span data-stu-id="5ad16-146">One of the following:</span></span>

| <span data-ttu-id="5ad16-147">Wert</span><span class="sxs-lookup"><span data-stu-id="5ad16-147">Value</span></span>       | <span data-ttu-id="5ad16-148">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5ad16-148">Description</span></span> |
|-------------|------------|
| <span data-ttu-id="5ad16-149">**IDYES**</span><span class="sxs-lookup"><span data-stu-id="5ad16-149">**IDYES**</span></span>       | <span data-ttu-id="5ad16-150">Ermöglicht den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="5ad16-150">Allows the operation.</span></span>           |
| <span data-ttu-id="5ad16-151">**IDNO**</span><span class="sxs-lookup"><span data-stu-id="5ad16-151">**IDNO**</span></span>        | <span data-ttu-id="5ad16-152">Verhindert, dass der Vorgang in diesem Ordner erfolgt, aber mit allen anderen Vorgängen, die genehmigt wurden (z. b. einem Batch Kopiervorgang) fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="5ad16-152">Prevents the operation on this folder but continues with any other operations that have been approved (for example, a batch copy operation).</span></span>           |
| <span data-ttu-id="5ad16-153">**IDCANCEL**</span><span class="sxs-lookup"><span data-stu-id="5ad16-153">**IDCANCEL**</span></span>    | <span data-ttu-id="5ad16-154">Verhindert den aktuellen Vorgang und bricht alle ausstehenden Vorgänge ab.</span><span class="sxs-lookup"><span data-stu-id="5ad16-154">Prevents the current operation and cancels any pending operations.</span></span>           |


</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="5ad16-155">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ad16-155">Return value</span></span>

<span data-ttu-id="5ad16-156">Gibt **S_OK** zurück, wenn erfolgreich, oder andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="5ad16-156">Returns **S_OK** if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ad16-157">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ad16-157">Remarks</span></span>

<span data-ttu-id="5ad16-158">Die Shell Ruft den Kopier-Hook-Handler des cloudanbieters für jeden Ordner unter dem registrierten Synchronisierungs Stamm auf.</span><span class="sxs-lookup"><span data-stu-id="5ad16-158">The Shell calls the cloud provider's copy hook handler for every folder under the registered sync root.</span></span> <span data-ttu-id="5ad16-159">Legen Sie zum Registrieren eines kopierhook-Handlers für Cloud-Ordner den **copyhook** -Wert unter dem **HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Explorer/syncrootmanager/{syncrootid}** -Schlüssel auf die CLSID des Kopier-Hook-Objekts fest.</span><span class="sxs-lookup"><span data-stu-id="5ad16-159">To register a copy hook handler for cloud folders, set the **CopyHook** value under the **HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Explorer/SyncRootManager/{SyncRootId}** key to the CLSID of the copy hook object.</span></span>

<span data-ttu-id="5ad16-160">Wenn die **copycallback** -Methode aufgerufen wird, initialisiert die Shell die [istorageprovidercopyhook](nn-shobjidl-istorageprovidercopyhook.md) -Schnittstelle direkt, ohne zuerst eine [ishellextinit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) -Schnittstelle zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5ad16-160">When the **CopyCallback** method is called, the Shell initializes the [IStorageProviderCopyHook](nn-shobjidl-istorageprovidercopyhook.md) interface directly without using an [IShellExtInit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface first.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ad16-161">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="5ad16-161">Requirements</span></span>

| <span data-ttu-id="5ad16-162">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ad16-162">Requirement</span></span> | <span data-ttu-id="5ad16-163">Wert</span><span class="sxs-lookup"><span data-stu-id="5ad16-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ad16-164">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ad16-164">Minimum supported client</span></span> | <span data-ttu-id="5ad16-165">Windows 10 Insider Preview-Build 19624</span><span class="sxs-lookup"><span data-stu-id="5ad16-165">Windows 10 Insider Preview Build 19624</span></span>                                |
| <span data-ttu-id="5ad16-166">Header</span><span class="sxs-lookup"><span data-stu-id="5ad16-166">Header</span></span>                   | <span data-ttu-id="5ad16-167">shobjidl. h</span><span class="sxs-lookup"><span data-stu-id="5ad16-167">shobjidl.h</span></span>   |

## <a name="see-also"></a><span data-ttu-id="5ad16-168">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5ad16-168">See also</span></span>

[<span data-ttu-id="5ad16-169">Erstellen einer Cloud-Synchronisierungs-Engine, die Platzhalter Dateien unterstützt</span><span class="sxs-lookup"><span data-stu-id="5ad16-169">Build a Cloud Sync Engine that Supports Placeholder Files</span></span>](../cfapi/build-a-cloud-file-sync-engine.md)