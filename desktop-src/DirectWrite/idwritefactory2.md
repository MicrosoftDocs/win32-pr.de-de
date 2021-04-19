---
title: IDWriteFactory2-Schnittstelle
description: Die Root Factory-Schnittstelle für alle DirectWrite-Objekte.
ms.assetid: 1D3EEC28-EAB3-4FA2-98E9-7A8FDAF6E6FE
keywords:
- IDWriteFactory1 Interface Direct Write
- IDWriteFactory1 Interface Direct Write, beschrieben
topic_type:
- apiref
api_name:
- IDWriteFactory1
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7d5ba0f8d480981ab6ebea6dcdbd955b7b967e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339983"
---
# <a name="idwritefactory2-interface"></a><span data-ttu-id="ccc33-105">IDWriteFactory2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ccc33-105">IDWriteFactory2 interface</span></span>

<span data-ttu-id="ccc33-106">Die Root Factory-Schnittstelle für alle [DirectWrite](direct-write-portal.md) -Objekte.</span><span class="sxs-lookup"><span data-stu-id="ccc33-106">The root factory interface for all [DirectWrite](direct-write-portal.md) objects.</span></span>

## <a name="members"></a><span data-ttu-id="ccc33-107">Member</span><span class="sxs-lookup"><span data-stu-id="ccc33-107">Members</span></span>

<span data-ttu-id="ccc33-108">Die **IDWriteFactory1** -Schnittstelle erbt von [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1).</span><span class="sxs-lookup"><span data-stu-id="ccc33-108">The **IDWriteFactory1** interface inherits from [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1).</span></span> <span data-ttu-id="ccc33-109">**IDWriteFactory2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ccc33-109">**IDWriteFactory2** also has these types of members:</span></span>

-   [<span data-ttu-id="ccc33-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="ccc33-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ccc33-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="ccc33-111">Methods</span></span>

<span data-ttu-id="ccc33-112">Die **IDWriteFactory1** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="ccc33-112">The **IDWriteFactory1** interface has these methods.</span></span>



| <span data-ttu-id="ccc33-113">Methode</span><span class="sxs-lookup"><span data-stu-id="ccc33-113">Method</span></span>                                                                             | <span data-ttu-id="ccc33-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ccc33-114">Description</span></span>                                                                                                |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ccc33-115">**"Kreatecustomrenderingpara"**</span><span class="sxs-lookup"><span data-stu-id="ccc33-115">**CreateCustomRenderingParams**</span></span>](idwritefactory2-createcustomrenderingparams.md) | <span data-ttu-id="ccc33-116">Erstellt ein Renderparameter-Objekt mit den angegebenen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ccc33-116">Creates a rendering parameters object with the specified properties.</span></span><br/>                            |
| [<span data-ttu-id="ccc33-117">**"Kreatefontfallbackbuilder"**</span><span class="sxs-lookup"><span data-stu-id="ccc33-117">**CreateFontFallbackBuilder**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-createfontfallbackbuilder)     | <span data-ttu-id="ccc33-118">Erstellt ein Schriftart Fall Back Builder-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ccc33-118">Creates a font fallback builder object.</span></span><br/>                                                         |
| [<span data-ttu-id="ccc33-119">**"Kreateglyphrunanalysis"**</span><span class="sxs-lookup"><span data-stu-id="ccc33-119">**CreateGlyphRunAnalysis**</span></span>](idwritefactory2-createglyphrunanalysis.md)           | <span data-ttu-id="ccc33-120">Erstellt ein Symbol zum Ausführen von Symbolen, das Informationen kapselt, die zum renderischen Ausführen von Symbolen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ccc33-120">Creates a glyph run analysis object, which encapsulates information used to render a glyph run.</span></span><br/> |
| [<span data-ttu-id="ccc33-121">**Getsystemfontfallback**</span><span class="sxs-lookup"><span data-stu-id="ccc33-121">**GetSystemFontFallback**</span></span>](idwritefactory2-getsystemfontfallback.md)             | <span data-ttu-id="ccc33-122">Erstellt ein Schriftart Fall Back Objekt aus der System Schriftart-fallbackliste.</span><span class="sxs-lookup"><span data-stu-id="ccc33-122">Creates a font fallback object from the system font fallback list.</span></span><br/>                              |
| [<span data-ttu-id="ccc33-123">**Translatecolorglyphrun**</span><span class="sxs-lookup"><span data-stu-id="ccc33-123">**TranslateColorGlyphRun**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-translatecolorglyphrun)           | <span data-ttu-id="ccc33-124">Diese Methode wird für eine Glyphe-Ausführung aufgerufen, um Sie in mehrere Farb Symbol Ausführungen umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="ccc33-124">This method is called on a glyph run to translate it in to multiple color glyph runs.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="ccc33-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ccc33-125">Requirements</span></span>



| <span data-ttu-id="ccc33-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ccc33-126">Requirement</span></span> | <span data-ttu-id="ccc33-127">Wert</span><span class="sxs-lookup"><span data-stu-id="ccc33-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccc33-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ccc33-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ccc33-129">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="ccc33-129">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="ccc33-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ccc33-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ccc33-131">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="ccc33-131">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="ccc33-132">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="ccc33-132">Minimum supported phone</span></span><br/>  | <span data-ttu-id="ccc33-133">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="ccc33-133">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="ccc33-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ccc33-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="ccc33-135"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ccc33-135"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ccc33-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ccc33-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccc33-137"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccc33-137"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ccc33-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ccc33-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccc33-139">**IDWriteFactory1**</span><span class="sxs-lookup"><span data-stu-id="ccc33-139">**IDWriteFactory1**</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1)
</dt> <dt>

[<span data-ttu-id="ccc33-140">**Idschreitefactory**</span><span class="sxs-lookup"><span data-stu-id="ccc33-140">**IDWriteFactory**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)
</dt> </dl>

 

