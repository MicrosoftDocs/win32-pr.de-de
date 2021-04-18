---
title: IDWriteTextFormat2-Schnittstelle
description: Beschreibt die Schriftart-und Absatz Eigenschaften, die zum Formatieren von Text verwendet werden, und beschreibt Gebiets Schema Informationen. | IDWriteTextFormat2-Schnittstelle
ms.assetid: 4396d2b0-240f-ee8b-1d21-c4294fb29b51
keywords:
- IDWriteTextFormat2 Interface Direct Write
- IDWriteTextFormat2 Interface Direct Write, beschrieben
topic_type:
- apiref
api_name:
- IDWriteTextFormat2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06abf78095953f684ed6ec3fd241c699b2b37db4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106351888"
---
# <a name="idwritetextformat2-interface"></a><span data-ttu-id="2d898-106">IDWriteTextFormat2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="2d898-106">IDWriteTextFormat2 interface</span></span>

<span data-ttu-id="2d898-107">Beschreibt die Schriftart-und Absatz Eigenschaften, die zum Formatieren von Text verwendet werden, und beschreibt Gebiets Schema Informationen.</span><span class="sxs-lookup"><span data-stu-id="2d898-107">Describes the font and paragraph properties used to format text, and it describes locale information.</span></span>

## <a name="members"></a><span data-ttu-id="2d898-108">Member</span><span class="sxs-lookup"><span data-stu-id="2d898-108">Members</span></span>

<span data-ttu-id="2d898-109">Die **IDWriteTextFormat2** -Schnittstelle erbt von [**IDWriteTextFormat1**](idwritetextformat1.md).</span><span class="sxs-lookup"><span data-stu-id="2d898-109">The **IDWriteTextFormat2** interface inherits from [**IDWriteTextFormat1**](idwritetextformat1.md).</span></span> <span data-ttu-id="2d898-110">**IDWriteTextFormat2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2d898-110">**IDWriteTextFormat2** also has these types of members:</span></span>

-   [<span data-ttu-id="2d898-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="2d898-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2d898-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="2d898-112">Methods</span></span>

<span data-ttu-id="2d898-113">Die **IDWriteTextFormat2** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="2d898-113">The **IDWriteTextFormat2** interface has these methods.</span></span>



| <span data-ttu-id="2d898-114">Methode</span><span class="sxs-lookup"><span data-stu-id="2d898-114">Method</span></span>                                                      | <span data-ttu-id="2d898-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d898-115">Description</span></span>                                                                      |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="2d898-116">**GetLineSpacing**</span><span class="sxs-lookup"><span data-stu-id="2d898-116">**GetLineSpacing**</span></span>](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritetextformat2-getlinespacing) | <span data-ttu-id="2d898-117">Ruft den Anpassungs Satz für den Zeilenabstand für einen mehrzeiligen Textabschnitt ab.</span><span class="sxs-lookup"><span data-stu-id="2d898-117">Gets the line spacing adjustment set for a multiline text paragraph.</span></span> <br/> |
| [<span data-ttu-id="2d898-118">**SetLineSpacing**</span><span class="sxs-lookup"><span data-stu-id="2d898-118">**SetLineSpacing**</span></span>](idwritetextformat2-setlinespacing.md) | <span data-ttu-id="2d898-119">Zeilenabstand festlegen.</span><span class="sxs-lookup"><span data-stu-id="2d898-119">Set line spacing.</span></span><br/>                                                     |



 

## <a name="requirements"></a><span data-ttu-id="2d898-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d898-120">Requirements</span></span>



| <span data-ttu-id="2d898-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d898-121">Requirement</span></span> | <span data-ttu-id="2d898-122">Wert</span><span class="sxs-lookup"><span data-stu-id="2d898-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d898-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2d898-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2d898-124">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="2d898-124">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="2d898-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2d898-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2d898-126">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="2d898-126">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="2d898-127">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="2d898-127">Minimum supported phone</span></span><br/>  | <span data-ttu-id="2d898-128">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="2d898-128">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="2d898-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2d898-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="2d898-130"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d898-130"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2d898-131">DLL</span><span class="sxs-lookup"><span data-stu-id="2d898-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d898-132"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d898-132"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2d898-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d898-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d898-134">**IDWriteTextFormat1**</span><span class="sxs-lookup"><span data-stu-id="2d898-134">**IDWriteTextFormat1**</span></span>](idwritetextformat1.md)
</dt> </dl>

 

