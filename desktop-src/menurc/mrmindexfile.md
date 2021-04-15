---
title: Mrmindexfile-Funktion (mrmresourceindexer. h)
description: Indiziert eine Ressourcen Datei, die zu einer UWP-App gehört. Nimmt eine explizite (aber optionale) Liste von Ressourcen Qualifizierern an. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme.
ms.assetid: C9F245B4-D2D3-4863-BB64-72619FC73D3C
keywords:
- Funktionen der mrtrexfile-Funktion und weitere Ressourcen
topic_type:
- apiref
api_name:
- MrmIndexFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9db3e0521f954a2d5d5e0286fb6f21b8e5f55eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478645"
---
# <a name="mrmindexfile-function"></a><span data-ttu-id="b58dd-106">Mrmindexfile-Funktion</span><span class="sxs-lookup"><span data-stu-id="b58dd-106">MrmIndexFile function</span></span>

<span data-ttu-id="b58dd-107">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="b58dd-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b58dd-108">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="b58dd-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b58dd-109">Indiziert eine Ressourcen Datei, die zu einer UWP-App gehört.</span><span class="sxs-lookup"><span data-stu-id="b58dd-109">Indexes a resource file belonging to a UWP app.</span></span> <span data-ttu-id="b58dd-110">Nimmt eine explizite (aber optionale) Liste von Ressourcen Qualifizierern an.</span><span class="sxs-lookup"><span data-stu-id="b58dd-110">Takes an explicit (but optional) list of resource qualifiers.</span></span> <span data-ttu-id="b58dd-111">Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="b58dd-111">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="b58dd-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="b58dd-112">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexFile(
  _In_     MrmResourceIndexerHandle indexer,
  _In_     PCWSTR                   resourceUri,
  _In_     PCWSTR                   filePath,
  _In_opt_ PCWSTR                   qualifiers
);
```



## <a name="parameters"></a><span data-ttu-id="b58dd-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b58dd-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b58dd-114">*Indexer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b58dd-114">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b58dd-115">Typ: **[ **mrmresourceindexerhandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="b58dd-115">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="b58dd-116">Ein Handle, das den ressourcenindexer identifiziert, der die Ressourcen Datei indiziert.</span><span class="sxs-lookup"><span data-stu-id="b58dd-116">A handle identifying the resource indexer that will index the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="b58dd-117">*resourceUri* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b58dd-117">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b58dd-118">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="b58dd-118">Type: **PCWSTR**</span></span>

<span data-ttu-id="b58dd-119">Der Ressourcen-URI, der der Ressource zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b58dd-119">The resource URI to assign to the resource.</span></span> <span data-ttu-id="b58dd-120">Der Pfad wird als Name der Unterstruktur der Ressourcen Zuordnung für diese Ressource verwendet, wenn Sie später eine PRI-Datei von diesem ressourcenindexer generieren.</span><span class="sxs-lookup"><span data-stu-id="b58dd-120">The path will be used as the resource map subtree name for this resource when you later generate a PRI file from this resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="b58dd-121">*FilePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b58dd-121">*filePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b58dd-122">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="b58dd-122">Type: **PCWSTR**</span></span>

<span data-ttu-id="b58dd-123">Ein relativer Pfad zu einer Datei, die eine Ressource enthält, die Sie indizieren möchten.</span><span class="sxs-lookup"><span data-stu-id="b58dd-123">A relative path to a file containing a resource that you want to index.</span></span> <span data-ttu-id="b58dd-124">Dieser Pfad ist relativ zum Projektstamm der UWP-APP, für die Sie pri-Dateien erstellen.</span><span class="sxs-lookup"><span data-stu-id="b58dd-124">This path is relative to the project root of the UWP app for which you are generating PRI files.</span></span> <span data-ttu-id="b58dd-125">Der Projektstamm ist der Wert von *projectroot* , den Sie an [**mrmkreateresourceingedexer**](mrmcreateresourceindexer.md)übergeben haben.</span><span class="sxs-lookup"><span data-stu-id="b58dd-125">That project root is the value of *projectRoot* that you passed to [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span></span>

</dd> <dt>

<span data-ttu-id="b58dd-126">*Qualifizierer* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="b58dd-126">*qualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b58dd-127">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="b58dd-127">Type: **PCWSTR**</span></span>

<span data-ttu-id="b58dd-128">Eine optionale Liste der Ressourcen Qualifizierer, z. b. L "language-en-US \_ Scale-100 \_ Contrast-Standard".</span><span class="sxs-lookup"><span data-stu-id="b58dd-128">An optional list of resource qualifiers, for example L"language-en-US\_scale-100\_contrast-standard".</span></span> <span data-ttu-id="b58dd-129">Eine leere Zeichenfolge oder **nullptr** weist auf eine neutrale Ressource hin.</span><span class="sxs-lookup"><span data-stu-id="b58dd-129">An empty string or **nullptr** indicates a neutral resource.</span></span> <span data-ttu-id="b58dd-130">Ressourcen Qualifizierer werden *nicht* von *resourceUri* und *ContainerPath* abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b58dd-130">Resource qualifiers are *not* inferred from *resourceUri* nor from *containerPath*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b58dd-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b58dd-131">Return value</span></span>

<span data-ttu-id="b58dd-132">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b58dd-132">Type: **HRESULT**</span></span>

<span data-ttu-id="b58dd-133">S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert.</span><span class="sxs-lookup"><span data-stu-id="b58dd-133">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="b58dd-134">Verwenden Sie die Makros Success () oder failed () (in WinError. h definiert), um den Erfolg oder Misserfolg zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="b58dd-134">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="b58dd-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b58dd-135">Remarks</span></span>

<span data-ttu-id="b58dd-136">Wenn Sie Ressourcen Qualifizierer angeben möchten, übergeben Sie Sie an den *Qualifizierer* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="b58dd-136">If you want to specify any resource qualifiers, then pass them in the *qualifiers* parameter.</span></span> <span data-ttu-id="b58dd-137">Ressourcen Qualifizierer werden *nicht* von *resourceUri* oder von *FilePath* abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b58dd-137">Resource qualifiers are *not* inferred from *resourceUri* nor from *filePath*.</span></span>

<span data-ttu-id="b58dd-138">Das Dateinamen Segment von *resourceUri* (nicht *FilePath*) wird als Ressourcen Name verwendet.</span><span class="sxs-lookup"><span data-stu-id="b58dd-138">The file name segment of *resourceUri* (not *filePath*) is used as the resource name.</span></span>

## <a name="requirements"></a><span data-ttu-id="b58dd-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b58dd-139">Requirements</span></span>



| <span data-ttu-id="b58dd-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b58dd-140">Requirement</span></span> | <span data-ttu-id="b58dd-141">Wert</span><span class="sxs-lookup"><span data-stu-id="b58dd-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b58dd-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b58dd-142">Minimum supported client</span></span><br/> | <span data-ttu-id="b58dd-143">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b58dd-143">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b58dd-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b58dd-144">Minimum supported server</span></span><br/> | <span data-ttu-id="b58dd-145">Nur Windows Server \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b58dd-145">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b58dd-146">Header</span><span class="sxs-lookup"><span data-stu-id="b58dd-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="b58dd-147"><dt>Mrmresourceingedexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="b58dd-147"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="b58dd-148">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b58dd-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="b58dd-149"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b58dd-149"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="b58dd-150">DLL</span><span class="sxs-lookup"><span data-stu-id="b58dd-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b58dd-151"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b58dd-151"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="b58dd-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b58dd-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b58dd-153">APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme</span><span class="sxs-lookup"><span data-stu-id="b58dd-153">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

