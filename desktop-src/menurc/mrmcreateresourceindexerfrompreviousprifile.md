---
title: Mrmkreateresourceindexerfrompreviousprifile-Funktion (mrmresourceindexer. h)
description: Erstellt einen ressourcenindexer aus einer PRI-Datei, die mit einem vorherigen Aufruf von mrmkreateresourcefile erstellt wurde. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme.
ms.assetid: 8B3743EF-1A27-4B70-9577-8549B91DBC1E
keywords:
- Mrmcreateresourceindexerfrompreviousprifile-Funktions Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousPriFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be08170dc8ae25db34492273e7c612352d5e0530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340795"
---
# <a name="mrmcreateresourceindexerfrompreviousprifile-function"></a><span data-ttu-id="b82df-105">Mrmkreateresourceindexerfrompreviousprifile-Funktion</span><span class="sxs-lookup"><span data-stu-id="b82df-105">MrmCreateResourceIndexerFromPreviousPriFile function</span></span>

<span data-ttu-id="b82df-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="b82df-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b82df-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="b82df-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b82df-108">Erstellt einen ressourcenindexer aus einer PRI-Datei, die mit einem vorherigen Aufruf von [**mrmkreateresourcefile**](mrmcreateresourcefile.md)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b82df-108">Creates a resource indexer from a PRI file created with a previous call to [**MrmCreateResourceFile**](mrmcreateresourcefile.md).</span></span> <span data-ttu-id="b82df-109">Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="b82df-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="b82df-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b82df-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousPriFile(
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     PCWSTR                   priFile,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a><span data-ttu-id="b82df-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b82df-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b82df-112">*projectroot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b82df-112">*projectRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b82df-113">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="b82df-113">Type: **PCWSTR**</span></span>

<span data-ttu-id="b82df-114">Der Projektstamm der UWP-APP, für die Sie pri-Dateien erstellen.</span><span class="sxs-lookup"><span data-stu-id="b82df-114">The project root of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="b82df-115">Anders ausgedrückt: der Pfad zu den Ressourcen Dateien dieser app.</span><span class="sxs-lookup"><span data-stu-id="b82df-115">In other words, the path to that app's resource files.</span></span> <span data-ttu-id="b82df-116">Sie geben diese Angabe an, damit Sie in nachfolgenden API-aufrufen desselben ressourcenindexers Pfade relativ zu diesem Stamm angeben können.</span><span class="sxs-lookup"><span data-stu-id="b82df-116">You specify this so that you can then specify paths relative to that root in subsequent API calls to the same resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="b82df-117">*platformversion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b82df-117">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b82df-118">Typ: **[ **mrmplatformversion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="b82df-118">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="b82df-119">Die Version der Zielplattform für den ressourcenindexer.</span><span class="sxs-lookup"><span data-stu-id="b82df-119">The target platform version for the resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="b82df-120">*defaultqualifizierer* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="b82df-120">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b82df-121">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="b82df-121">Type: **PCWSTR**</span></span>

<span data-ttu-id="b82df-122">Eine Liste der Standard Ressourcen Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="b82df-122">A list of default resource qualifiers.</span></span> <span data-ttu-id="b82df-123">Beispiel: L "language-en-US \_ Scale-100 \_ Contrast-Standard"</span><span class="sxs-lookup"><span data-stu-id="b82df-123">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="b82df-124">*prifile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b82df-124">*priFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b82df-125">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="b82df-125">Type: **PCWSTR**</span></span>

<span data-ttu-id="b82df-126">Ein vollständiger Dateipfad zu einer PRI-Datei.</span><span class="sxs-lookup"><span data-stu-id="b82df-126">A full file path to a PRI file.</span></span>

</dd> <dt>

<span data-ttu-id="b82df-127">*Indexer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b82df-127">*indexer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b82df-128">Typ: \**[**mrmresourceindexerhandle**](mrmresourceindexerhandle.md) \** _</span><span class="sxs-lookup"><span data-stu-id="b82df-128">Type: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\** _</span></span>

<span data-ttu-id="b82df-129">Ein Zeiger auf ein ressourcenindexer-handle.</span><span class="sxs-lookup"><span data-stu-id="b82df-129">A pointer to a resource indexer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b82df-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b82df-130">Return value</span></span>

<span data-ttu-id="b82df-131">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="b82df-131">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="b82df-132">S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert.</span><span class="sxs-lookup"><span data-stu-id="b82df-132">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="b82df-133">Verwenden Sie die Makros Success () oder failed () (in WinError. h definiert), um den Erfolg oder Misserfolg zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="b82df-133">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b82df-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b82df-134">Requirements</span></span>



| <span data-ttu-id="b82df-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b82df-135">Requirement</span></span> | <span data-ttu-id="b82df-136">Wert</span><span class="sxs-lookup"><span data-stu-id="b82df-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b82df-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b82df-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b82df-138">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b82df-138">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b82df-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b82df-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b82df-140">Nur Windows Server \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b82df-140">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b82df-141">Header</span><span class="sxs-lookup"><span data-stu-id="b82df-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="b82df-142"><dt>Mrmresourceingedexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="b82df-142"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="b82df-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b82df-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="b82df-144"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b82df-144"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="b82df-145">DLL</span><span class="sxs-lookup"><span data-stu-id="b82df-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b82df-146"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b82df-146"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="b82df-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b82df-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b82df-148">APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme</span><span class="sxs-lookup"><span data-stu-id="b82df-148">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

