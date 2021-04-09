---
title: LVM_GETINSERTMARKRECT Meldung (kommstrg. h)
description: Ruft das Rechteck ab, das die Einfügemarke umschließt.
ms.assetid: 7b10229c-73ab-426c-8a8a-71258a33e248
keywords:
- Windows-Steuerelemente für LVM_GETINSERTMARKRECT Meldung
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARKRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd85bfb94f6425d2666372fd141b531fcb238643
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956993"
---
# <a name="lvm_getinsertmarkrect-message"></a><span data-ttu-id="03085-104">LVM \_ getinsertmarkrect-Nachricht</span><span class="sxs-lookup"><span data-stu-id="03085-104">LVM\_GETINSERTMARKRECT message</span></span>

<span data-ttu-id="03085-105">Ruft das Rechteck ab, das die Einfügemarke umschließt.</span><span class="sxs-lookup"><span data-stu-id="03085-105">Retrieves the rectangle that bounds the insertion point.</span></span>

## <a name="parameters"></a><span data-ttu-id="03085-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="03085-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03085-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="03085-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="03085-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="03085-108">Not used; must be zero.</span></span></dd> <dt>

<span data-ttu-id="03085-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="03085-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="03085-110">Ein Zeiger auf eine <a href="/previous-versions//dd162897(v=vs.85)">**Rect**</a> -Struktur, die die Koordinaten eines Rechtecks enthält, das die Einfügemarke umschließt.</span><span class="sxs-lookup"><span data-stu-id="03085-110">Pointer to a <a href="/previous-versions//dd162897(v=vs.85)">**RECT**</a> structure that contains the coordinates of a rectangle that bounds the insertion point.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03085-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="03085-111">Return value</span></span>

<span data-ttu-id="03085-112">Gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="03085-112">Returns one of the following values.</span></span>



| <span data-ttu-id="03085-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="03085-113">Return code</span></span>                                                                      | <span data-ttu-id="03085-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="03085-114">Description</span></span>                          |
|----------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="03085-115"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="03085-115"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="03085-116">Keine Einfügemarke gefunden.</span><span class="sxs-lookup"><span data-stu-id="03085-116">No insertion point found.</span></span><br/> |
| <dl> <span data-ttu-id="03085-117"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="03085-117"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="03085-118">Einfügemarke gefunden.</span><span class="sxs-lookup"><span data-stu-id="03085-118">Insertion point found.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="03085-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03085-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="03085-120">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="03085-120">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="03085-121">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="03085-121">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="03085-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03085-122">Requirements</span></span>



| <span data-ttu-id="03085-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03085-123">Requirement</span></span> | <span data-ttu-id="03085-124">Wert</span><span class="sxs-lookup"><span data-stu-id="03085-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="03085-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="03085-125">Minimum supported client</span></span><br/> | <span data-ttu-id="03085-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03085-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="03085-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="03085-127">Minimum supported server</span></span><br/> | <span data-ttu-id="03085-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03085-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="03085-129">Header</span><span class="sxs-lookup"><span data-stu-id="03085-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="03085-130"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="03085-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

