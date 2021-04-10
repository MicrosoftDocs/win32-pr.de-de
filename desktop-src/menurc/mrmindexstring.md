---
title: Mrmindexstring-Funktion (mrmresourcumdexer. h)
description: Indiziert eine einzelne Zeichen folgen Ressource, die zu einer UWP-App gehört.
ms.assetid: 098F47E7-4BEC-452F-A33C-111F3F524E67
keywords:
- Funktionen von mrmindexstring-Funktionen und andere Ressourcen
topic_type:
- apiref
api_name:
- MrmIndexString
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec0c81155ae2484dd38f29e332a5f0093b07cd9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102990"
---
# <a name="mrmindexstring-function"></a><span data-ttu-id="b7d22-104">Mrmindexstring-Funktion</span><span class="sxs-lookup"><span data-stu-id="b7d22-104">MrmIndexString function</span></span>

<span data-ttu-id="b7d22-105">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="b7d22-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b7d22-106">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="b7d22-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b7d22-107">Indiziert eine einzelne Zeichen folgen Ressource, die zu einer UWP-App gehört.</span><span class="sxs-lookup"><span data-stu-id="b7d22-107">Indexes a single string resource belonging to a UWP app.</span></span> <span data-ttu-id="b7d22-108">Nimmt eine explizite (aber optionale) Liste von Ressourcen Qualifizierern an.</span><span class="sxs-lookup"><span data-stu-id="b7d22-108">Takes an explicit (but optional) list of resource qualifiers.</span></span> <span data-ttu-id="b7d22-109">Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="b7d22-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="b7d22-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7d22-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexString(
  _In_     MrmResourceIndexerHandle indexer,
  _In_     PCWSTR                   resourceUri,
  _In_     PCWSTR                   resourceString,
  _In_opt_ PCWSTR                   qualifiers
);
```



## <a name="parameters"></a><span data-ttu-id="b7d22-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7d22-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7d22-112">*Indexer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7d22-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7d22-113">Typ: **[ **mrmresourceindexerhandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="b7d22-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="b7d22-114">Ein Handle, das den ressourcenindexer identifiziert, der die Zeichen folgen Ressourcen indiziert.</span><span class="sxs-lookup"><span data-stu-id="b7d22-114">A handle identifying the resource indexer that will index the string resources.</span></span>

</dd> <dt>

<span data-ttu-id="b7d22-115">*resourceUri* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7d22-115">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7d22-116">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="b7d22-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="b7d22-117">Der Ressourcen-URI, der der Ressource zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b7d22-117">The resource URI to assign to the resource.</span></span> <span data-ttu-id="b7d22-118">Der Pfad wird als Name der Unterstruktur der Ressourcen Zuordnung für diese Ressource verwendet, wenn Sie später eine PRI-Datei von diesem ressourcenindexer generieren.</span><span class="sxs-lookup"><span data-stu-id="b7d22-118">The path will be used as the resource map subtree name for this resource when you later generate a PRI file from this resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="b7d22-119">*resourcestring* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7d22-119">*resourceString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7d22-120">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="b7d22-120">Type: **PCWSTR**</span></span>

<span data-ttu-id="b7d22-121">Der Wert der Zeichen folgen Ressource.</span><span class="sxs-lookup"><span data-stu-id="b7d22-121">The value of the string resource.</span></span>

</dd> <dt>

<span data-ttu-id="b7d22-122">*Qualifizierer* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="b7d22-122">*qualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b7d22-123">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="b7d22-123">Type: **PCWSTR**</span></span>

<span data-ttu-id="b7d22-124">Eine optionale Liste der Ressourcen Qualifizierer, z. b. L "language-en-US \_ Scale-100 \_ Contrast-Standard".</span><span class="sxs-lookup"><span data-stu-id="b7d22-124">An optional list of resource qualifiers, for example L"language-en-US\_scale-100\_contrast-standard".</span></span> <span data-ttu-id="b7d22-125">Eine leere Zeichenfolge oder **nullptr** weist auf eine neutrale Ressource hin.</span><span class="sxs-lookup"><span data-stu-id="b7d22-125">An empty string or **nullptr** indicates a neutral resource.</span></span> <span data-ttu-id="b7d22-126">Ressourcen Qualifizierer werden *nicht* von *resourceUri* abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b7d22-126">Resource qualifiers are *not* inferred from *resourceUri*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7d22-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b7d22-127">Return value</span></span>

<span data-ttu-id="b7d22-128">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b7d22-128">Type: **HRESULT**</span></span>

<span data-ttu-id="b7d22-129">S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert.</span><span class="sxs-lookup"><span data-stu-id="b7d22-129">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="b7d22-130">Verwenden Sie die Makros Success () oder failed () (in WinError. h definiert), um den Erfolg oder Misserfolg zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="b7d22-130">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7d22-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7d22-131">Remarks</span></span>

<span data-ttu-id="b7d22-132">Wenn Sie Ressourcen Qualifizierer angeben möchten, übergeben Sie Sie an den *Qualifizierer* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="b7d22-132">If you want to specify any resource qualifiers, then pass them in the *qualifiers* parameter.</span></span> <span data-ttu-id="b7d22-133">Ressourcen Qualifizierer werden *nicht* von *resourceUri* abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b7d22-133">Resource qualifiers are *not* inferred from *resourceUri*.</span></span>

<span data-ttu-id="b7d22-134">Das Dateinamen Segment von *resourceUri* wird als Ressourcen Name verwendet.</span><span class="sxs-lookup"><span data-stu-id="b7d22-134">The file name segment of *resourceUri* is used as the resource name.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7d22-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7d22-135">Requirements</span></span>



| <span data-ttu-id="b7d22-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7d22-136">Requirement</span></span> | <span data-ttu-id="b7d22-137">Wert</span><span class="sxs-lookup"><span data-stu-id="b7d22-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7d22-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b7d22-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b7d22-139">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b7d22-139">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b7d22-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b7d22-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b7d22-141">Nur Windows Server \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b7d22-141">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b7d22-142">Header</span><span class="sxs-lookup"><span data-stu-id="b7d22-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7d22-143"><dt>Mrmresourceingedexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7d22-143"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="b7d22-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b7d22-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="b7d22-145"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7d22-145"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="b7d22-146">DLL</span><span class="sxs-lookup"><span data-stu-id="b7d22-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7d22-147"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7d22-147"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="b7d22-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7d22-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7d22-149">APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme</span><span class="sxs-lookup"><span data-stu-id="b7d22-149">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

