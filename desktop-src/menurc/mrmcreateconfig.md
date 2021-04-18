---
title: Mrmkreateconfig-Funktion (mrmresourceingedexer. h)
description: Erstellt eine neue, initialisierte PRI-Konfigurationsdatei, die die von Ihnen angegebenen qualifiziererstandardwerte definiert. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme.
ms.assetid: F8FB4E9C-1C04-460A-BFA1-FB663653DA3C
keywords:
- Mrmcreateconfig-Funktions Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- MrmCreateConfig
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3adb270d9bbd9194822181314a697fa1d267a127
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339365"
---
# <a name="mrmcreateconfig-function"></a><span data-ttu-id="6d078-105">Mrmkreateconfig-Funktion</span><span class="sxs-lookup"><span data-stu-id="6d078-105">MrmCreateConfig function</span></span>

<span data-ttu-id="6d078-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="6d078-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6d078-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="6d078-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6d078-108">Erstellt eine neue, initialisierte PRI-Konfigurationsdatei, die die von Ihnen angegebenen qualifiziererstandardwerte definiert.</span><span class="sxs-lookup"><span data-stu-id="6d078-108">Creates a new, initialized PRI config file defining the qualifier defaults that you specify.</span></span> <span data-ttu-id="6d078-109">Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="6d078-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="6d078-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d078-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateConfig(
  _In_     MrmPlatformVersion platformVersion,
  _In_opt_ PCWSTR             defaultQualifiers,
  _In_     PCWSTR             outputXmlFile
);
```



## <a name="parameters"></a><span data-ttu-id="6d078-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d078-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d078-112">*platformversion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d078-112">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d078-113">Typ: **[ **mrmplatformversion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="6d078-113">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="6d078-114">Die Platt Form Version (*targetosversion*), die für die generierte Konfigurationsdatei verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6d078-114">The platform version (*targetOsVersion*) to use for the generated configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="6d078-115">*defaultqualifizierer* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="6d078-115">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6d078-116">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="6d078-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="6d078-117">Eine Liste der Standard Ressourcen Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="6d078-117">A list of default resource qualifiers.</span></span> <span data-ttu-id="6d078-118">Beispiel: L "language-en-US \_ Scale-100 \_ Contrast-Standard"</span><span class="sxs-lookup"><span data-stu-id="6d078-118">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="6d078-119">*outputxmlfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d078-119">*outputXmlFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d078-120">Typ: **pcwstr**</span><span class="sxs-lookup"><span data-stu-id="6d078-120">Type: **PCWSTR**</span></span>

<span data-ttu-id="6d078-121">Der Pfad der zu erstellenden Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="6d078-121">The path of the configuration file to create.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d078-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6d078-122">Return value</span></span>

<span data-ttu-id="6d078-123">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6d078-123">Type: **HRESULT**</span></span>

<span data-ttu-id="6d078-124">S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert.</span><span class="sxs-lookup"><span data-stu-id="6d078-124">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="6d078-125">Verwenden Sie die Makros Success () oder failed () (in WinError. h definiert), um den Erfolg oder Misserfolg zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="6d078-125">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d078-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d078-126">Requirements</span></span>



| <span data-ttu-id="6d078-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d078-127">Requirement</span></span> | <span data-ttu-id="6d078-128">Wert</span><span class="sxs-lookup"><span data-stu-id="6d078-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d078-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6d078-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6d078-130">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d078-130">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6d078-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6d078-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6d078-132">Nur Windows Server \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d078-132">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6d078-133">Header</span><span class="sxs-lookup"><span data-stu-id="6d078-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d078-134"><dt>Mrmresourceingedexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d078-134"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="6d078-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6d078-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="6d078-136"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d078-136"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="6d078-137">DLL</span><span class="sxs-lookup"><span data-stu-id="6d078-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d078-138"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d078-138"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="6d078-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d078-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d078-140">APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme</span><span class="sxs-lookup"><span data-stu-id="6d078-140">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

