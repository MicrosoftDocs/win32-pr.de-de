---
description: Ruft die Schriftart ab, mit der das Steuerelement gerade seinen Text zeichnet.
ms.assetid: a6d05ef5-9933-4d03-a677-a8328bf1cb7d
title: WM_GETFONT Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5254b701630f09cc7980470a9f5be68ad377bc03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357905"
---
# <a name="wm_getfont-message"></a><span data-ttu-id="a11b9-103">WM- \_ getFont-Nachricht</span><span class="sxs-lookup"><span data-stu-id="a11b9-103">WM\_GETFONT message</span></span>

<span data-ttu-id="a11b9-104">Ruft die Schriftart ab, mit der das Steuerelement gerade seinen Text zeichnet.</span><span class="sxs-lookup"><span data-stu-id="a11b9-104">Retrieves the font with which the control is currently drawing its text.</span></span>


```C++
#define WM_GETFONT                      0x0031
```



## <a name="parameters"></a><span data-ttu-id="a11b9-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="a11b9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a11b9-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a11b9-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a11b9-107">Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="a11b9-107">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a11b9-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a11b9-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a11b9-109">Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="a11b9-109">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a11b9-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a11b9-110">Return value</span></span>

<span data-ttu-id="a11b9-111">Typ: **hFont**</span><span class="sxs-lookup"><span data-stu-id="a11b9-111">Type: **HFONT**</span></span>

<span data-ttu-id="a11b9-112">Der Rückgabewert ist ein Handle für die Schriftart, die vom Steuerelement verwendet wird, oder **null** , wenn das Steuerelement die System Schriftart verwendet.</span><span class="sxs-lookup"><span data-stu-id="a11b9-112">The return value is a handle to the font used by the control, or **NULL** if the control is using the system font.</span></span>

## <a name="requirements"></a><span data-ttu-id="a11b9-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a11b9-113">Requirements</span></span>



| <span data-ttu-id="a11b9-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a11b9-114">Requirement</span></span> | <span data-ttu-id="a11b9-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a11b9-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a11b9-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a11b9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a11b9-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a11b9-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a11b9-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a11b9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a11b9-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a11b9-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a11b9-120">Header</span><span class="sxs-lookup"><span data-stu-id="a11b9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a11b9-121"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="a11b9-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a11b9-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a11b9-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="a11b9-123">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="a11b9-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a11b9-124">**WM- \_ setFont**</span><span class="sxs-lookup"><span data-stu-id="a11b9-124">**WM\_SETFONT**</span></span>](wm-setfont.md)
</dt> <dt>

<span data-ttu-id="a11b9-125">**Licher**</span><span class="sxs-lookup"><span data-stu-id="a11b9-125">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a11b9-126">Windows</span><span class="sxs-lookup"><span data-stu-id="a11b9-126">Windows</span></span>](windows.md)
</dt> </dl>

 

 




