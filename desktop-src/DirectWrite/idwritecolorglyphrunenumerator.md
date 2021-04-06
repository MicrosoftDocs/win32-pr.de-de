---
title: Idschreitecolorglyphrunenumerator-Schnittstelle
description: Diese Schnittstelle ermöglicht es der Anwendung, die farbglyphe aufzählen.
ms.assetid: 649AD648-32BB-4BF4-A82F-075E93505E33
keywords:
- Idwrite-colorglyphrunenumerator-Schnittstelle direkt schreiben
- Direkter Schreibvorgang für idschreitecolorglyphrunenumerator-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IDWriteColorGlyphRunEnumerator
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e41831610f3ef564db55241267b75820cb9d87af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742240"
---
# <a name="idwritecolorglyphrunenumerator-interface"></a><span data-ttu-id="7eeb9-105">Idschreitecolorglyphrunenumerator-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="7eeb9-105">IDWriteColorGlyphRunEnumerator interface</span></span>

<span data-ttu-id="7eeb9-106">Diese Schnittstelle ermöglicht es der Anwendung, die farbglyphe aufzählen.</span><span class="sxs-lookup"><span data-stu-id="7eeb9-106">This interface allows the application to enumerate through the color glyph runs.</span></span> <span data-ttu-id="7eeb9-107">Der Enumerator listet die Ebenen in einer zurück zur Vorderseite auf, um eine geeignete Schicht zu haben.</span><span class="sxs-lookup"><span data-stu-id="7eeb9-107">The enumerator enumerates the layers in a back to front order for appropriate layering.</span></span>

## <a name="members"></a><span data-ttu-id="7eeb9-108">Member</span><span class="sxs-lookup"><span data-stu-id="7eeb9-108">Members</span></span>

<span data-ttu-id="7eeb9-109">Die **idschreitecolorglyphrunenumerator** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7eeb9-109">The **IDWriteColorGlyphRunEnumerator** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7eeb9-110">**Idwrite tecolorglyphrunenumerator** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7eeb9-110">**IDWriteColorGlyphRunEnumerator** also has these types of members:</span></span>

-   [<span data-ttu-id="7eeb9-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="7eeb9-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7eeb9-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="7eeb9-112">Methods</span></span>

<span data-ttu-id="7eeb9-113">Die **idschreitecolorglyphrunenumerator** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="7eeb9-113">The **IDWriteColorGlyphRunEnumerator** interface has these methods.</span></span>



| <span data-ttu-id="7eeb9-114">Methode</span><span class="sxs-lookup"><span data-stu-id="7eeb9-114">Method</span></span>                                                                | <span data-ttu-id="7eeb9-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7eeb9-115">Description</span></span>                                                 |
|:----------------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="7eeb9-116">**Getcurrentrun**</span><span class="sxs-lookup"><span data-stu-id="7eeb9-116">**GetCurrentRun**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritecolorglyphrunenumerator-getcurrentrun) | <span data-ttu-id="7eeb9-117">Gibt die aktuelle Glyphe des Enumerators zurück.</span><span class="sxs-lookup"><span data-stu-id="7eeb9-117">Returns the current glyph run of the enumerator.</span></span><br/> |
| [<span data-ttu-id="7eeb9-118">**MoveNext**</span><span class="sxs-lookup"><span data-stu-id="7eeb9-118">**MoveNext**</span></span>](idwritecolorglyphrunenumerator-movenext.md)           | <span data-ttu-id="7eeb9-119">Wechselt zum nächsten Symbol, das im Enumerator ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7eeb9-119">Move to the next glyph run in the enumerator.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="7eeb9-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7eeb9-120">Requirements</span></span>



| <span data-ttu-id="7eeb9-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7eeb9-121">Requirement</span></span> | <span data-ttu-id="7eeb9-122">Wert</span><span class="sxs-lookup"><span data-stu-id="7eeb9-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7eeb9-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7eeb9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7eeb9-124">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="7eeb9-124">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="7eeb9-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7eeb9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7eeb9-126">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="7eeb9-126">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="7eeb9-127">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="7eeb9-127">Minimum supported phone</span></span><br/>  | <span data-ttu-id="7eeb9-128">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="7eeb9-128">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="7eeb9-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7eeb9-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="7eeb9-130"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7eeb9-130"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="7eeb9-131">DLL</span><span class="sxs-lookup"><span data-stu-id="7eeb9-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7eeb9-132"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7eeb9-132"><dt>Dwrite.dll</dt></span></span> </dl>   |



 

