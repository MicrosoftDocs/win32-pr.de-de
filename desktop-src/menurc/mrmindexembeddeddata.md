---
title: Mrmindexembeddeddata-Funktion (mrmresourceindexer. h)
description: Indiziert eine einzelne embeddecoddata-Ressource, die zu einer UWP-App gehört.
ms.assetid: 4DA37CF9-43B6-44EE-8A10-DBD4510D7885
keywords:
- Funktionen von mrmindexembedddata und andere Ressourcen
topic_type:
- apiref
api_name:
- MrmIndexEmbeddedData
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 308d08e0e125e7919ad3eb32e6cba2184356fce5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341990"
---
# <a name="mrmindexembeddeddata-function"></a><span data-ttu-id="771d8-104">Mrmindexembeddecoddata-Funktion</span><span class="sxs-lookup"><span data-stu-id="771d8-104">MrmIndexEmbeddedData function</span></span>

<span data-ttu-id="771d8-105">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="771d8-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="771d8-106">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="771d8-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="771d8-107">Indiziert eine einzelne **embeddecoddata** -Ressource, die zu einer UWP-App gehört.</span><span class="sxs-lookup"><span data-stu-id="771d8-107">Indexes a single **embeddeddata** resource belonging to a UWP app.</span></span> <span data-ttu-id="771d8-108">Nimmt eine explizite (aber optionale) Liste von Ressourcen Qualifizierern an.</span><span class="sxs-lookup"><span data-stu-id="771d8-108">Takes an explicit (but optional) list of resource qualifiers.</span></span> <span data-ttu-id="771d8-109">Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="771d8-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="771d8-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="771d8-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexEmbeddedData(
  _In_           MrmResourceIndexerHandle indexer,
  _In_           PCWSTR                   resourceUri,
  _In_     const BYTE                     *embeddedData,
  _In_           ULONG                    embeddedDataSize,
  _In_opt_       PCWSTR                   qualifiers
);
```



## <a name="parameters"></a><span data-ttu-id="771d8-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="771d8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="771d8-112">*Indexer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="771d8-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="771d8-113">Typ: **[ **mrmresourceindexerhandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="771d8-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="771d8-114">Ein Handle, das den ressourcenindexer identifiziert, der die Ressourcen Datei indiziert.</span><span class="sxs-lookup"><span data-stu-id="771d8-114">A handle identifying the resource indexer that will index the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="771d8-115">*resourceUri* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="771d8-115">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="771d8-116">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="771d8-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="771d8-117">Der Ressourcen-URI, der der Ressource zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="771d8-117">The resource URI to assign to the resource.</span></span> <span data-ttu-id="771d8-118">Der Pfad wird als Name der Unterstruktur der Ressourcen Zuordnung für diese Ressource verwendet, wenn Sie später eine PRI-Datei von diesem ressourcenindexer generieren.</span><span class="sxs-lookup"><span data-stu-id="771d8-118">The path will be used as the resource map subtree name for this resource when you later generate a PRI file from this resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="771d8-119">*embedddata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="771d8-119">*embeddedData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="771d8-120">Typ: \* Konstante *Byte \** _</span><span class="sxs-lookup"><span data-stu-id="771d8-120">Type: \**const BYTE\** _</span></span>

<span data-ttu-id="771d8-121">Ein Zeiger auf die Daten der Ressource, die Sie indizieren möchten.</span><span class="sxs-lookup"><span data-stu-id="771d8-121">A pointer to the data of the resource that you want to index.</span></span>

</dd> <dt>

<span data-ttu-id="771d8-122">_embeddedDataSize \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="771d8-122">_embeddedDataSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="771d8-123">Typ: **ulong**</span><span class="sxs-lookup"><span data-stu-id="771d8-123">Type: **ULONG**</span></span>

<span data-ttu-id="771d8-124">Die Größe der Daten, auf die von *embeddecoddata* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="771d8-124">The size of the data pointed to by *embeddedData*.</span></span>

</dd> <dt>

<span data-ttu-id="771d8-125">*Qualifizierer* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="771d8-125">*qualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="771d8-126">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="771d8-126">Type: **PCWSTR**</span></span>

<span data-ttu-id="771d8-127">Eine optionale Liste der Ressourcen Qualifizierer, z. b. L "language-en-US \_ Scale-100 \_ Contrast-Standard".</span><span class="sxs-lookup"><span data-stu-id="771d8-127">An optional list of resource qualifiers, for example L"language-en-US\_scale-100\_contrast-standard".</span></span> <span data-ttu-id="771d8-128">Eine leere Zeichenfolge oder **nullptr** weist auf eine neutrale Ressource hin.</span><span class="sxs-lookup"><span data-stu-id="771d8-128">An empty string or **nullptr** indicates a neutral resource.</span></span> <span data-ttu-id="771d8-129">Ressourcen Qualifizierer werden *nicht* von *resourceUri* abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="771d8-129">Resource qualifiers are *not* inferred from *resourceUri*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="771d8-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="771d8-130">Return value</span></span>

<span data-ttu-id="771d8-131">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="771d8-131">Type: **HRESULT**</span></span>

<span data-ttu-id="771d8-132">S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert.</span><span class="sxs-lookup"><span data-stu-id="771d8-132">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="771d8-133">Verwenden Sie die Makros Success () oder failed () (in WinError. h definiert), um den Erfolg oder Misserfolg zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="771d8-133">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="771d8-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="771d8-134">Remarks</span></span>

<span data-ttu-id="771d8-135">Wenn Sie Ressourcen Qualifizierer angeben möchten, übergeben Sie Sie an den *Qualifizierer* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="771d8-135">If you want to specify any resource qualifiers, then pass them in the *qualifiers* parameter.</span></span> <span data-ttu-id="771d8-136">Ressourcen Qualifizierer werden *nicht* von *resourceUri* abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="771d8-136">Resource qualifiers are *not* inferred from *resourceUri*.</span></span>

<span data-ttu-id="771d8-137">Das Dateinamen Segment von *resourceUri* wird als Ressourcen Name verwendet.</span><span class="sxs-lookup"><span data-stu-id="771d8-137">The file name segment of *resourceUri* is used as the resource name.</span></span>

## <a name="requirements"></a><span data-ttu-id="771d8-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="771d8-138">Requirements</span></span>



| <span data-ttu-id="771d8-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="771d8-139">Requirement</span></span> | <span data-ttu-id="771d8-140">Wert</span><span class="sxs-lookup"><span data-stu-id="771d8-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="771d8-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="771d8-141">Minimum supported client</span></span><br/> | <span data-ttu-id="771d8-142">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="771d8-142">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="771d8-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="771d8-143">Minimum supported server</span></span><br/> | <span data-ttu-id="771d8-144">Nur Windows Server \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="771d8-144">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="771d8-145">Header</span><span class="sxs-lookup"><span data-stu-id="771d8-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="771d8-146"><dt>Mrmresourceingedexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="771d8-146"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="771d8-147">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="771d8-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="771d8-148"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="771d8-148"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="771d8-149">DLL</span><span class="sxs-lookup"><span data-stu-id="771d8-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="771d8-150"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="771d8-150"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="771d8-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="771d8-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="771d8-152">APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme</span><span class="sxs-lookup"><span data-stu-id="771d8-152">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

