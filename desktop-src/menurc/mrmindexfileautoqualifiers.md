---
title: Mrmindexfileautoqualifiziererfunktion (mrmresourceingedexer. h)
description: Indiziert eine Ressourcen Datei, die zu einer UWP-App gehört. Leitet eine Liste von Ressourcen Qualifizierern aus dem filePath-Parameter ab. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme.
ms.assetid: CEA4D845-987C-48D6-B80E-9F055363FFE0
keywords:
- Funktions Menüs und andere Ressourcen für die mrmindexfileautoqualifizierer
topic_type:
- apiref
api_name:
- MrmIndexFileAutoQualifiers
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65254a8715073060e9b4fc1578b68d54ae987958
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102991"
---
# <a name="mrmindexfileautoqualifiers-function"></a><span data-ttu-id="54da7-106">Mrmindexfileautoqualifizierer-Funktion</span><span class="sxs-lookup"><span data-stu-id="54da7-106">MrmIndexFileAutoQualifiers function</span></span>

<span data-ttu-id="54da7-107">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="54da7-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="54da7-108">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="54da7-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="54da7-109">Indiziert eine Ressourcen Datei, die zu einer UWP-App gehört.</span><span class="sxs-lookup"><span data-stu-id="54da7-109">Indexes a resource file belonging to a UWP app.</span></span> <span data-ttu-id="54da7-110">Leitet eine Liste von Ressourcen Qualifizierern aus dem *FilePath* -Parameter ab.</span><span class="sxs-lookup"><span data-stu-id="54da7-110">Infers a list of resource qualifiers from the *filePath* parameter.</span></span> <span data-ttu-id="54da7-111">Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="54da7-111">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="54da7-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="54da7-112">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexFileAutoQualifiers(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ PCWSTR                   filePath
);
```



## <a name="parameters"></a><span data-ttu-id="54da7-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="54da7-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54da7-114">*Indexer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54da7-114">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54da7-115">Typ: **[ **mrmresourceindexerhandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="54da7-115">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="54da7-116">Ein Handle, das den ressourcenindexer identifiziert, der die Ressourcen Datei indiziert.</span><span class="sxs-lookup"><span data-stu-id="54da7-116">A handle identifying the resource indexer that will index the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="54da7-117">*FilePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54da7-117">*filePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54da7-118">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="54da7-118">Type: **PCWSTR**</span></span>

<span data-ttu-id="54da7-119">Ein relativer Pfad zu einer Datei, die eine Ressource enthält, die Sie indizieren möchten.</span><span class="sxs-lookup"><span data-stu-id="54da7-119">A relative path to a file containing a resource that you want to index.</span></span> <span data-ttu-id="54da7-120">Dieser Pfad ist relativ zum Projektstamm der UWP-APP, für die Sie pri-Dateien erstellen.</span><span class="sxs-lookup"><span data-stu-id="54da7-120">This path is relative to the project root of the UWP app for which you are generating PRI files.</span></span> <span data-ttu-id="54da7-121">Der Projektstamm ist der Wert von *projectroot* , den Sie an [**mrmkreateresourceingedexer**](mrmcreateresourceindexer.md)übergeben haben.</span><span class="sxs-lookup"><span data-stu-id="54da7-121">That project root is the value of *projectRoot* that you passed to [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54da7-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54da7-122">Return value</span></span>

<span data-ttu-id="54da7-123">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="54da7-123">Type: **HRESULT**</span></span>

<span data-ttu-id="54da7-124">S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert.</span><span class="sxs-lookup"><span data-stu-id="54da7-124">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="54da7-125">Verwenden Sie die Makros Success () oder failed () (in WinError. h definiert), um den Erfolg oder Misserfolg zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="54da7-125">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="54da7-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54da7-126">Remarks</span></span>

<span data-ttu-id="54da7-127">Das Dateinamen Segment von *FilePath* wird als Ressourcen Name verwendet. und Ressourcen Qualifizierer werden aus dem Pfad abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="54da7-127">The file name segment of *filePath* is used as the resource name; and resource qualifiers are derived from its path.</span></span> <span data-ttu-id="54da7-128">Wenn Sie z. b. L "Images \\ de-de \\ Scale-100 \\background.png" an *FilePath* übergeben, fügt der ressourcenindexer eine Ressource mit dem Namen "background.png" mit den Ressourcen Qualifizierern "language-de-de" und "Scale-100" hinzu.</span><span class="sxs-lookup"><span data-stu-id="54da7-128">For example, if you pass L"Images\\de-DE\\scale-100\\background.png" to *filePath* then the resource indexer adds a resource named "background.png" with resource qualifiers "language-de-DE" and "scale-100".</span></span>

<span data-ttu-id="54da7-129">L "Files" wird als Name der Unterstruktur der Ressourcen Zuordnung für diese Ressource verwendet, wenn Sie später eine PRI-Datei von diesem ressourcenindexer generieren.</span><span class="sxs-lookup"><span data-stu-id="54da7-129">L"Files" will be used as the resource map subtree name for this resource when you later generate a PRI file from this resource indexer.</span></span>

## <a name="requirements"></a><span data-ttu-id="54da7-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54da7-130">Requirements</span></span>



| <span data-ttu-id="54da7-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54da7-131">Requirement</span></span> | <span data-ttu-id="54da7-132">Wert</span><span class="sxs-lookup"><span data-stu-id="54da7-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54da7-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54da7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="54da7-134">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54da7-134">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="54da7-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54da7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="54da7-136">Nur Windows Server \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54da7-136">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="54da7-137">Header</span><span class="sxs-lookup"><span data-stu-id="54da7-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="54da7-138"><dt>Mrmresourceingedexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="54da7-138"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="54da7-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="54da7-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="54da7-140"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54da7-140"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="54da7-141">DLL</span><span class="sxs-lookup"><span data-stu-id="54da7-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54da7-142"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54da7-142"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="54da7-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54da7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54da7-144">APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme</span><span class="sxs-lookup"><span data-stu-id="54da7-144">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

