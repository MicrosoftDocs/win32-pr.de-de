---
title: Mrmkreateresourcefilinput Memory-Funktion (mrmresourceingedexer. h)
description: Erstellt PRI-Informationen als BLOB im Speicher, nicht als Datei auf dem Datenträger.
ms.assetid: 68BDAD27-545A-4DC6-B909-4242A0863690
keywords:
- Funktionen von "mrmcreateresourcefilinput Memory" und weitere Ressourcen
topic_type:
- apiref
api_name:
- MrmCreateResourceFileInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17bbe36a55b5be18f9f4005b4e0ae24d3d610bd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478651"
---
# <a name="mrmcreateresourcefileinmemory-function"></a><span data-ttu-id="2f069-104">Mrmkreateresourcefilinput Memory-Funktion</span><span class="sxs-lookup"><span data-stu-id="2f069-104">MrmCreateResourceFileInMemory function</span></span>

<span data-ttu-id="2f069-105">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="2f069-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2f069-106">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="2f069-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2f069-107">Erstellt PRI-Informationen als BLOB im Speicher, nicht als Datei auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="2f069-107">Creates PRI info as a blob in memory, not as a file on disk.</span></span> <span data-ttu-id="2f069-108">Die-Funktion ordnet Speicher zu und gibt einen Zeiger auf diesen Speicher in *outputpridata* zurück.</span><span class="sxs-lookup"><span data-stu-id="2f069-108">The function allocates memory and returns a pointer to that memory in *outputPriData*.</span></span> <span data-ttu-id="2f069-109">Nennen Sie [**mrmfreememory**](mrmfreememory.md) mit dem gleichen Zeiger, um diesen Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="2f069-109">Call [**MrmFreeMemory**](mrmfreememory.md) with the same pointer to free that memory.</span></span> <span data-ttu-id="2f069-110">Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="2f069-110">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="2f069-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f069-111">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceFileInMemory(
  _In_  MrmResourceIndexerHandle indexer,
  _In_  MrmPackagingMode         packagingMode,
  _In_  MrmPackagingOptions      packagingOptions,
  _Out_ BYTE                     **outputPriData,
  _Out_ ULONG                    *outputPriSize
);
```



## <a name="parameters"></a><span data-ttu-id="2f069-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f069-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f069-113">*Indexer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f069-113">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f069-114">Typ: **[ **mrmresourceindexerhandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="2f069-114">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="2f069-115">Ein Handle, das den ressourcenindexer identifiziert, von dem die PRI-Informationen erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2f069-115">A handle identifying the resource indexer from which to create the PRI info.</span></span>

</dd> <dt>

<span data-ttu-id="2f069-116">*packagingmode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f069-116">*packagingMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f069-117">Typ: **[ **mrmpackagingmode**](mrmpackagingmode.md)**</span><span class="sxs-lookup"><span data-stu-id="2f069-117">Type: **[**MrmPackagingMode**](mrmpackagingmode.md)**</span></span>

<span data-ttu-id="2f069-118">Gibt an, ob die PRI-Informationen eigenständig oder ein Ressourcenpaket sein sollen.</span><span class="sxs-lookup"><span data-stu-id="2f069-118">Specifies whether the PRI info should be standalone, or be a resource pack.</span></span> <span data-ttu-id="2f069-119">**Mrmpackagingmodeautosplit** wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2f069-119">**MrmPackagingModeAutoSplit** is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="2f069-120">*packagingoptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f069-120">*packagingOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f069-121">Typ: **[ **mrmpackagingoptions**](mrmpackagingoptions.md)**</span><span class="sxs-lookup"><span data-stu-id="2f069-121">Type: **[**MrmPackagingOptions**](mrmpackagingoptions.md)**</span></span>

<span data-ttu-id="2f069-122">Gibt zusätzliche Optionen zu den PRI-Informationen an.</span><span class="sxs-lookup"><span data-stu-id="2f069-122">Specifies additional options about the PRI info.</span></span>

</dd> <dt>

<span data-ttu-id="2f069-123">*outputpridata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2f069-123">*outputPriData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f069-124">Type: **Byte \* \***</span><span class="sxs-lookup"><span data-stu-id="2f069-124">Type: **BYTE\*\***</span></span>

<span data-ttu-id="2f069-125">Die Adresse eines Zeigers auf ein Byte.</span><span class="sxs-lookup"><span data-stu-id="2f069-125">The address of a pointer to BYTE.</span></span> <span data-ttu-id="2f069-126">Die-Funktion ordnet Speicher zu und gibt einen Zeiger auf diesen Speicher in *outputpridata* zurück.</span><span class="sxs-lookup"><span data-stu-id="2f069-126">The function allocates memory and returns a pointer to that memory in *outputPriData*.</span></span> <span data-ttu-id="2f069-127">Nennen Sie [**mrmfreememory**](mrmfreememory.md) mit dem Zeiger auf Byte, um diesen Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="2f069-127">Call [**MrmFreeMemory**](mrmfreememory.md) with your pointer to BYTE to free that memory.</span></span>

</dd> <dt>

<span data-ttu-id="2f069-128">*outputprisize* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2f069-128">*outputPriSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f069-129">Typ: \**ulong \** _</span><span class="sxs-lookup"><span data-stu-id="2f069-129">Type: \**ULONG\** _</span></span>

<span data-ttu-id="2f069-130">Die Adresse eines ulong.</span><span class="sxs-lookup"><span data-stu-id="2f069-130">The address of a ULONG.</span></span> <span data-ttu-id="2f069-131">In _outputPriSize \* gibt die-Funktion die Größe des belegten Speichers zurück, auf den von *outputpridata* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="2f069-131">In _outputPriSize\*, the function returns the size of the allocated memory pointed to by *outputPriData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f069-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f069-132">Return value</span></span>

<span data-ttu-id="2f069-133">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2f069-133">Type: **HRESULT**</span></span>

<span data-ttu-id="2f069-134">S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert.</span><span class="sxs-lookup"><span data-stu-id="2f069-134">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="2f069-135">Verwenden Sie die Makros Success () oder failed () (in WinError. h definiert), um den Erfolg oder Misserfolg zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="2f069-135">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f069-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f069-136">Remarks</span></span>

<span data-ttu-id="2f069-137">Wenn Sie *outputpridata* an [**mrmkreateresourcindexerfrompreviouspridata**](mrmcreateresourceindexerfrompreviouspridata-.md)übergeben, geben Sie den Arbeitsspeicher erst frei, nachdem Sie den ressourcenindexer verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="2f069-137">If you pass *outputPriData* to [**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md), then don't free the memory until after you've finished using the resource indexer.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f069-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f069-138">Requirements</span></span>



| <span data-ttu-id="2f069-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f069-139">Requirement</span></span> | <span data-ttu-id="2f069-140">Wert</span><span class="sxs-lookup"><span data-stu-id="2f069-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f069-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2f069-141">Minimum supported client</span></span><br/> | <span data-ttu-id="2f069-142">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f069-142">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2f069-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2f069-143">Minimum supported server</span></span><br/> | <span data-ttu-id="2f069-144">Nur Windows Server \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f069-144">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2f069-145">Header</span><span class="sxs-lookup"><span data-stu-id="2f069-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f069-146"><dt>Mrmresourceingedexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f069-146"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="2f069-147">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2f069-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="2f069-148"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f069-148"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="2f069-149">DLL</span><span class="sxs-lookup"><span data-stu-id="2f069-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f069-150"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f069-150"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="2f069-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f069-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f069-152">APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme</span><span class="sxs-lookup"><span data-stu-id="2f069-152">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

