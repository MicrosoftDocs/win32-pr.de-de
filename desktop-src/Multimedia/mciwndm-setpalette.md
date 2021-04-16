---
title: MCIWNDM_SETPALETTE Meldung (VFW. h)
description: Die mciwndm- \_ SetPalette-Nachricht sendet ein Palettenhandle an das MCI-Gerät, das dem mciwnd-Fenster zugeordnet ist. Sie können diese Nachricht explizit oder mithilfe des mciwndsetpalette-Makros senden.
ms.assetid: d2399cb7-d83c-465c-b02f-e6a016c28ae3
keywords:
- MCIWNDM_SETPALETTE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_SETPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba7e354082de4fc15f4179555a8b635b9426af90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477829"
---
# <a name="mciwndm_setpalette-message"></a><span data-ttu-id="d7c66-105">Mciwndm- \_ SetPalette-Nachricht</span><span class="sxs-lookup"><span data-stu-id="d7c66-105">MCIWNDM\_SETPALETTE message</span></span>

<span data-ttu-id="d7c66-106">Die **mciwndm- \_ SetPalette** -Nachricht sendet ein Palettenhandle an das MCI-Gerät, das dem mciwnd-Fenster zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d7c66-106">The **MCIWNDM\_SETPALETTE** message sends a palette handle to the MCI device associated with the MCIWnd window.</span></span> <span data-ttu-id="d7c66-107">Sie können diese Nachricht explizit oder mithilfe des [**mciwndsetpalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="d7c66-107">You can send this message explicitly or by using the [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) macro.</span></span>


```C++
MCIWNDM_SETPALETTE 
wParam = (WPARAM) (HPALETTE) hpal; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="d7c66-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7c66-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7c66-109"><span id="hpal"></span><span id="HPAL"></span>*hpal*</span><span class="sxs-lookup"><span data-stu-id="d7c66-109"><span id="hpal"></span><span id="HPAL"></span>*hpal*</span></span>
</dt> <dd>

<span data-ttu-id="d7c66-110">Palettenhandle.</span><span class="sxs-lookup"><span data-stu-id="d7c66-110">Palette handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7c66-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d7c66-111">Return Value</span></span>

<span data-ttu-id="d7c66-112">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="d7c66-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7c66-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7c66-113">Requirements</span></span>



| <span data-ttu-id="d7c66-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7c66-114">Requirement</span></span> | <span data-ttu-id="d7c66-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d7c66-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d7c66-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d7c66-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d7c66-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7c66-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d7c66-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d7c66-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d7c66-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7c66-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d7c66-120">Header</span><span class="sxs-lookup"><span data-stu-id="d7c66-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7c66-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7c66-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7c66-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7c66-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7c66-123">**Mciwndsetpalette**</span><span class="sxs-lookup"><span data-stu-id="d7c66-123">**MCIWndSetPalette**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette)
</dt> </dl>

 

 





