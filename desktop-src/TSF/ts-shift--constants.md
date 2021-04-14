---
title: TS_SHIFT_ Konstanten (textstor. h)
description: Die TS \_ Shift \_ \-Konstanten werden von der ianchor-Schnittstelle für die Bearbeitung von ausgeblendetem Text und der Zeichen Zählung verwendet.
ms.assetid: 93329238-f6e8-432e-9167-550a02b33b46
topic_type:
- apiref
api_name:
- TS_SHIFT_COUNT_HIDDEN
- TS_SHIFT_HALT_HIDDEN
- TS_SHIFT_HALT_VISIBLE
- TS_SHIFT_COUNT_ONLY
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98f3a11463aea1633079d771bf6a8b333475865e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391930"
---
# <a name="ts_shift_-constants"></a><span data-ttu-id="c269b-103">TS- \_ Verschiebungs \_ \* Konstanten</span><span class="sxs-lookup"><span data-stu-id="c269b-103">TS\_SHIFT\_\* Constants</span></span>

<span data-ttu-id="c269b-104">Die TS \_ -Verschiebungs \_ \* Konstanten werden von der **ianchor** -Schnittstelle zur Bearbeitung von ausgeblendetem Text und der Zeichen Zählung verwendet.</span><span class="sxs-lookup"><span data-stu-id="c269b-104">The TS\_Shift\_\* constants are used by the **IAnchor** interface for manipulation of hidden text and character counting.</span></span>



| <span data-ttu-id="c269b-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="c269b-105">Constant/value</span></span>                                                                                                                                                                                                                                       | <span data-ttu-id="c269b-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c269b-106">Description</span></span>                                                                                                                                                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_SHIFT_COUNT_HIDDEN"></span><span id="ts_shift_count_hidden"></span><dl> <span data-ttu-id="c269b-107"><dt>**TS \_ UMSCHALT \_ Anzahl \_ ausgeblendet**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="c269b-107"><dt>**TS\_SHIFT\_COUNT\_HIDDEN**</dt> <dt>( 0x1 )</dt></span></span> </dl> | <span data-ttu-id="c269b-108">Gibt an, dass der Anker an die nächste Bereichs Grenze verschoben wird, einschließlich der Grenze eines ausgeblendeten Text Bereichs.</span><span class="sxs-lookup"><span data-stu-id="c269b-108">Specifies that the anchor will be shifted to the next region boundary, including the boundary of a hidden text region.</span></span> <span data-ttu-id="c269b-109">Wenn nicht festgelegt, wird der Anker nach einem beliebigen angrenzenden ausgeblendeten Text verschoben, bis ein Bereich von sichtbarem Text gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="c269b-109">If not set, the anchor will be shifted past any adjacent hidden text until a region of visible text is found.</span></span><br/> |
| <span id="TS_SHIFT_HALT_HIDDEN"></span><span id="ts_shift_halt_hidden"></span><dl> <span data-ttu-id="c269b-110"><dt>**TS \_ UMSCHALT \_ Stopp \_ ausgeblendet**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="c269b-110"><dt>**TS\_SHIFT\_HALT\_HIDDEN**</dt> <dt>( 0x2 )</dt></span></span> </dl>    | <span data-ttu-id="c269b-111">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c269b-111">Not used.</span></span><br/>                                                                                                                                                                                                                            |
| <span id="TS_SHIFT_HALT_VISIBLE"></span><span id="ts_shift_halt_visible"></span><dl> <span data-ttu-id="c269b-112"><dt>**TS \_ UMSCHALT \_ Stopp \_ sichtbar**</dt> <dt>(0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="c269b-112"><dt>**TS\_SHIFT\_HALT\_VISIBLE**</dt> <dt>( 0x4 )</dt></span></span> </dl> | <span data-ttu-id="c269b-113">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c269b-113">Not used.</span></span><br/>                                                                                                                                                                                                                            |
| <span id="TS_SHIFT_COUNT_ONLY"></span><span id="ts_shift_count_only"></span><dl> <span data-ttu-id="c269b-114"><dt>**TS \_ \_ \_ Nur Verschiebungs Anzahl**</dt> <dt>(0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="c269b-114"><dt>**TS\_SHIFT\_COUNT\_ONLY**</dt> <dt>( 0x8 )</dt></span></span> </dl>       | <span data-ttu-id="c269b-115">Der Anker wird nicht verschoben.</span><span class="sxs-lookup"><span data-stu-id="c269b-115">The anchor is not shifted.</span></span><br/>                                                                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="c269b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c269b-116">Requirements</span></span>



| <span data-ttu-id="c269b-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c269b-117">Requirement</span></span> | <span data-ttu-id="c269b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c269b-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c269b-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c269b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c269b-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c269b-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c269b-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c269b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c269b-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c269b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c269b-123">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="c269b-123">Redistributable</span></span><br/>          | <span data-ttu-id="c269b-124">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c269b-124">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="c269b-125">Header</span><span class="sxs-lookup"><span data-stu-id="c269b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c269b-126"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="c269b-126"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="c269b-127">IDL</span><span class="sxs-lookup"><span data-stu-id="c269b-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c269b-128"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c269b-128"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c269b-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c269b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c269b-130">Ianchor:: Shif tregion</span><span class="sxs-lookup"><span data-stu-id="c269b-130">IAnchor::ShiftRegion</span></span>](/windows/desktop/api/Textstor/nf-textstor-ianchor-shiftregion)
</dt> </dl>

 

 





