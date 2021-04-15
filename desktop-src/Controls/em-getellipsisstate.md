---
title: EM_GETELLIPSISSTATE Meldung (RichEdit. h)
description: Ruft den aktuellen Ellipsen Zustand ab.
ms.assetid: D02AE225-F5BF-401A-9877-55C68946CDBE
keywords:
- Windows-Steuerelemente für EM_GETELLIPSISSTATE Meldung
topic_type:
- apiref
api_name:
- EM_GETELLIPSISSTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 905bc8ecc180189f46e896aa0d9aaa3ba88b3f0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476833"
---
# <a name="em_getellipsisstate-message"></a><span data-ttu-id="c76c4-104">EM \_ getellipsisstate-Meldung</span><span class="sxs-lookup"><span data-stu-id="c76c4-104">EM\_GETELLIPSISSTATE message</span></span>

<span data-ttu-id="c76c4-105">Ruft den aktuellen Ellipsen Zustand ab.</span><span class="sxs-lookup"><span data-stu-id="c76c4-105">Retrieves the current ellipsis state.</span></span>


```C++
#define EM_GETELLIPSISSTATE       (WM_USER + 322)
```



## <a name="parameters"></a><span data-ttu-id="c76c4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c76c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c76c4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c76c4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c76c4-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="c76c4-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c76c4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c76c4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c76c4-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="c76c4-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c76c4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c76c4-111">Return value</span></span>

<span data-ttu-id="c76c4-112">Der Rückgabewert ist true, wenn ein Auslassungs Zeichen angezeigt wird, andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="c76c4-112">The return value is TRUE if an ellipsis is being displayed and FALSE otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c76c4-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c76c4-113">Requirements</span></span>



| <span data-ttu-id="c76c4-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c76c4-114">Requirement</span></span> | <span data-ttu-id="c76c4-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c76c4-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c76c4-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c76c4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c76c4-117">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c76c4-117">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c76c4-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c76c4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c76c4-119">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c76c4-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c76c4-120">Header</span><span class="sxs-lookup"><span data-stu-id="c76c4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c76c4-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c76c4-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c76c4-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c76c4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c76c4-123">**EM \_ getellipsismode**</span><span class="sxs-lookup"><span data-stu-id="c76c4-123">**EM\_GETELLIPSISMODE**</span></span>](em-getellipsismode.md)
</dt> <dt>

[<span data-ttu-id="c76c4-124">**EM/ \_ tellipsismode**</span><span class="sxs-lookup"><span data-stu-id="c76c4-124">**EM\_SETELLIPSISMODE**</span></span>](em-setellipsismode.md)
</dt> </dl>

 

 





