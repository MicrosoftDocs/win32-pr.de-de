---
title: Mrmkreateresourceingedexerfrompreviousschemadata-Funktion (mrmresourceingedexer. h)
description: Erstellt einen ressourcenindexer aus in-Memory-Schema Daten, die mit einem vorherigen Aufruf von mrmdumpprifileinmemory oder mrmdumppridatainmemory erstellt wurden.
ms.assetid: D9C90C12-CEFE-4794-9553-8BFBE9E43D99
keywords:
- Mrmcreateresourcindexerfrompreviousschemadata-Funktions Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousSchemaData
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 621500f8f35714daad0e259e6a718c25129987dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477154"
---
# <a name="mrmcreateresourceindexerfrompreviousschemadata-function"></a><span data-ttu-id="ef3ad-104">Mrmkreateresourceingedexerfrompreviousschemadata-Funktion</span><span class="sxs-lookup"><span data-stu-id="ef3ad-104">MrmCreateResourceIndexerFromPreviousSchemaData function</span></span>

<span data-ttu-id="ef3ad-105">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="ef3ad-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ef3ad-106">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="ef3ad-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ef3ad-107">Erstellt einen ressourcenindexer aus in-Memory-Schema Daten, die mit einem vorherigen Aufruf von [**mrmdumpprifileinmemory**](mrmdumpprifileinmemory.md) oder [**mrmdumppridatainmemory**](mrmdumppridatainmemory.md)erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="ef3ad-107">Creates a resource indexer from in-memory schema data created with a previous call to either [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) or [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span></span> <span data-ttu-id="ef3ad-108">Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="ef3ad-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="ef3ad-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef3ad-109">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousSchemaData(
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     BYTE                     *schemaXmlData,
  _In_     ULONG                    schemaXmlSize,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a><span data-ttu-id="ef3ad-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef3ad-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef3ad-111">*projectroot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef3ad-111">*projectRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef3ad-112">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="ef3ad-112">Type: **PCWSTR**</span></span>

<span data-ttu-id="ef3ad-113">Der Projektstamm der UWP-APP, für die Sie pri-Dateien erstellen.</span><span class="sxs-lookup"><span data-stu-id="ef3ad-113">The project root of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="ef3ad-114">Anders ausgedrückt: der Pfad zu den Ressourcen Dateien dieser app.</span><span class="sxs-lookup"><span data-stu-id="ef3ad-114">In other words, the path to that app's resource files.</span></span> <span data-ttu-id="ef3ad-115">Sie geben diese Angabe an, damit Sie in nachfolgenden API-aufrufen desselben ressourcenindexers Pfade relativ zu diesem Stamm angeben können.</span><span class="sxs-lookup"><span data-stu-id="ef3ad-115">You specify this so that you can then specify paths relative to that root in subsequent API calls to the same resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="ef3ad-116">*platformversion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef3ad-116">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef3ad-117">Typ: **[ **mrmplatformversion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="ef3ad-117">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="ef3ad-118">Die Version der Zielplattform für den ressourcenindexer.</span><span class="sxs-lookup"><span data-stu-id="ef3ad-118">The target platform version for the resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="ef3ad-119">*defaultqualifizierer* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="ef3ad-119">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ef3ad-120">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="ef3ad-120">Type: **PCWSTR**</span></span>

<span data-ttu-id="ef3ad-121">Eine Liste der Standard Ressourcen Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="ef3ad-121">A list of default resource qualifiers.</span></span> <span data-ttu-id="ef3ad-122">Beispiel: L "language-en-US \_ Scale-100 \_ Contrast-Standard"</span><span class="sxs-lookup"><span data-stu-id="ef3ad-122">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="ef3ad-123">*schemaxmldata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef3ad-123">*schemaXmlData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef3ad-124">Typ: \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="ef3ad-124">Type: \**BYTE\** _</span></span>

<span data-ttu-id="ef3ad-125">Ein Zeiger auf Schema Daten, die durch einen vorherigen-Befehl entweder für [_ *mrmdumpprifileinmemory* \*](mrmdumpprifileinmemory.md) oder [**mrmdumppridatainmemory**](mrmdumppridatainmemory.md)erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="ef3ad-125">A pointer to schema data created by a previous call to either [_ *MrmDumpPriFileInMemory*\*](mrmdumpprifileinmemory.md) or [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span></span> <span data-ttu-id="ef3ad-126">Machen Sie *schemaxmldata* erst frei, wenn Sie den von dieser Funktion erstellten ressourcenindexer verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="ef3ad-126">Don't free *schemaXmlData* until after you've finished using the resource indexer created by this function.</span></span>

</dd> <dt>

<span data-ttu-id="ef3ad-127">*schemaxmlsize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef3ad-127">*schemaXmlSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef3ad-128">Typ: **ulong**</span><span class="sxs-lookup"><span data-stu-id="ef3ad-128">Type: **ULONG**</span></span>

<span data-ttu-id="ef3ad-129">Die Größe der Daten, auf die von *schemaxmldata* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ef3ad-129">The size of the data pointed to by *schemaXmlData*.</span></span>

</dd> <dt>

<span data-ttu-id="ef3ad-130">*Indexer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ef3ad-130">*indexer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef3ad-131">Typ: \**[**mrmresourceindexerhandle**](mrmresourceindexerhandle.md) \** _</span><span class="sxs-lookup"><span data-stu-id="ef3ad-131">Type: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\** _</span></span>

<span data-ttu-id="ef3ad-132">Ein Zeiger auf ein ressourcenindexer-handle.</span><span class="sxs-lookup"><span data-stu-id="ef3ad-132">A pointer to a resource indexer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef3ad-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ef3ad-133">Return value</span></span>

<span data-ttu-id="ef3ad-134">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="ef3ad-134">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="ef3ad-135">S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert.</span><span class="sxs-lookup"><span data-stu-id="ef3ad-135">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="ef3ad-136">Verwenden Sie die Makros Success () oder failed () (in WinError. h definiert), um den Erfolg oder Misserfolg zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="ef3ad-136">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef3ad-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef3ad-137">Remarks</span></span>

<span data-ttu-id="ef3ad-138">Machen Sie *schemaxmldata* erst frei, wenn Sie den von dieser Funktion erstellten ressourcenindexer verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="ef3ad-138">Don't free *schemaXmlData* until after you've finished using the resource indexer created by this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef3ad-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef3ad-139">Requirements</span></span>



| <span data-ttu-id="ef3ad-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef3ad-140">Requirement</span></span> | <span data-ttu-id="ef3ad-141">Wert</span><span class="sxs-lookup"><span data-stu-id="ef3ad-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef3ad-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ef3ad-142">Minimum supported client</span></span><br/> | <span data-ttu-id="ef3ad-143">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef3ad-143">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ef3ad-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ef3ad-144">Minimum supported server</span></span><br/> | <span data-ttu-id="ef3ad-145">Nur Windows Server \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef3ad-145">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ef3ad-146">Header</span><span class="sxs-lookup"><span data-stu-id="ef3ad-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef3ad-147"><dt>Mrmresourceingedexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef3ad-147"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="ef3ad-148">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ef3ad-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="ef3ad-149"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef3ad-149"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="ef3ad-150">DLL</span><span class="sxs-lookup"><span data-stu-id="ef3ad-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef3ad-151"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef3ad-151"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="ef3ad-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef3ad-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef3ad-153">APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme</span><span class="sxs-lookup"><span data-stu-id="ef3ad-153">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

