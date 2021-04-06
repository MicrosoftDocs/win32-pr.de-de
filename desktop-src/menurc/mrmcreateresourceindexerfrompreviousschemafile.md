---
title: Mrmkreateresourceindexerfrompreviousschemafile-Funktion (mrmresourceindexer. h)
description: Erstellt einen ressourcenindexer aus einer Schema Datei, die mit einem vorherigen Aufruf von mrmdumpprifile erstellt wurde. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme.
ms.assetid: 2ECF355C-C6FD-4949-B455-52E3FF455005
keywords:
- Mrmcreateresourceindexerfrompreviousschemafile-Funktions Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousSchemaFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 304e0aebe75ac416623cb1ec1053a7b6ae504194
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743056"
---
# <a name="mrmcreateresourceindexerfrompreviousschemafile-function"></a><span data-ttu-id="35fbe-105">Mrmkreateresourceindexerfrompreviousschemafile-Funktion</span><span class="sxs-lookup"><span data-stu-id="35fbe-105">MrmCreateResourceIndexerFromPreviousSchemaFile function</span></span>

<span data-ttu-id="35fbe-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="35fbe-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="35fbe-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="35fbe-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="35fbe-108">Erstellt einen ressourcenindexer aus einer Schema Datei, die mit einem vorherigen Aufruf von [**mrmdumpprifile**](mrmdumpprifile.md)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="35fbe-108">Creates a resource indexer from a schema file created with a previous call to [**MrmDumpPriFile**](mrmdumpprifile.md).</span></span> <span data-ttu-id="35fbe-109">Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="35fbe-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="35fbe-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="35fbe-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousSchemaFile(
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     PCWSTR                   schemaFile,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a><span data-ttu-id="35fbe-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="35fbe-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35fbe-112">*projectroot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35fbe-112">*projectRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35fbe-113">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="35fbe-113">Type: **PCWSTR**</span></span>

<span data-ttu-id="35fbe-114">Der Projektstamm der UWP-APP, für die Sie pri-Dateien erstellen.</span><span class="sxs-lookup"><span data-stu-id="35fbe-114">The project root of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="35fbe-115">Anders ausgedrückt: der Pfad zu den Ressourcen Dateien dieser app.</span><span class="sxs-lookup"><span data-stu-id="35fbe-115">In other words, the path to that app's resource files.</span></span> <span data-ttu-id="35fbe-116">Sie geben diese Angabe an, damit Sie in nachfolgenden API-aufrufen desselben ressourcenindexers Pfade relativ zu diesem Stamm angeben können.</span><span class="sxs-lookup"><span data-stu-id="35fbe-116">You specify this so that you can then specify paths relative to that root in subsequent API calls to the same resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="35fbe-117">*platformversion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35fbe-117">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35fbe-118">Typ: **[ **mrmplatformversion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="35fbe-118">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="35fbe-119">Die Version der Zielplattform für den ressourcenindexer.</span><span class="sxs-lookup"><span data-stu-id="35fbe-119">The target platform version for the resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="35fbe-120">*defaultqualifizierer* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="35fbe-120">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="35fbe-121">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="35fbe-121">Type: **PCWSTR**</span></span>

<span data-ttu-id="35fbe-122">Eine Liste der Standard Ressourcen Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="35fbe-122">A list of default resource qualifiers.</span></span> <span data-ttu-id="35fbe-123">Beispiel: L "language-en-US \_ Scale-100 \_ Contrast-Standard"</span><span class="sxs-lookup"><span data-stu-id="35fbe-123">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="35fbe-124">*SchemaFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35fbe-124">*schemaFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35fbe-125">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="35fbe-125">Type: **PCWSTR**</span></span>

<span data-ttu-id="35fbe-126">Ein vollständiger Dateipfad zu einer Schema Datei, die durch einen vorherigen-Befehl von [**mrmdumpprifile**](mrmdumpprifile.md)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="35fbe-126">A full file path to a schema file created by a previous call to [**MrmDumpPriFile**](mrmdumpprifile.md).</span></span>

</dd> <dt>

<span data-ttu-id="35fbe-127">*Indexer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="35fbe-127">*indexer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="35fbe-128">Typ: \**[**mrmresourceindexerhandle**](mrmresourceindexerhandle.md) \** _</span><span class="sxs-lookup"><span data-stu-id="35fbe-128">Type: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\** _</span></span>

<span data-ttu-id="35fbe-129">Ein Zeiger auf ein ressourcenindexer-handle.</span><span class="sxs-lookup"><span data-stu-id="35fbe-129">A pointer to a resource indexer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35fbe-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="35fbe-130">Return value</span></span>

<span data-ttu-id="35fbe-131">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="35fbe-131">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="35fbe-132">S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert.</span><span class="sxs-lookup"><span data-stu-id="35fbe-132">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="35fbe-133">Verwenden Sie die Makros Success () oder failed () (in WinError. h definiert), um den Erfolg oder Misserfolg zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="35fbe-133">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="35fbe-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35fbe-134">Requirements</span></span>



| <span data-ttu-id="35fbe-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35fbe-135">Requirement</span></span> | <span data-ttu-id="35fbe-136">Wert</span><span class="sxs-lookup"><span data-stu-id="35fbe-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35fbe-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="35fbe-137">Minimum supported client</span></span><br/> | <span data-ttu-id="35fbe-138">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35fbe-138">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="35fbe-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="35fbe-139">Minimum supported server</span></span><br/> | <span data-ttu-id="35fbe-140">Nur Windows Server \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35fbe-140">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="35fbe-141">Header</span><span class="sxs-lookup"><span data-stu-id="35fbe-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="35fbe-142"><dt>Mrmresourceingedexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="35fbe-142"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="35fbe-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="35fbe-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="35fbe-144"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35fbe-144"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="35fbe-145">DLL</span><span class="sxs-lookup"><span data-stu-id="35fbe-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35fbe-146"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35fbe-146"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="35fbe-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35fbe-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35fbe-148">APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme</span><span class="sxs-lookup"><span data-stu-id="35fbe-148">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

