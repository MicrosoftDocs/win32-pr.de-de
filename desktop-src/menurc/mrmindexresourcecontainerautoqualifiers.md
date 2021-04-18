---
title: Mrmindexresourcecontainerautoqualifiqualifizierungsfunktion (mrmresourceingedexer. h)
description: Indiziert die Zeichen folgen Ressourcen, die in einer Ressourcen Datei (. resw/. resjson) oder einer priinfo-oder prifile-Datei enthalten sind, die zu einer UWP-App gehört.
ms.assetid: 7FCAA2B5-FF45-4961-84BA-B444B550C91D
keywords:
- Funktionen von mrmindexresourcecontainerautoqualifizierern und anderen Ressourcen
topic_type:
- apiref
api_name:
- MrmIndexResourceContainerAutoQualifiers
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 234566d166e73f75a70b6e613d3f0dfda648ff7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344703"
---
# <a name="mrmindexresourcecontainerautoqualifiers-function"></a><span data-ttu-id="f0454-104">Mrmindexresourcecontainerautoqualifiqualifizierungfunktion</span><span class="sxs-lookup"><span data-stu-id="f0454-104">MrmIndexResourceContainerAutoQualifiers function</span></span>

<span data-ttu-id="f0454-105">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="f0454-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f0454-106">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="f0454-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f0454-107">Indiziert die Zeichen folgen Ressourcen, die in einer Ressourcen Datei (. resw/. resjson) oder einer priinfo-oder prifile-Datei enthalten sind, die zu einer UWP-App gehört.</span><span class="sxs-lookup"><span data-stu-id="f0454-107">Indexes the string resources contained inside a Resources File (.resw/.resjson), or a .priinfo or .prifile, belonging to a UWP app.</span></span> <span data-ttu-id="f0454-108">Leitet eine Liste von Ressourcen Qualifizierern aus dem *Container Path* -Parameter ab.</span><span class="sxs-lookup"><span data-stu-id="f0454-108">Infers a list of resource qualifiers from the *containerPath* parameter.</span></span> <span data-ttu-id="f0454-109">Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="f0454-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="f0454-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0454-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexResourceContainerAutoQualifiers(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ PCWSTR                   containerPath
);
```



## <a name="parameters"></a><span data-ttu-id="f0454-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0454-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0454-112">*Indexer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0454-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0454-113">Typ: **[ **mrmresourceindexerhandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="f0454-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="f0454-114">Ein Handle, das den ressourcenindexer identifiziert, der die Zeichen folgen Ressourcen indiziert.</span><span class="sxs-lookup"><span data-stu-id="f0454-114">A handle identifying the resource indexer that will index the string resources.</span></span>

</dd> <dt>

<span data-ttu-id="f0454-115">*ContainerPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0454-115">*containerPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0454-116">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="f0454-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="f0454-117">Ein relativer Pfad zu einer. resw-, resjson-, priinfo-oder prifile-Datei, die Zeichen folgen Ressourcen enthält, die Sie indizieren möchten.</span><span class="sxs-lookup"><span data-stu-id="f0454-117">A relative path to a .resw, .resjson, .priinfo, or .prifile containing string resources that you want to index.</span></span> <span data-ttu-id="f0454-118">Dieser Pfad ist relativ zum Projektstamm der UWP-APP, für die Sie pri-Dateien erstellen.</span><span class="sxs-lookup"><span data-stu-id="f0454-118">This path is relative to the project root of the UWP app for which you are generating PRI files.</span></span> <span data-ttu-id="f0454-119">Der Projektstamm ist der Wert von *projectroot* , den Sie an [**mrmkreateresourceingedexer**](mrmcreateresourceindexer.md)übergeben haben.</span><span class="sxs-lookup"><span data-stu-id="f0454-119">That project root is the value of *projectRoot* that you passed to [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0454-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0454-120">Return value</span></span>

<span data-ttu-id="f0454-121">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f0454-121">Type: **HRESULT**</span></span>

<span data-ttu-id="f0454-122">S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert.</span><span class="sxs-lookup"><span data-stu-id="f0454-122">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="f0454-123">Verwenden Sie die Makros Success () oder failed () (in WinError. h definiert), um den Erfolg oder Misserfolg zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="f0454-123">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0454-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f0454-124">Remarks</span></span>

<span data-ttu-id="f0454-125">Ressourcen Qualifizierer werden aus *ContainerPath* abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f0454-125">Resource qualifiers are inferred from *containerPath*.</span></span> <span data-ttu-id="f0454-126">Beispielsweise fügt der Wert L "en-US \\ \\ Resources. resw" Zeichen folgen Ressourcen mit dem Qualifizierer "language-en-US" hinzu.</span><span class="sxs-lookup"><span data-stu-id="f0454-126">For example, a value of L"en-US\\\\resources.resw" adds string resources with the qualifier "language-en-US".</span></span>

<span data-ttu-id="f0454-127">Der Name der Ressourcen Datei wird als Name der Unterstruktur der Ressourcen Zuordnung für diese Ressourcen verwendet, wenn Sie später eine PRI-Datei von diesem ressourcenindexer generieren.</span><span class="sxs-lookup"><span data-stu-id="f0454-127">The name of the Resources File will be used as the resource map subtree name for these resources when you later generate a PRI file from this resource indexer.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0454-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0454-128">Requirements</span></span>



| <span data-ttu-id="f0454-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0454-129">Requirement</span></span> | <span data-ttu-id="f0454-130">Wert</span><span class="sxs-lookup"><span data-stu-id="f0454-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0454-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f0454-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f0454-132">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0454-132">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="f0454-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f0454-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f0454-134">Nur Windows Server \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0454-134">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f0454-135">Header</span><span class="sxs-lookup"><span data-stu-id="f0454-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0454-136"><dt>Mrmresourceingedexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0454-136"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="f0454-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f0454-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="f0454-138"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0454-138"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="f0454-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f0454-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0454-140"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0454-140"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="f0454-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0454-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0454-142">APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme</span><span class="sxs-lookup"><span data-stu-id="f0454-142">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

