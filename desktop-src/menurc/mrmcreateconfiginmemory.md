---
title: Mrmkreateconfiginmemory-Funktion (mrmresourceingedexer. h)
description: Erstellt neue, initialisierte PRI-Konfigurationsinformationen (als in-Memory-Daten, nicht als Datei), die die von Ihnen angegebenen qualifiziererstandardwerte definieren.
ms.assetid: D8822D6E-5F68-46A1-B99F-52575DB1D277
keywords:
- Funktionen von mrmcreateconfginmemory-Funktionen und andere Ressourcen
topic_type:
- apiref
api_name:
- MrmCreateConfigInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d809ac640061ecf8bd51b9e2016aefe537b1ee8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518695"
---
# <a name="mrmcreateconfiginmemory-function"></a><span data-ttu-id="11e90-104">Mrmkreateconfginmemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="11e90-104">MrmCreateConfigInMemory function</span></span>

<span data-ttu-id="11e90-105">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="11e90-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="11e90-106">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="11e90-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="11e90-107">Erstellt neue, initialisierte PRI-Konfigurationsinformationen (als in-Memory-Daten, nicht als Datei), die die von Ihnen angegebenen qualifiziererstandardwerte definieren.</span><span class="sxs-lookup"><span data-stu-id="11e90-107">Creates new, initialized PRI configuration info (as in-memory data, not as a file) defining the qualifier defaults that you specify.</span></span> <span data-ttu-id="11e90-108">Die-Funktion ordnet Speicher zu und gibt einen Zeiger auf diesen Speicher in *outputxmldata* zurück.</span><span class="sxs-lookup"><span data-stu-id="11e90-108">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="11e90-109">Nennen Sie [**mrmfreememory**](mrmfreememory.md) mit dem gleichen Zeiger, um diesen Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="11e90-109">Call [**MrmFreeMemory**](mrmfreememory.md) with the same pointer to free that memory.</span></span> <span data-ttu-id="11e90-110">Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="11e90-110">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="11e90-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="11e90-111">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateConfigInMemory(
  _In_     MrmPlatformVersion platformVersion,
  _In_opt_ PCWSTR             defaultQualifiers,
  _Out_    BYTE               **outputXmlData,
  _Out_    ULONG              *outputXmlSize
);
```



## <a name="parameters"></a><span data-ttu-id="11e90-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="11e90-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11e90-113">*platformversion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11e90-113">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11e90-114">Typ: **[ **mrmplatformversion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="11e90-114">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="11e90-115">Die Platt Form Version (*targetosversion*), die für die generierten Konfigurationsinformationen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="11e90-115">The platform version (*targetOsVersion*) to use for the generated configuration info.</span></span>

</dd> <dt>

<span data-ttu-id="11e90-116">*defaultqualifizierer* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="11e90-116">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="11e90-117">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="11e90-117">Type: **PCWSTR**</span></span>

<span data-ttu-id="11e90-118">Eine Liste der Standard Ressourcen Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="11e90-118">A list of default resource qualifiers.</span></span> <span data-ttu-id="11e90-119">Beispiel: L "language-en-US \_ Scale-100 \_ Contrast-Standard"</span><span class="sxs-lookup"><span data-stu-id="11e90-119">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="11e90-120">*outputxmldata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="11e90-120">*outputXmlData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11e90-121">Type: **Byte \* \***</span><span class="sxs-lookup"><span data-stu-id="11e90-121">Type: **BYTE\*\***</span></span>

<span data-ttu-id="11e90-122">Die Adresse eines Zeigers auf ein Byte.</span><span class="sxs-lookup"><span data-stu-id="11e90-122">The address of a pointer to BYTE.</span></span> <span data-ttu-id="11e90-123">Die-Funktion ordnet Speicher zu und gibt einen Zeiger auf diesen Speicher in *outputxmldata* zurück.</span><span class="sxs-lookup"><span data-stu-id="11e90-123">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="11e90-124">Nennen Sie [**mrmfreememory**](mrmfreememory.md) mit dem Zeiger auf Byte, um diesen Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="11e90-124">Call [**MrmFreeMemory**](mrmfreememory.md) with your pointer to BYTE to free that memory.</span></span>

</dd> <dt>

<span data-ttu-id="11e90-125">*outputxmlsize* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="11e90-125">*outputXmlSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11e90-126">Typ: \**ulong \** _</span><span class="sxs-lookup"><span data-stu-id="11e90-126">Type: \**ULONG\** _</span></span>

<span data-ttu-id="11e90-127">Die Adresse eines ulong.</span><span class="sxs-lookup"><span data-stu-id="11e90-127">The address of a ULONG.</span></span> <span data-ttu-id="11e90-128">In _outputXmlSize \* gibt die-Funktion die Größe des belegten Speichers zurück, auf den von *outputxmldata* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="11e90-128">In _outputXmlSize\*, the function returns the size of the allocated memory pointed to by *outputXmlData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11e90-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11e90-129">Return value</span></span>

<span data-ttu-id="11e90-130">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="11e90-130">Type: **HRESULT**</span></span>

<span data-ttu-id="11e90-131">S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert.</span><span class="sxs-lookup"><span data-stu-id="11e90-131">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="11e90-132">Verwenden Sie die Makros Success () oder failed () (in WinError. h definiert), um den Erfolg oder Misserfolg zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="11e90-132">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="11e90-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11e90-133">Requirements</span></span>



| <span data-ttu-id="11e90-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11e90-134">Requirement</span></span> | <span data-ttu-id="11e90-135">Wert</span><span class="sxs-lookup"><span data-stu-id="11e90-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11e90-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11e90-136">Minimum supported client</span></span><br/> | <span data-ttu-id="11e90-137">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11e90-137">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="11e90-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11e90-138">Minimum supported server</span></span><br/> | <span data-ttu-id="11e90-139">Nur Windows Server \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11e90-139">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="11e90-140">Header</span><span class="sxs-lookup"><span data-stu-id="11e90-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="11e90-141"><dt>Mrmresourceingedexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="11e90-141"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="11e90-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="11e90-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="11e90-143"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11e90-143"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="11e90-144">DLL</span><span class="sxs-lookup"><span data-stu-id="11e90-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11e90-145"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11e90-145"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="11e90-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11e90-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11e90-147">APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme</span><span class="sxs-lookup"><span data-stu-id="11e90-147">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

