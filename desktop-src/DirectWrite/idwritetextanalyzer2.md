---
title: IDWriteTextAnalyzer2-Schnittstelle
description: Analysiert verschiedene Texteigenschaften für die Verarbeitung komplexer Skripts.
ms.assetid: 62DF6E71-F99D-47E9-A9BE-2A481A60AEDD
keywords:
- IDWriteTextAnalyzer2 Interface Direct Write
- IDWriteTextAnalyzer2 Interface Direct Write, beschrieben
topic_type:
- apiref
api_name:
- IDWriteTextAnalyzer2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2548cc7961c8d866d4067e794e033701457d5b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518107"
---
# <a name="idwritetextanalyzer2-interface"></a><span data-ttu-id="30c7a-105">IDWriteTextAnalyzer2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="30c7a-105">IDWriteTextAnalyzer2 interface</span></span>

<span data-ttu-id="30c7a-106">Analysiert verschiedene Texteigenschaften für die Verarbeitung komplexer Skripts.</span><span class="sxs-lookup"><span data-stu-id="30c7a-106">Analyzes various text properties for complex script processing.</span></span>

## <a name="members"></a><span data-ttu-id="30c7a-107">Member</span><span class="sxs-lookup"><span data-stu-id="30c7a-107">Members</span></span>

<span data-ttu-id="30c7a-108">Die **IDWriteTextAnalyzer2** -Schnittstelle erbt von [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1).</span><span class="sxs-lookup"><span data-stu-id="30c7a-108">The **IDWriteTextAnalyzer2** interface inherits from [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1).</span></span> <span data-ttu-id="30c7a-109">**IDWriteTextAnalyzer2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="30c7a-109">**IDWriteTextAnalyzer2** also has these types of members:</span></span>

-   [<span data-ttu-id="30c7a-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="30c7a-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="30c7a-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="30c7a-111">Methods</span></span>

<span data-ttu-id="30c7a-112">Die **IDWriteTextAnalyzer2** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="30c7a-112">The **IDWriteTextAnalyzer2** interface has these methods.</span></span>



| <span data-ttu-id="30c7a-113">Methode</span><span class="sxs-lookup"><span data-stu-id="30c7a-113">Method</span></span>                                                                                    | <span data-ttu-id="30c7a-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="30c7a-114">Description</span></span>                                                                             |
|:------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="30c7a-115">**Checktypographicfeature**</span><span class="sxs-lookup"><span data-stu-id="30c7a-115">**CheckTypographicFeature**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-checktypographicfeature)           | <span data-ttu-id="30c7a-116">Überprüft, ob ein typografisches Feature für ein Symbol oder einen Satz von Symbolen verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="30c7a-116">Checks if a typographic feature is available for a glyph or a set of glyphs.</span></span><br/> |
| [<span data-ttu-id="30c7a-117">**Getglyphorientationtransform**</span><span class="sxs-lookup"><span data-stu-id="30c7a-117">**GetGlyphOrientationTransform**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-getglyphorientationtransform) | <span data-ttu-id="30c7a-118">Gibt eine 2x3-Transformationsmatrix für den jeweiligen Winkel zum Zeichnen der Symbol Führung zurück.</span><span class="sxs-lookup"><span data-stu-id="30c7a-118">Returns 2x3 transform matrix for the respective angle to draw the glyph run.</span></span><br/> |
| [<span data-ttu-id="30c7a-119">**Gettypographicfeatures**</span><span class="sxs-lookup"><span data-stu-id="30c7a-119">**GetTypographicFeatures**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-gettypographicfeatures)             | <span data-ttu-id="30c7a-120">Gibt eine vollständige Liste der OpenType-Funktionen zurück, die für ein Skript oder eine Schriftart verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="30c7a-120">Returns a complete list of OpenType features available for a script or font.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="30c7a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30c7a-121">Requirements</span></span>



| <span data-ttu-id="30c7a-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30c7a-122">Requirement</span></span> | <span data-ttu-id="30c7a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="30c7a-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30c7a-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="30c7a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="30c7a-125">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="30c7a-125">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="30c7a-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="30c7a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="30c7a-127">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="30c7a-127">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="30c7a-128">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="30c7a-128">Minimum supported phone</span></span><br/>  | <span data-ttu-id="30c7a-129">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="30c7a-129">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="30c7a-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="30c7a-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="30c7a-131"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30c7a-131"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="30c7a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="30c7a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30c7a-133"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30c7a-133"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="30c7a-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30c7a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30c7a-135">**IDWriteTextAnalyzer1**</span><span class="sxs-lookup"><span data-stu-id="30c7a-135">**IDWriteTextAnalyzer1**</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)
</dt> </dl>

 

