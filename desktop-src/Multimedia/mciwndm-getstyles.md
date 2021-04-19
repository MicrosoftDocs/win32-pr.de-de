---
title: MCIWNDM_GETSTYLES Meldung (VFW. h)
description: Die mciwndm \_ getStyles-Nachricht Ruft die Flags ab, die die aktuellen, von einem Fenster verwendeten mciwnd-Fenster Stile angeben. Sie können diese Nachricht explizit oder mit dem mciwndgetstyles-Makro senden.
ms.assetid: cd34ba05-47cb-488e-a6c6-4ec1c0d25de8
keywords:
- MCIWNDM_GETSTYLES-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETSTYLES
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 983e37291977edf2473c2b603cd5b40792fb7989
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342661"
---
# <a name="mciwndm_getstyles-message"></a><span data-ttu-id="25831-105">Mciwndm \_ getStyles-Nachricht</span><span class="sxs-lookup"><span data-stu-id="25831-105">MCIWNDM\_GETSTYLES message</span></span>

<span data-ttu-id="25831-106">Die **mciwndm \_ getStyles** -Nachricht Ruft die Flags ab, die die aktuellen, von einem Fenster verwendeten mciwnd-Fenster Stile angeben.</span><span class="sxs-lookup"><span data-stu-id="25831-106">The **MCIWNDM\_GETSTYLES** message retrieves the flags specifying the current MCIWnd window styles used by a window.</span></span> <span data-ttu-id="25831-107">Sie können diese Nachricht explizit oder mit dem [**mciwndgetstyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="25831-107">You can send this message explicitly or by using the [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) macro.</span></span>


```C++
MCIWNDM_GETSTYLES 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="25831-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="25831-108">Return Value</span></span>

<span data-ttu-id="25831-109">Gibt einen Wert zurück, der die aktuellen Stile des mciwnd-Fensters darstellt.</span><span class="sxs-lookup"><span data-stu-id="25831-109">Returns a value representing the current styles of the MCIWnd window.</span></span> <span data-ttu-id="25831-110">Der Rückgabewert ist der bitweise OR-Operator der mciwnd-Fenster Stile (mciwndf-Flags).</span><span class="sxs-lookup"><span data-stu-id="25831-110">The return value is the bitwise OR operator of the MCIWnd window styles (MCIWNDF flags).</span></span>

## <a name="requirements"></a><span data-ttu-id="25831-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25831-111">Requirements</span></span>



| <span data-ttu-id="25831-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25831-112">Requirement</span></span> | <span data-ttu-id="25831-113">Wert</span><span class="sxs-lookup"><span data-stu-id="25831-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="25831-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="25831-114">Minimum supported client</span></span><br/> | <span data-ttu-id="25831-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25831-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="25831-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="25831-116">Minimum supported server</span></span><br/> | <span data-ttu-id="25831-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25831-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="25831-118">Header</span><span class="sxs-lookup"><span data-stu-id="25831-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="25831-119"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="25831-119"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25831-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25831-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25831-121">**Mciwndgetstyles**</span><span class="sxs-lookup"><span data-stu-id="25831-121">**MCIWndGetStyles**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles)
</dt> </dl>

 

 





