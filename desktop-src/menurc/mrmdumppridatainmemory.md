---
title: Mrmdumppridatainmemory-Funktion (mrmresourceindexer. h)
description: Sichert PRI-Informationen (als BLOB im Arbeitsspeicher, erstellt durch einen vorherigen-Befehl von mrmkreateresourcefileinmemory) an die zugehörige XML-Entsprechung (als in-Memory-Daten), um Sie leichter lesbar zu machen.
ms.assetid: 6E563B43-4E0A-465D-A8EA-7DE61738DE06
keywords:
- Funktionen von mrmdumppridatainmemory-Funktionen und andere Ressourcen
topic_type:
- apiref
api_name:
- MrmDumpPriDataInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072309dcf9ebda1ba4a5669034019582b99105f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345505"
---
# <a name="mrmdumppridatainmemory-function"></a><span data-ttu-id="be181-104">Mrmdumppridatainmemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="be181-104">MrmDumpPriDataInMemory function</span></span>

<span data-ttu-id="be181-105">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="be181-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="be181-106">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="be181-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="be181-107">Sichert PRI-Informationen (als BLOB im Arbeitsspeicher, erstellt durch einen vorherigen-Befehl von [**mrmkreateresourcefileinmemory**](mrmcreateresourcefileinmemory.md)) an die zugehörige XML-Entsprechung (als in-Memory-Daten), um Sie leichter lesbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="be181-107">Dumps PRI info (as a blob in memory, created by a previous call to [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md)) to its XML equivalent (as in-memory data), in order to make it more easily readable.</span></span> <span data-ttu-id="be181-108">Die-Funktion ordnet Speicher zu und gibt einen Zeiger auf diesen Speicher in *outputxmldata* zurück.</span><span class="sxs-lookup"><span data-stu-id="be181-108">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="be181-109">Nennen Sie [**mrmfreememory**](mrmfreememory.md) mit dem gleichen Zeiger, um diesen Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="be181-109">Call [**MrmFreeMemory**](mrmfreememory.md) with the same pointer to free that memory.</span></span> <span data-ttu-id="be181-110">Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="be181-110">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="be181-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="be181-111">Syntax</span></span>


```C++
HRESULT HRESULT MrmDumpPriDataInMemory(
  _In_     BYTE        *inputPriData,
  _In_     ULONG       inputPriSize,
  _In_opt_ BYTE        *schemaPriData,
  _In_     ULONG       schemaPriSize,
  _In_     MrmDumpType dumpType,
  _Out_    BYTE        **outputXmlData,
  _Out_    ULONG       *outputXmlSize
);
```



## <a name="parameters"></a><span data-ttu-id="be181-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="be181-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be181-113">*inputpridata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be181-113">*inputPriData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be181-114">Typ: \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="be181-114">Type: \**BYTE\** _</span></span>

<span data-ttu-id="be181-115">Ein Zeiger auf PRI-Daten, die durch einen vorherigen-Befehl von [_ *mrmkreateresourcefileinmemory* \*](mrmcreateresourcefileinmemory.md)erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="be181-115">A pointer to PRI data created by a previous call to [_ *MrmCreateResourceFileInMemory*\*](mrmcreateresourcefileinmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="be181-116">*Input prisize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be181-116">*inputPriSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be181-117">Typ: **ulong**</span><span class="sxs-lookup"><span data-stu-id="be181-117">Type: **ULONG**</span></span>

<span data-ttu-id="be181-118">Die Größe der Daten, auf die von *inputpridata* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="be181-118">The size of the data pointed to by *inputPriData*.</span></span>

</dd> <dt>

<span data-ttu-id="be181-119">*schemapridata* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="be181-119">*schemaPriData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="be181-120">Typ: \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="be181-120">Type: \**BYTE\** _</span></span>

<span data-ttu-id="be181-121">Ein optionaler Zeiger auf PRI Info (als BLOB im Arbeitsspeicher), der Schema Daten darstellt, die durch einen vorherigen-Befehl von [_ *mrmkreateresourcefileinmemory* \*](mrmcreateresourcefileinmemory.md)erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="be181-121">An optional pointer to PRI info (as a blob in memory) representing schema data created by a previous call to [_ *MrmCreateResourceFileInMemory*\*](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="be181-122">Machen Sie *schemapridata* erst frei, wenn Sie die Verwendung des ressourcenindexers abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="be181-122">Don't free *schemaPriData* until after you've finished using the resource indexer.</span></span> <span data-ttu-id="be181-123">Siehe auch Hinweise.</span><span class="sxs-lookup"><span data-stu-id="be181-123">Also see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="be181-124">*schemaprisize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be181-124">*schemaPriSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be181-125">Typ: **ulong**</span><span class="sxs-lookup"><span data-stu-id="be181-125">Type: **ULONG**</span></span>

<span data-ttu-id="be181-126">Die Größe der Daten, auf die von *schemapridata* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="be181-126">The size of the data pointed to by *schemaPriData*.</span></span>

</dd> <dt>

<span data-ttu-id="be181-127">*dumptype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be181-127">*dumpType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be181-128">Typ: **[ **mrmdumptype**](mrmdumptype.md)**</span><span class="sxs-lookup"><span data-stu-id="be181-128">Type: **[**MrmDumpType**](mrmdumptype.md)**</span></span>

<span data-ttu-id="be181-129">Gibt an, wie detailliert das XML-Dump sein soll oder ob ein Schema gekippt werden soll.</span><span class="sxs-lookup"><span data-stu-id="be181-129">Specifies how detailed the XML dump should be, or whether a schema should be dumped.</span></span>

</dd> <dt>

<span data-ttu-id="be181-130">*outputxmldata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="be181-130">*outputXmlData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be181-131">Type: **Byte \* \***</span><span class="sxs-lookup"><span data-stu-id="be181-131">Type: **BYTE\*\***</span></span>

<span data-ttu-id="be181-132">Die Adresse eines Zeigers auf ein Byte.</span><span class="sxs-lookup"><span data-stu-id="be181-132">The address of a pointer to BYTE.</span></span> <span data-ttu-id="be181-133">Die-Funktion ordnet Speicher zu und gibt einen Zeiger auf diesen Speicher in *outputxmldata* zurück.</span><span class="sxs-lookup"><span data-stu-id="be181-133">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="be181-134">Nennen Sie [**mrmfreememory**](mrmfreememory.md) mit dem Zeiger auf Byte, um diesen Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="be181-134">Call [**MrmFreeMemory**](mrmfreememory.md) with your pointer to BYTE to free that memory.</span></span>

</dd> <dt>

<span data-ttu-id="be181-135">*outputxmlsize* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="be181-135">*outputXmlSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be181-136">Typ: \**ulong \** _</span><span class="sxs-lookup"><span data-stu-id="be181-136">Type: \**ULONG\** _</span></span>

<span data-ttu-id="be181-137">Die Adresse eines ulong.</span><span class="sxs-lookup"><span data-stu-id="be181-137">The address of a ULONG.</span></span> <span data-ttu-id="be181-138">In _outputXmlSize \* gibt die-Funktion die Größe des belegten Speichers zurück, auf den von *outputxmldata* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="be181-138">In _outputXmlSize\*, the function returns the size of the allocated memory pointed to by *outputXmlData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be181-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="be181-139">Return value</span></span>

<span data-ttu-id="be181-140">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="be181-140">Type: **HRESULT**</span></span>

<span data-ttu-id="be181-141">S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert.</span><span class="sxs-lookup"><span data-stu-id="be181-141">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="be181-142">Verwenden Sie die Makros Success () oder failed () (in WinError. h definiert), um den Erfolg oder Misserfolg zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="be181-142">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="be181-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be181-143">Remarks</span></span>

<span data-ttu-id="be181-144">Ein Schema freies Ressourcenpaket, das mit dem " [**mrmpackagingoptionsomitschemafromresourcepacks**](mrmpackagingoptions.md) "-Argument erstellt wurde, das an [**mrmkreateresourcefile**](mrmcreateresourcefile.md) oder [**mrmkreateresourcefileinmemory**](mrmcreateresourcefileinmemory.md) übergeben wurde (oder mit dem Schalter *omitschemafromresourcepacks* in der PRI-Konfigurationsdatei).</span><span class="sxs-lookup"><span data-stu-id="be181-144">A schema-free resource pack is one that was created with the [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) argument passed to [**MrmCreateResourceFile**](mrmcreateresourcefile.md) or [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (or with the *omitSchemaFromResourcePacks* switch in the PRI config file).</span></span> <span data-ttu-id="be181-145">Zum Sichern eines Ressourcen Pakets, das Schema frei ist, übergeben Sie den Pfad zu ihren Hauptpaket-PRI-Daten als Argument für den *schemapridata* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="be181-145">To dump a schema-free resource pack, pass the path to your main package PRI data as the argument for the *schemaPriData* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="be181-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be181-146">Requirements</span></span>



| <span data-ttu-id="be181-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be181-147">Requirement</span></span> | <span data-ttu-id="be181-148">Wert</span><span class="sxs-lookup"><span data-stu-id="be181-148">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be181-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="be181-149">Minimum supported client</span></span><br/> | <span data-ttu-id="be181-150">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="be181-150">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="be181-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="be181-151">Minimum supported server</span></span><br/> | <span data-ttu-id="be181-152">Nur Windows Server \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="be181-152">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="be181-153">Header</span><span class="sxs-lookup"><span data-stu-id="be181-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="be181-154"><dt>Mrmresourceingedexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="be181-154"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="be181-155">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="be181-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="be181-156"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be181-156"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="be181-157">DLL</span><span class="sxs-lookup"><span data-stu-id="be181-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be181-158"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be181-158"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="be181-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be181-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be181-160">APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme</span><span class="sxs-lookup"><span data-stu-id="be181-160">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

