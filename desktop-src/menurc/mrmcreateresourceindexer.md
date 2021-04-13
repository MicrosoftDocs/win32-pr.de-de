---
title: Mrmkreateresourceingedexer-Funktion (mrmresourceingedexer. h)
description: Erstellt einen ressourcenindexer, der zum Generieren von PRI-Dateien (Package Resource Index) für eine UWP-App verwendet wird. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme.
ms.assetid: 9AE3EF90-4ADC-4646-9C62-87A702333B9A
keywords:
- Funktionen von mrmcreateresourcindexer Functions und andere Ressourcen
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexer
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5240112c3fef6e358cfbc90638ef867108aabeb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392144"
---
# <a name="mrmcreateresourceindexer-function"></a><span data-ttu-id="78c64-105">Mrmkreateresourceingedexer-Funktion</span><span class="sxs-lookup"><span data-stu-id="78c64-105">MrmCreateResourceIndexer function</span></span>

<span data-ttu-id="78c64-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="78c64-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="78c64-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="78c64-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="78c64-108">Erstellt einen ressourcenindexer, der zum Generieren von PRI-Dateien (Package Resource Index) für eine UWP-App verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="78c64-108">Creates a resource indexer, used to generate package resource index (PRI) files for a UWP app.</span></span> <span data-ttu-id="78c64-109">Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="78c64-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="78c64-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="78c64-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceIndexer(
  _In_     PCWSTR                   packageFamilyName,
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a><span data-ttu-id="78c64-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="78c64-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78c64-112">*packagefamilyname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78c64-112">*packageFamilyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78c64-113">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="78c64-113">Type: **PCWSTR**</span></span>

<span data-ttu-id="78c64-114">Der Paket Familienname der UWP-APP, für die Sie pri-Dateien erstellen.</span><span class="sxs-lookup"><span data-stu-id="78c64-114">The package family name of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="78c64-115">Dieser Wert wird als Ressourcen Zuordnungs Name verwendet, wenn Sie später eine PRI-Datei von diesem ressourcenindexer generieren.</span><span class="sxs-lookup"><span data-stu-id="78c64-115">This value will be used as the resource map name when you later generate a PRI file from this resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="78c64-116">*projectroot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78c64-116">*projectRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78c64-117">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="78c64-117">Type: **PCWSTR**</span></span>

<span data-ttu-id="78c64-118">Der Projektstamm der UWP-APP, für die Sie pri-Dateien erstellen.</span><span class="sxs-lookup"><span data-stu-id="78c64-118">The project root of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="78c64-119">Anders ausgedrückt: der Pfad zu den Ressourcen Dateien dieser app.</span><span class="sxs-lookup"><span data-stu-id="78c64-119">In other words, the path to that app's resource files.</span></span> <span data-ttu-id="78c64-120">Sie geben diese Angabe an, damit Sie in nachfolgenden API-aufrufen desselben ressourcenindexers Pfade relativ zu diesem Stamm angeben können.</span><span class="sxs-lookup"><span data-stu-id="78c64-120">You specify this so that you can then specify paths relative to that root in subsequent API calls to the same resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="78c64-121">*platformversion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78c64-121">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78c64-122">Typ: **[ **mrmplatformversion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="78c64-122">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="78c64-123">Die Version der Zielplattform für den ressourcenindexer.</span><span class="sxs-lookup"><span data-stu-id="78c64-123">The target platform version for the resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="78c64-124">*defaultqualifizierer* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="78c64-124">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="78c64-125">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="78c64-125">Type: **PCWSTR**</span></span>

<span data-ttu-id="78c64-126">Eine Liste der Standard Ressourcen Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="78c64-126">A list of default resource qualifiers.</span></span> <span data-ttu-id="78c64-127">Beispiel: L "language-en-US \_ Scale-100 \_ Contrast-Standard"</span><span class="sxs-lookup"><span data-stu-id="78c64-127">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="78c64-128">*Indexer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="78c64-128">*indexer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="78c64-129">Typ: \**[**mrmresourceindexerhandle**](mrmresourceindexerhandle.md) \** _</span><span class="sxs-lookup"><span data-stu-id="78c64-129">Type: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\** _</span></span>

<span data-ttu-id="78c64-130">Ein Zeiger auf ein ressourcenindexer-handle.</span><span class="sxs-lookup"><span data-stu-id="78c64-130">A pointer to a resource indexer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78c64-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78c64-131">Return value</span></span>

<span data-ttu-id="78c64-132">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="78c64-132">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="78c64-133">S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert.</span><span class="sxs-lookup"><span data-stu-id="78c64-133">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="78c64-134">Verwenden Sie die Makros Success () oder failed () (in WinError. h definiert), um den Erfolg oder Misserfolg zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="78c64-134">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="78c64-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78c64-135">Requirements</span></span>



| <span data-ttu-id="78c64-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78c64-136">Requirement</span></span> | <span data-ttu-id="78c64-137">Wert</span><span class="sxs-lookup"><span data-stu-id="78c64-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78c64-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="78c64-138">Minimum supported client</span></span><br/> | <span data-ttu-id="78c64-139">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="78c64-139">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="78c64-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="78c64-140">Minimum supported server</span></span><br/> | <span data-ttu-id="78c64-141">Nur Windows Server \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="78c64-141">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="78c64-142">Header</span><span class="sxs-lookup"><span data-stu-id="78c64-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="78c64-143"><dt>Mrmresourceingedexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="78c64-143"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="78c64-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="78c64-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="78c64-145"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="78c64-145"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="78c64-146">DLL</span><span class="sxs-lookup"><span data-stu-id="78c64-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78c64-147"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78c64-147"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="78c64-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78c64-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78c64-149">APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme</span><span class="sxs-lookup"><span data-stu-id="78c64-149">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

