---
title: Mrmdumpprifilinput Memory-Funktion (mrmresourceingedexer. h)
description: Sichert eine PRI-Datei (die binär ist) in Ihre XML-Entsprechung (als in-Memory-Daten), um Sie leichter lesbar zu machen.
ms.assetid: 04FD048F-1473-47B1-9CAB-03FEF98A9B48
keywords:
- Funktionen von "mrmdumpprifilinput Memory" und weitere Ressourcen
topic_type:
- apiref
api_name:
- MrmDumpPriFileInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 253db38bf1e272f21ff66210bdbd07d5a33f4c60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338118"
---
# <a name="mrmdumpprifileinmemory-function"></a><span data-ttu-id="8bc68-104">Mrmdumpprifilinput Memory-Funktion</span><span class="sxs-lookup"><span data-stu-id="8bc68-104">MrmDumpPriFileInMemory function</span></span>

<span data-ttu-id="8bc68-105">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="8bc68-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8bc68-106">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="8bc68-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8bc68-107">Sichert eine PRI-Datei (die binär ist) in Ihre XML-Entsprechung (als in-Memory-Daten), um Sie leichter lesbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="8bc68-107">Dumps a PRI file (which is binary) to its XML equivalent (as in-memory data), in order to make it more easily readable.</span></span> <span data-ttu-id="8bc68-108">Die-Funktion ordnet Speicher zu und gibt einen Zeiger auf diesen Speicher in *outputxmldata* zurück.</span><span class="sxs-lookup"><span data-stu-id="8bc68-108">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="8bc68-109">Nennen Sie [**mrmfreememory**](mrmfreememory.md) mit dem gleichen Zeiger, um diesen Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="8bc68-109">Call [**MrmFreeMemory**](mrmfreememory.md) with the same pointer to free that memory.</span></span> <span data-ttu-id="8bc68-110">Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="8bc68-110">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="8bc68-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="8bc68-111">Syntax</span></span>


```C++
HRESULT HRESULT MrmDumpPriFileInMemory(
  _In_     PCWSTR      indexFileName,
  _In_opt_ PCWSTR      schemaPriFile,
  _In_     MrmDumpType dumpType,
  _Out_    BYTE        **outputXmlData,
  _Out_    ULONG       *outputXmlSize
);
```



## <a name="parameters"></a><span data-ttu-id="8bc68-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8bc68-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bc68-113">*indexfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8bc68-113">*indexFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bc68-114">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="8bc68-114">Type: **PCWSTR**</span></span>

<span data-ttu-id="8bc68-115">Ein vollständiger Dateipfad zu einer PRI-Datei.</span><span class="sxs-lookup"><span data-stu-id="8bc68-115">A full file path to a PRI file.</span></span> <span data-ttu-id="8bc68-116">Dies ist die PRI-Datei, die in XML gekippt wird.</span><span class="sxs-lookup"><span data-stu-id="8bc68-116">This is the PRI file that will be dumped to XML.</span></span>

</dd> <dt>

<span data-ttu-id="8bc68-117">*schemaprifile* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="8bc68-117">*schemaPriFile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8bc68-118">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="8bc68-118">Type: **PCWSTR**</span></span>

<span data-ttu-id="8bc68-119">Ein optionaler Vollständiger Dateipfad zu einer Schema Datei (oder zu einer PRI-Datei, die ein Schema darstellt. siehe Hinweise).</span><span class="sxs-lookup"><span data-stu-id="8bc68-119">An optional full file path to a schema file (or to a PRI file representing a schema; see Remarks).</span></span>

</dd> <dt>

<span data-ttu-id="8bc68-120">*dumptype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8bc68-120">*dumpType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bc68-121">Typ: **[ **mrmdumptype**](mrmdumptype.md)**</span><span class="sxs-lookup"><span data-stu-id="8bc68-121">Type: **[**MrmDumpType**](mrmdumptype.md)**</span></span>

<span data-ttu-id="8bc68-122">Gibt an, wie detailliert das XML-Dump sein soll oder ob ein Schema gekippt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8bc68-122">Specifies how detailed the XML dump should be, or whether a schema should be dumped.</span></span>

</dd> <dt>

<span data-ttu-id="8bc68-123">*outputxmldata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8bc68-123">*outputXmlData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8bc68-124">Type: **Byte \* \***</span><span class="sxs-lookup"><span data-stu-id="8bc68-124">Type: **BYTE\*\***</span></span>

<span data-ttu-id="8bc68-125">Die Adresse eines Zeigers auf ein Byte.</span><span class="sxs-lookup"><span data-stu-id="8bc68-125">The address of a pointer to BYTE.</span></span> <span data-ttu-id="8bc68-126">Die-Funktion ordnet Speicher zu und gibt einen Zeiger auf diesen Speicher in *outputxmldata* zurück.</span><span class="sxs-lookup"><span data-stu-id="8bc68-126">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="8bc68-127">Nennen Sie [**mrmfreememory**](mrmfreememory.md) mit dem Zeiger auf Byte, um diesen Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="8bc68-127">Call [**MrmFreeMemory**](mrmfreememory.md) with your pointer to BYTE to free that memory.</span></span>

</dd> <dt>

<span data-ttu-id="8bc68-128">*outputxmlsize* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8bc68-128">*outputXmlSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8bc68-129">Typ: \**ulong \** _</span><span class="sxs-lookup"><span data-stu-id="8bc68-129">Type: \**ULONG\** _</span></span>

<span data-ttu-id="8bc68-130">Die Adresse eines ulong.</span><span class="sxs-lookup"><span data-stu-id="8bc68-130">The address of a ULONG.</span></span> <span data-ttu-id="8bc68-131">In _outputXmlSize \* gibt die-Funktion die Größe des belegten Speichers zurück, auf den von *outputxmldata* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="8bc68-131">In _outputXmlSize\*, the function returns the size of the allocated memory pointed to by *outputXmlData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bc68-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8bc68-132">Return value</span></span>

<span data-ttu-id="8bc68-133">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8bc68-133">Type: **HRESULT**</span></span>

<span data-ttu-id="8bc68-134">S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert.</span><span class="sxs-lookup"><span data-stu-id="8bc68-134">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="8bc68-135">Verwenden Sie die Makros Success () oder failed () (in WinError. h definiert), um den Erfolg oder Misserfolg zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="8bc68-135">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bc68-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8bc68-136">Remarks</span></span>

<span data-ttu-id="8bc68-137">Ein Schema freies Ressourcenpaket, das mit dem " [**mrmpackagingoptionsomitschemafromresourcepacks**](mrmpackagingoptions.md) "-Argument erstellt wurde, das an [**mrmkreateresourcefile**](mrmcreateresourcefile.md) oder [**mrmkreateresourcefileinmemory**](mrmcreateresourcefileinmemory.md) übergeben wurde (oder mit dem Schalter *omitschemafromresourcepacks* in der PRI-Konfigurationsdatei).</span><span class="sxs-lookup"><span data-stu-id="8bc68-137">A schema-free resource pack is one that was created with the [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) argument passed to [**MrmCreateResourceFile**](mrmcreateresourcefile.md) or [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (or with the *omitSchemaFromResourcePacks* switch in the PRI config file).</span></span> <span data-ttu-id="8bc68-138">Zum Sichern eines Ressourcen Pakets mit Schema freiem Speicher übergeben Sie den Pfad zu ihren Hauptpaket-PRI-Daten als Argument für den *schemaprifile* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="8bc68-138">To dump a schema-free resource pack, pass the path to your main package PRI data as the argument for the *schemaPriFile* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bc68-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8bc68-139">Requirements</span></span>



| <span data-ttu-id="8bc68-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8bc68-140">Requirement</span></span> | <span data-ttu-id="8bc68-141">Wert</span><span class="sxs-lookup"><span data-stu-id="8bc68-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bc68-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8bc68-142">Minimum supported client</span></span><br/> | <span data-ttu-id="8bc68-143">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8bc68-143">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="8bc68-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8bc68-144">Minimum supported server</span></span><br/> | <span data-ttu-id="8bc68-145">Nur Windows Server \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8bc68-145">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8bc68-146">Header</span><span class="sxs-lookup"><span data-stu-id="8bc68-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bc68-147"><dt>Mrmresourceingedexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bc68-147"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="8bc68-148">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8bc68-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="8bc68-149"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8bc68-149"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="8bc68-150">DLL</span><span class="sxs-lookup"><span data-stu-id="8bc68-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bc68-151"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bc68-151"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="8bc68-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8bc68-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bc68-153">APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme</span><span class="sxs-lookup"><span data-stu-id="8bc68-153">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

