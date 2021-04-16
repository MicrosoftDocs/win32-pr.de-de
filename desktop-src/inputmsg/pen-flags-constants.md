---
title: Pen-Flags
description: Werte, die im Feld "kflags" der POINTER_PEN_INFO Struktur angezeigt werden können.
ms.assetid: BC3CE568-4090-4451-B780-18530C988305
topic_type:
- apiref
api_name:
- PEN_FLAG_NONE
- PEN_FLAG_BARREL
- PEN_FLAG_INVERTED
- PEN_FLAG_ERASER
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: d7c28beaf58b6fa96bb8dd82b2dd650b2a7d6950
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477949"
---
# <a name="pen-flags"></a><span data-ttu-id="42abf-103">Pen-Flags</span><span class="sxs-lookup"><span data-stu-id="42abf-103">Pen Flags</span></span>

<span data-ttu-id="42abf-104">Werte, die im Feld " **kflags** " der [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) Struktur angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="42abf-104">Values that can appear in the **penFlags** field of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure.</span></span>

<dl> <dt>

<span data-ttu-id="42abf-105"><span id="PEN_FLAG_NONE"></span><span id="pen_flag_none"></span>**PEN_FLAG_NONE**</span><span class="sxs-lookup"><span data-stu-id="42abf-105"><span id="PEN_FLAG_NONE"></span><span id="pen_flag_none"></span>**PEN_FLAG_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42abf-106">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42abf-106">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="42abf-107">Es ist kein Pen-Flag vorhanden.</span><span class="sxs-lookup"><span data-stu-id="42abf-107">There is no pen flag.</span></span> <span data-ttu-id="42abf-108">Dies ist die Standardoption.</span><span class="sxs-lookup"><span data-stu-id="42abf-108">This is the default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42abf-109"><span id="PEN_FLAG_BARREL"></span><span id="pen_flag_barrel"></span>**PEN_FLAG_BARREL**</span><span class="sxs-lookup"><span data-stu-id="42abf-109"><span id="PEN_FLAG_BARREL"></span><span id="pen_flag_barrel"></span>**PEN_FLAG_BARREL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42abf-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="42abf-110">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="42abf-111">Die Schaltfläche "Barrel" wird gedrückt.</span><span class="sxs-lookup"><span data-stu-id="42abf-111">The barrel button is pressed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42abf-112"><span id="PEN_FLAG_INVERTED"></span><span id="pen_flag_inverted"></span>**PEN_FLAG_INVERTED**</span><span class="sxs-lookup"><span data-stu-id="42abf-112"><span id="PEN_FLAG_INVERTED"></span><span id="pen_flag_inverted"></span>**PEN_FLAG_INVERTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42abf-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="42abf-113">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="42abf-114">Der Stift ist invertiert.</span><span class="sxs-lookup"><span data-stu-id="42abf-114">The pen is inverted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42abf-115"><span id="PEN_FLAG_ERASER"></span><span id="pen_flag_eraser"></span>**PEN_FLAG_ERASER**</span><span class="sxs-lookup"><span data-stu-id="42abf-115"><span id="PEN_FLAG_ERASER"></span><span id="pen_flag_eraser"></span>**PEN_FLAG_ERASER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42abf-116">0x00000004</span><span class="sxs-lookup"><span data-stu-id="42abf-116">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="42abf-117">Die radiererschaltfläche wird gedrückt.</span><span class="sxs-lookup"><span data-stu-id="42abf-117">The eraser button is pressed.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42abf-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42abf-118">Requirements</span></span>



| <span data-ttu-id="42abf-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42abf-119">Requirement</span></span> | <span data-ttu-id="42abf-120">Wert</span><span class="sxs-lookup"><span data-stu-id="42abf-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="42abf-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="42abf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="42abf-122">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42abf-122">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="42abf-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="42abf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="42abf-124">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42abf-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="42abf-125">Header</span><span class="sxs-lookup"><span data-stu-id="42abf-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="42abf-126"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="42abf-126"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42abf-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42abf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42abf-128">Konstanten</span><span class="sxs-lookup"><span data-stu-id="42abf-128">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="42abf-129">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="42abf-129">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





