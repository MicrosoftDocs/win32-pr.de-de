---
title: Mrmkreateresourceingedexerfrompreviouspridata-Funktion (mrmresourceingedexer. h)
description: Erstellt einen ressourcenindexer aus PRI-Daten, die durch einen vorherigen Aufruf von mrmkreateresourcefileinmemory erstellt wurden. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme.
ms.assetid: 945ED98C-8D73-404F-ACE3-7DD314FB405A
keywords:
- Mrmcreateresourcindexerfrompreviouspridata-Funktions Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousPriData
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 152ded28e6158fb80d8157c751026091afb51f65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341008"
---
# <a name="mrmcreateresourceindexerfrompreviouspridata-function"></a><span data-ttu-id="602e5-105">Mrmkreateresourceingedexerfrompreviouspridata-Funktion</span><span class="sxs-lookup"><span data-stu-id="602e5-105">MrmCreateResourceIndexerFromPreviousPriData function</span></span>

<span data-ttu-id="602e5-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="602e5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="602e5-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="602e5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="602e5-108">Erstellt einen ressourcenindexer aus PRI-Daten, die durch einen vorherigen Aufruf von [**mrmkreateresourcefileinmemory**](mrmcreateresourcefileinmemory.md)erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="602e5-108">Creates a resource indexer from PRI data created by a previous call to [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="602e5-109">Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="602e5-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="602e5-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="602e5-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousPriData (
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     BYTE                     *priData,
  _In_     ULONG                    priSize,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a><span data-ttu-id="602e5-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="602e5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="602e5-112">*projectroot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="602e5-112">*projectRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="602e5-113">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="602e5-113">Type: **PCWSTR**</span></span>

<span data-ttu-id="602e5-114">Der Projektstamm der UWP-APP, für die Sie pri-Dateien erstellen.</span><span class="sxs-lookup"><span data-stu-id="602e5-114">The project root of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="602e5-115">Anders ausgedrückt: der Pfad zu den Ressourcen Dateien dieser app.</span><span class="sxs-lookup"><span data-stu-id="602e5-115">In other words, the path to that app's resource files.</span></span> <span data-ttu-id="602e5-116">Sie geben diese Angabe an, damit Sie in nachfolgenden API-aufrufen desselben ressourcenindexers Pfade relativ zu diesem Stamm angeben können.</span><span class="sxs-lookup"><span data-stu-id="602e5-116">You specify this so that you can then specify paths relative to that root in subsequent API calls to the same resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="602e5-117">*platformversion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="602e5-117">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="602e5-118">Typ: **[ **mrmplatformversion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="602e5-118">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="602e5-119">Die Version der Zielplattform für den ressourcenindexer.</span><span class="sxs-lookup"><span data-stu-id="602e5-119">The target platform version for the resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="602e5-120">*defaultqualifizierer* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="602e5-120">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="602e5-121">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="602e5-121">Type: **PCWSTR**</span></span>

<span data-ttu-id="602e5-122">Eine Liste der Standard Ressourcen Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="602e5-122">A list of default resource qualifiers.</span></span> <span data-ttu-id="602e5-123">Beispiel: L "language-en-US \_ Scale-100 \_ Contrast-Standard"</span><span class="sxs-lookup"><span data-stu-id="602e5-123">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="602e5-124">*pridata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="602e5-124">*priData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="602e5-125">Typ: \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="602e5-125">Type: \**BYTE\** _</span></span>

<span data-ttu-id="602e5-126">Ein Zeiger auf PRI-Daten, die durch einen vorherigen-Befehl von [_ *mrmkreateresourcefileinmemory* \*](mrmcreateresourcefileinmemory.md)erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="602e5-126">A pointer to PRI data created by a previous call to [_ *MrmCreateResourceFileInMemory*\*](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="602e5-127">Wenn Sie die von dieser Funktion erstellten ressourcenindexer nicht mehr verwenden, sollten Sie *pridata* nicht freigeben.</span><span class="sxs-lookup"><span data-stu-id="602e5-127">Don't free *priData* until after you've finished using the resource indexer created by this function.</span></span>

</dd> <dt>

<span data-ttu-id="602e5-128">*prisize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="602e5-128">*priSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="602e5-129">Typ: **ulong**</span><span class="sxs-lookup"><span data-stu-id="602e5-129">Type: **ULONG**</span></span>

<span data-ttu-id="602e5-130">Die Größe der Daten, auf die von *pridata* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="602e5-130">The size of the data pointed to by *priData*.</span></span>

</dd> <dt>

<span data-ttu-id="602e5-131">*Indexer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="602e5-131">*indexer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="602e5-132">Typ: \**[**mrmresourceindexerhandle**](mrmresourceindexerhandle.md) \** _</span><span class="sxs-lookup"><span data-stu-id="602e5-132">Type: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\** _</span></span>

<span data-ttu-id="602e5-133">Ein Zeiger auf ein ressourcenindexer-handle.</span><span class="sxs-lookup"><span data-stu-id="602e5-133">A pointer to a resource indexer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="602e5-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="602e5-134">Return value</span></span>

<span data-ttu-id="602e5-135">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="602e5-135">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="602e5-136">S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert.</span><span class="sxs-lookup"><span data-stu-id="602e5-136">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="602e5-137">Verwenden Sie die Makros Success () oder failed () (in WinError. h definiert), um den Erfolg oder Misserfolg zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="602e5-137">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="602e5-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="602e5-138">Remarks</span></span>

<span data-ttu-id="602e5-139">Wenn Sie die von dieser Funktion erstellten ressourcenindexer nicht mehr verwenden, sollten Sie *pridata* nicht freigeben.</span><span class="sxs-lookup"><span data-stu-id="602e5-139">Don't free *priData* until after you've finished using the resource indexer created by this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="602e5-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="602e5-140">Requirements</span></span>



| <span data-ttu-id="602e5-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="602e5-141">Requirement</span></span> | <span data-ttu-id="602e5-142">Wert</span><span class="sxs-lookup"><span data-stu-id="602e5-142">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="602e5-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="602e5-143">Minimum supported client</span></span><br/> | <span data-ttu-id="602e5-144">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="602e5-144">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="602e5-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="602e5-145">Minimum supported server</span></span><br/> | <span data-ttu-id="602e5-146">Nur Windows Server \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="602e5-146">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="602e5-147">Header</span><span class="sxs-lookup"><span data-stu-id="602e5-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="602e5-148"><dt>Mrmresourceingedexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="602e5-148"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="602e5-149">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="602e5-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="602e5-150"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="602e5-150"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="602e5-151">DLL</span><span class="sxs-lookup"><span data-stu-id="602e5-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="602e5-152"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="602e5-152"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="602e5-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="602e5-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="602e5-154">APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme</span><span class="sxs-lookup"><span data-stu-id="602e5-154">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

