---
title: DM_REPOSITION Meldung (Winuser. h)
description: Positioniert ein Dialogfeld der obersten Ebene neu, sodass es in den Desktop Bereich passt. Eine Anwendung kann diese Nachricht nach der Größe der Größe an ein Dialogfeld senden, um sicherzustellen, dass das gesamte Dialogfeld sichtbar bleibt.
ms.assetid: 8386d23e-06ea-4ea7-adde-ac97fc97861d
keywords:
- Dialog Felder DM_REPOSITION Meldung
topic_type:
- apiref
api_name:
- DM_REPOSITION
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19425d4d77a62117f3fadfdd98f0629b81bf334c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040963"
---
# <a name="dm_reposition-message"></a><span data-ttu-id="e9b97-105">DM- \_ neupositions Meldung</span><span class="sxs-lookup"><span data-stu-id="e9b97-105">DM\_REPOSITION message</span></span>

<span data-ttu-id="e9b97-106">Positioniert ein Dialogfeld der obersten Ebene neu, sodass es in den Desktop Bereich passt.</span><span class="sxs-lookup"><span data-stu-id="e9b97-106">Repositions a top-level dialog box so that it fits within the desktop area.</span></span> <span data-ttu-id="e9b97-107">Eine Anwendung kann diese Nachricht nach der Größe der Größe an ein Dialogfeld senden, um sicherzustellen, dass das gesamte Dialogfeld sichtbar bleibt.</span><span class="sxs-lookup"><span data-stu-id="e9b97-107">An application can send this message to a dialog box after resizing it to ensure that the entire dialog box remains visible.</span></span>


```C++
#define WM_USER              0x0400
#define DM_REPOSITION       (WM_USER+2)
```



## <a name="parameters"></a><span data-ttu-id="e9b97-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9b97-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9b97-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e9b97-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9b97-110">Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="e9b97-110">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e9b97-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e9b97-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9b97-112">Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="e9b97-112">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9b97-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e9b97-113">Return value</span></span>

<span data-ttu-id="e9b97-114">Diese Nachricht weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="e9b97-114">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9b97-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9b97-115">Remarks</span></span>

<span data-ttu-id="e9b97-116">Diese Meldung hat keine Auswirkung, wenn das Dialogfeld ein untergeordnetes Fenster ist.</span><span class="sxs-lookup"><span data-stu-id="e9b97-116">This message has no effect if the dialog box is a child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9b97-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9b97-117">Requirements</span></span>



| <span data-ttu-id="e9b97-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9b97-118">Requirement</span></span> | <span data-ttu-id="e9b97-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e9b97-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9b97-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e9b97-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e9b97-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9b97-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e9b97-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e9b97-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e9b97-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9b97-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e9b97-124">Header</span><span class="sxs-lookup"><span data-stu-id="e9b97-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9b97-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="e9b97-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9b97-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9b97-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9b97-127">Übersicht über Dialogfelder</span><span class="sxs-lookup"><span data-stu-id="e9b97-127">Dialog Boxes Overview</span></span>](dialog-boxes.md)
</dt> </dl>

 

 





