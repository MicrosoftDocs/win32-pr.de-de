---
title: Fenster Konstanten für den Berührungs Treffer Test
description: Gibt an, wie Nachrichten für Touch-Treffer Tests von Fenstern verarbeitet werden, die über die registertouchhittestingwindow-Funktion registriert werden.
ms.assetid: CC6CCD0B-882F-4DA7-B886-D4BD18D6060C
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_DEFAULT
- TOUCH_HIT_TESTING_CLIENT
- TOUCH_HIT_TESTING_NONE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 46d577e03eaf918e4f2ea40aae30a2ab5112b630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392099"
---
# <a name="touch-hit-testing-window-constants"></a><span data-ttu-id="e304a-103">Fenster Konstanten für den Berührungs Treffer Test</span><span class="sxs-lookup"><span data-stu-id="e304a-103">Touch Hit Testing Window Constants</span></span>

<span data-ttu-id="e304a-104">Gibt an, wie Nachrichten für Touch-Treffer Tests von Fenstern verarbeitet werden, die über die [**registertouchhittestingwindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) -Funktion registriert werden.</span><span class="sxs-lookup"><span data-stu-id="e304a-104">Indicates how messages for touch hit testing are processed by windows that are registered through the [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) function.</span></span>



| <span data-ttu-id="e304a-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="e304a-105">Constant/value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="e304a-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e304a-106">Description</span></span>                                                                                                                            |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TOUCH_HIT_TESTING_DEFAULT"></span><span id="touch_hit_testing_default"></span><dl> <span data-ttu-id="e304a-107"><dt>**TOUCH_HIT_TESTING_DEFAULT**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="e304a-107"><dt>**TOUCH_HIT_TESTING_DEFAULT**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="e304a-108">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) -Nachrichten werden nicht an das Zielfenster gesendet, sondern an untergeordnete Fenster gesendet.</span><span class="sxs-lookup"><span data-stu-id="e304a-108">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messages are not sent to the target window but are sent to child windows.</span></span><br/> |
| <span id="TOUCH_HIT_TESTING_CLIENT"></span><span id="touch_hit_testing_client"></span><dl> <span data-ttu-id="e304a-109"><dt>**TOUCH_HIT_TESTING_CLIENT**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="e304a-109"><dt>**TOUCH_HIT_TESTING_CLIENT**</dt> <dt>1 (0x1)</dt></span></span> </dl>    | <span data-ttu-id="e304a-110">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) Meldungen werden an das Zielfenster gesendet.</span><span class="sxs-lookup"><span data-stu-id="e304a-110">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messages are sent to the target window.</span></span><br/>                                   |
| <span id="TOUCH_HIT_TESTING_NONE"></span><span id="touch_hit_testing_none"></span><dl> <span data-ttu-id="e304a-111"><dt>**TOUCH_HIT_TESTING_NONE**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="e304a-111"><dt>**TOUCH_HIT_TESTING_NONE**</dt> <dt>2 (0x2)</dt></span></span> </dl>          | <span data-ttu-id="e304a-112">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) -Nachrichten werden nicht an das Zielfenster oder die untergeordneten Fenster gesendet.</span><span class="sxs-lookup"><span data-stu-id="e304a-112">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messages are not sent to the target window or child windows.</span></span><br/>              |



## <a name="requirements"></a><span data-ttu-id="e304a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e304a-113">Requirements</span></span>



| <span data-ttu-id="e304a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e304a-114">Requirement</span></span> | <span data-ttu-id="e304a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e304a-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e304a-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e304a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e304a-117">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e304a-117">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e304a-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e304a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e304a-119">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e304a-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e304a-120">Header</span><span class="sxs-lookup"><span data-stu-id="e304a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e304a-121"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="e304a-121"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e304a-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e304a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e304a-123">Konstanten</span><span class="sxs-lookup"><span data-stu-id="e304a-123">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="e304a-124">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="e304a-124">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

