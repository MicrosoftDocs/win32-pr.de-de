---
title: MCIWNDM_GETPALETTE Meldung (VFW. h)
description: Die mciwndm \_ getpalette-Nachricht Ruft ein Handle der Palette ab, die von einem MCI-Gerät verwendet wird. Sie können diese Nachricht explizit oder mithilfe des mciwndgetpalette-Makros senden.
ms.assetid: f8426344-0fee-4419-9d8a-dcee26cb4c28
keywords:
- MCIWNDM_GETPALETTE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faec3dd5d9c401d943fbc55ca58e452d3fb25497
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040216"
---
# <a name="mciwndm_getpalette-message"></a><span data-ttu-id="f8e37-105">Mciwndm \_ getpalette-Nachricht</span><span class="sxs-lookup"><span data-stu-id="f8e37-105">MCIWNDM\_GETPALETTE message</span></span>

<span data-ttu-id="f8e37-106">Die **mciwndm \_ getpalette** -Nachricht Ruft ein Handle der Palette ab, die von einem MCI-Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f8e37-106">The **MCIWNDM\_GETPALETTE** message retrieves a handle of the palette used by an MCI device.</span></span> <span data-ttu-id="f8e37-107">Sie können diese Nachricht explizit oder mithilfe des [**mciwndgetpalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="f8e37-107">You can send this message explicitly or by using the [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) macro.</span></span>


```C++
MCIWNDM_GETPALETTE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="f8e37-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f8e37-108">Return Value</span></span>

<span data-ttu-id="f8e37-109">Gibt das Handle der Palette zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f8e37-109">Returns the handle of the palette if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8e37-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8e37-110">Requirements</span></span>



| <span data-ttu-id="f8e37-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f8e37-111">Requirement</span></span> | <span data-ttu-id="f8e37-112">Wert</span><span class="sxs-lookup"><span data-stu-id="f8e37-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f8e37-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f8e37-113">Minimum supported client</span></span><br/> | <span data-ttu-id="f8e37-114">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8e37-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f8e37-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f8e37-115">Minimum supported server</span></span><br/> | <span data-ttu-id="f8e37-116">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8e37-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f8e37-117">Header</span><span class="sxs-lookup"><span data-stu-id="f8e37-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8e37-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8e37-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8e37-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8e37-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8e37-120">**Mciwndgetpalette**</span><span class="sxs-lookup"><span data-stu-id="f8e37-120">**MCIWndGetPalette**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette)
</dt> </dl>

 

 





