---
title: Mrmdumpprifile-Funktion (mrmresourceindexer. h)
description: Sichert eine PRI-Datei (die binär ist) in Ihre XML-Entsprechung (als Datei auf dem Datenträger), um Sie leichter lesbar zu machen.
ms.assetid: FE1982AB-881C-4F07-8B9E-E3770E5B5099
keywords:
- Funktionen der mrmdumpprifile-Funktion und weitere Ressourcen
topic_type:
- apiref
api_name:
- MrmDumpPriFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba254cbac0dd8afd328e0d7e04f573138f14b588
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741825"
---
# <a name="mrmdumpprifile-function"></a><span data-ttu-id="e19be-104">Mrmdumpprifile-Funktion</span><span class="sxs-lookup"><span data-stu-id="e19be-104">MrmDumpPriFile function</span></span>

<span data-ttu-id="e19be-105">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="e19be-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e19be-106">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="e19be-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e19be-107">Sichert eine PRI-Datei (die binär ist) in Ihre XML-Entsprechung (als Datei auf dem Datenträger), um Sie leichter lesbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="e19be-107">Dumps a PRI file (which is binary) to its XML equivalent (as a file on disk), in order to make it more easily readable.</span></span> <span data-ttu-id="e19be-108">Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="e19be-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="e19be-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e19be-109">Syntax</span></span>


```C++
HRESULT HRESULT MrmDumpPriFile(
  _In_     PCWSTR      indexFileName,
  _In_opt_ PCWSTR      schemaPriFile,
  _In_     MrmDumpType dumpType,
  _In_     PCWSTR      outputXmlFile
);
```



## <a name="parameters"></a><span data-ttu-id="e19be-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e19be-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e19be-111">*indexfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e19be-111">*indexFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e19be-112">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="e19be-112">Type: **PCWSTR**</span></span>

<span data-ttu-id="e19be-113">Ein vollständiger Dateipfad zu einer PRI-Datei.</span><span class="sxs-lookup"><span data-stu-id="e19be-113">A full file path to a PRI file.</span></span> <span data-ttu-id="e19be-114">Dies ist die PRI-Datei, die in XML gekippt wird.</span><span class="sxs-lookup"><span data-stu-id="e19be-114">This is the PRI file that will be dumped to XML.</span></span>

</dd> <dt>

<span data-ttu-id="e19be-115">*schemaprifile* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="e19be-115">*schemaPriFile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e19be-116">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="e19be-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="e19be-117">Ein optionaler Vollständiger Dateipfad zu einer Schema Datei (oder zu einer PRI-Datei, die ein Schema darstellt. siehe Hinweise).</span><span class="sxs-lookup"><span data-stu-id="e19be-117">An optional full file path to a schema file (or to a PRI file representing a schema; see Remarks).</span></span>

</dd> <dt>

<span data-ttu-id="e19be-118">*dumptype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e19be-118">*dumpType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e19be-119">Typ: **[ **mrmdumptype**](mrmdumptype.md)**</span><span class="sxs-lookup"><span data-stu-id="e19be-119">Type: **[**MrmDumpType**](mrmdumptype.md)**</span></span>

<span data-ttu-id="e19be-120">Gibt an, wie detailliert das XML-Dump sein soll oder ob ein Schema gekippt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e19be-120">Specifies how detailed the XML dump should be, or whether a schema should be dumped.</span></span>

</dd> <dt>

<span data-ttu-id="e19be-121">*outputxmlfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e19be-121">*outputXmlFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e19be-122">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="e19be-122">Type: **PCWSTR**</span></span>

<span data-ttu-id="e19be-123">Der Pfad einer XML-Datei, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e19be-123">The path of an XML file to create.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e19be-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e19be-124">Return value</span></span>

<span data-ttu-id="e19be-125">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e19be-125">Type: **HRESULT**</span></span>

<span data-ttu-id="e19be-126">S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert.</span><span class="sxs-lookup"><span data-stu-id="e19be-126">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="e19be-127">Verwenden Sie die Makros Success () oder failed () (in WinError. h definiert), um den Erfolg oder Misserfolg zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="e19be-127">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="e19be-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e19be-128">Remarks</span></span>

<span data-ttu-id="e19be-129">Ein Schema freies Ressourcenpaket, das mit dem " [**mrmpackagingoptionsomitschemafromresourcepacks**](mrmpackagingoptions.md) "-Argument erstellt wurde, das an [**mrmkreateresourcefile**](mrmcreateresourcefile.md) oder [**mrmkreateresourcefileinmemory**](mrmcreateresourcefileinmemory.md) übergeben wurde (oder mit dem Schalter *omitschemafromresourcepacks* in der PRI-Konfigurationsdatei).</span><span class="sxs-lookup"><span data-stu-id="e19be-129">A schema-free resource pack is one that was created with the [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) argument passed to [**MrmCreateResourceFile**](mrmcreateresourcefile.md) or [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (or with the *omitSchemaFromResourcePacks* switch in the PRI config file).</span></span> <span data-ttu-id="e19be-130">Zum Sichern eines Ressourcen Pakets mit Schema freiem Speicher übergeben Sie den Pfad zu ihren Hauptpaket-PRI-Daten als Argument für den *schemaprifile* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="e19be-130">To dump a schema-free resource pack, pass the path to your main package PRI data as the argument for the *schemaPriFile* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="e19be-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e19be-131">Requirements</span></span>



| <span data-ttu-id="e19be-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e19be-132">Requirement</span></span> | <span data-ttu-id="e19be-133">Wert</span><span class="sxs-lookup"><span data-stu-id="e19be-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e19be-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e19be-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e19be-135">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e19be-135">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e19be-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e19be-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e19be-137">Nur Windows Server \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e19be-137">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e19be-138">Header</span><span class="sxs-lookup"><span data-stu-id="e19be-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="e19be-139"><dt>Mrmresourceingedexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="e19be-139"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="e19be-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e19be-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="e19be-141"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e19be-141"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="e19be-142">DLL</span><span class="sxs-lookup"><span data-stu-id="e19be-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e19be-143"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e19be-143"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="e19be-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e19be-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e19be-145">APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme</span><span class="sxs-lookup"><span data-stu-id="e19be-145">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

