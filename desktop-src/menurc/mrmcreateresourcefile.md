---
title: Mrmkreateresourcefile-Funktion (mrmresourceindexer. h)
description: Erstellt eine PRI-Datei (mit dem Namen \ 0034; Resources. pri \ 0034;) oder Dateien auf dem Datenträger im angegebenen Ordner. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme.
ms.assetid: B9CE0638-4650-4E1A-BE5E-4CC7C6614030
keywords:
- Mrmcreateresourcefile-Funktions Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MrmCreateResourceFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80294e5829dbf90c8aa3b0f6485c2da4185add1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743064"
---
# <a name="mrmcreateresourcefile-function"></a><span data-ttu-id="bfa18-105">Mrmkreateresourcefile-Funktion</span><span class="sxs-lookup"><span data-stu-id="bfa18-105">MrmCreateResourceFile function</span></span>

<span data-ttu-id="bfa18-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="bfa18-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bfa18-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="bfa18-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bfa18-108">Erstellt eine PRI-Datei (mit dem Namen "Resources. pri") oder Dateien auf dem Datenträger im angegebenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="bfa18-108">Creates a PRI file (named "resources.pri"), or files, on disk in the specified folder.</span></span> <span data-ttu-id="bfa18-109">Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="bfa18-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="bfa18-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="bfa18-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceFile(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ MrmPackagingMode         packagingMode,
  _In_ MrmPackagingOptions      packagingOptions,
       PCWSTR                   outputDirectory
);
```



## <a name="parameters"></a><span data-ttu-id="bfa18-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="bfa18-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfa18-112">*Indexer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bfa18-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfa18-113">Typ: **[ **mrmresourceindexerhandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="bfa18-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="bfa18-114">Ein Handle, das den ressourcenindexer identifiziert, von dem die PRI-Datei erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bfa18-114">A handle identifying the resource indexer from which to create the PRI file.</span></span>

</dd> <dt>

<span data-ttu-id="bfa18-115">*packagingmode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bfa18-115">*packagingMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfa18-116">Typ: **[ **mrmpackagingmode**](mrmpackagingmode.md)**</span><span class="sxs-lookup"><span data-stu-id="bfa18-116">Type: **[**MrmPackagingMode**](mrmpackagingmode.md)**</span></span>

<span data-ttu-id="bfa18-117">Gibt an, ob die PRI-Datei eigenständig sein soll, automatisch nach Ressourcen Qualifizierer aufgeteilt werden oder ein Ressourcenpaket sein soll.</span><span class="sxs-lookup"><span data-stu-id="bfa18-117">Specifies whether the PRI file should be standalone, be automatically split by resource qualifier, or be a resource pack.</span></span>

</dd> <dt>

<span data-ttu-id="bfa18-118">*packagingoptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bfa18-118">*packagingOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfa18-119">Typ: **[ **mrmpackagingoptions**](mrmpackagingoptions.md)**</span><span class="sxs-lookup"><span data-stu-id="bfa18-119">Type: **[**MrmPackagingOptions**](mrmpackagingoptions.md)**</span></span>

<span data-ttu-id="bfa18-120">Gibt zusätzliche Optionen zur PRI-Datei an.</span><span class="sxs-lookup"><span data-stu-id="bfa18-120">Specifies additional options about the PRI file.</span></span>

</dd> <dt>

<span data-ttu-id="bfa18-121">*OutputDirectory*</span><span class="sxs-lookup"><span data-stu-id="bfa18-121">*outputDirectory*</span></span> 
</dt> <dd>

<span data-ttu-id="bfa18-122">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="bfa18-122">Type: **PCWSTR**</span></span>

<span data-ttu-id="bfa18-123">Ein Pfad zu einem Ordner, in dem die PRI-Datei gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bfa18-123">A path to a folder in which to save the PRI file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfa18-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bfa18-124">Return value</span></span>

<span data-ttu-id="bfa18-125">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bfa18-125">Type: **HRESULT**</span></span>

<span data-ttu-id="bfa18-126">S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert.</span><span class="sxs-lookup"><span data-stu-id="bfa18-126">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="bfa18-127">Verwenden Sie die Makros Success () oder failed () (in WinError. h definiert), um den Erfolg oder Misserfolg zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="bfa18-127">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfa18-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bfa18-128">Requirements</span></span>



| <span data-ttu-id="bfa18-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bfa18-129">Requirement</span></span> | <span data-ttu-id="bfa18-130">Wert</span><span class="sxs-lookup"><span data-stu-id="bfa18-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfa18-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bfa18-131">Minimum supported client</span></span><br/> | <span data-ttu-id="bfa18-132">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bfa18-132">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="bfa18-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bfa18-133">Minimum supported server</span></span><br/> | <span data-ttu-id="bfa18-134">Nur Windows Server \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bfa18-134">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bfa18-135">Header</span><span class="sxs-lookup"><span data-stu-id="bfa18-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfa18-136"><dt>Mrmresourceingedexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfa18-136"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="bfa18-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bfa18-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="bfa18-138"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bfa18-138"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="bfa18-139">DLL</span><span class="sxs-lookup"><span data-stu-id="bfa18-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfa18-140"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfa18-140"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="bfa18-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bfa18-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfa18-142">APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme</span><span class="sxs-lookup"><span data-stu-id="bfa18-142">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

