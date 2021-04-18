---
title: MCIWNDM_CHANGESTYLES Meldung (VFW. h)
description: Die mciwndm \_ changestyles-Meldung ändert die vom mciwnd-Fenster verwendeten Stile. Sie können diese Nachricht explizit oder mithilfe des mciwndchangestyles-Makros senden.
ms.assetid: 9074c21a-e49f-4089-a6d2-af8d513cb632
keywords:
- MCIWNDM_CHANGESTYLES-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_CHANGESTYLES
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b2cea636c3c879da642da753c4fd084b06c4334
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340313"
---
# <a name="mciwndm_changestyles-message"></a><span data-ttu-id="23720-105">Mciwndm \_ changestyles-Nachricht</span><span class="sxs-lookup"><span data-stu-id="23720-105">MCIWNDM\_CHANGESTYLES message</span></span>

<span data-ttu-id="23720-106">Die **mciwndm \_ changestyles** -Meldung ändert die vom mciwnd-Fenster verwendeten Stile.</span><span class="sxs-lookup"><span data-stu-id="23720-106">The **MCIWNDM\_CHANGESTYLES** message changes the styles used by the MCIWnd window.</span></span> <span data-ttu-id="23720-107">Sie können diese Nachricht explizit oder mithilfe des [**mciwndchangestyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="23720-107">You can send this message explicitly or by using the [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) macro.</span></span>


```C++
MCIWNDM_CHANGESTYLES 
wParam = (WPARAM) (UINT) mask; 
lParam = (LPARAM) (LONG) value; 
```



## <a name="parameters"></a><span data-ttu-id="23720-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="23720-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23720-109"><span id="mask"></span><span id="MASK"></span>*chel*</span><span class="sxs-lookup"><span data-stu-id="23720-109"><span id="mask"></span><span id="MASK"></span>*mask*</span></span>
</dt> <dd>

<span data-ttu-id="23720-110">Maske, die die Stile identifiziert, die geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="23720-110">Mask that identifies the styles that can change.</span></span> <span data-ttu-id="23720-111">Diese Maske ist der bitweise OR-Operator aller Stile, die geändert werden dürfen.</span><span class="sxs-lookup"><span data-stu-id="23720-111">This mask is the bitwise OR operator of all styles that will be permitted to change.</span></span>

</dd> <dt>

<span data-ttu-id="23720-112"><span id="value"></span><span id="VALUE"></span>*Wert*</span><span class="sxs-lookup"><span data-stu-id="23720-112"><span id="value"></span><span id="VALUE"></span>*value*</span></span>
</dt> <dd>

<span data-ttu-id="23720-113">Neue Stileinstellungen für das Fenster.</span><span class="sxs-lookup"><span data-stu-id="23720-113">New style settings for the window.</span></span> <span data-ttu-id="23720-114">Geben Sie 0 (null) für diesen Parameter an, um alle in der Maske identifizierten Stile zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="23720-114">Specify zero for this parameter to turn off all styles identified in the mask.</span></span> <span data-ttu-id="23720-115">Eine Liste der verfügbaren Stile finden Sie unter der Funktion " [**mciwndcreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) ".</span><span class="sxs-lookup"><span data-stu-id="23720-115">For a list of the available styles, see the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23720-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="23720-116">Return Value</span></span>

<span data-ttu-id="23720-117">Gibt 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="23720-117">Returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="23720-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23720-118">Requirements</span></span>



| <span data-ttu-id="23720-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="23720-119">Requirement</span></span> | <span data-ttu-id="23720-120">Wert</span><span class="sxs-lookup"><span data-stu-id="23720-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="23720-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="23720-121">Minimum supported client</span></span><br/> | <span data-ttu-id="23720-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="23720-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="23720-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="23720-123">Minimum supported server</span></span><br/> | <span data-ttu-id="23720-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="23720-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="23720-125">Header</span><span class="sxs-lookup"><span data-stu-id="23720-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="23720-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="23720-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23720-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23720-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23720-128">**Mciwndcreate**</span><span class="sxs-lookup"><span data-stu-id="23720-128">**MCIWndCreate**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)
</dt> <dt>

[<span data-ttu-id="23720-129">**Mciwndchangestyles**</span><span class="sxs-lookup"><span data-stu-id="23720-129">**MCIWndChangeStyles**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> </dl>

 

 





