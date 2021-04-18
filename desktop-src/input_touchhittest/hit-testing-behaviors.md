---
title: Verhalten der Berührungs Treffer Tests
description: Die folgenden Konstanten werden von Anwendungen oder Benutzeroberflächen-Frameworks verwendet, um zu identifizieren, wie Nachrichten für touchtreffer Tests von Fenstern verarbeitet werden, die über die registertouchhittestingwindow-Funktion registriert werden.
ms.assetid: D1ECCBFA-CD01-401E-A42E-4F954F5F0A32
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
ms.date: 02/07/2020
ms.openlocfilehash: 9b49f61870c6c7041d73d6fa8d5c078887360359
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345497"
---
# <a name="touch-hit-testing-behaviors"></a><span data-ttu-id="25043-103">Verhalten der Berührungs Treffer Tests</span><span class="sxs-lookup"><span data-stu-id="25043-103">Touch Hit Testing Behaviors</span></span>

<span data-ttu-id="25043-104">Die folgenden Konstanten werden von Anwendungen oder Benutzeroberflächen-Frameworks verwendet, um zu identifizieren, wie Nachrichten für touchtreffer Tests von Fenstern verarbeitet werden, die über die [**registertouchhittestingwindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) -Funktion registriert werden.</span><span class="sxs-lookup"><span data-stu-id="25043-104">The following constants are used by applications or UI frameworks to identify how messages for touch hit testing are processed by windows that are registered through the [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) function.</span></span>

| <span data-ttu-id="25043-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="25043-105">Constant/value</span></span> | <span data-ttu-id="25043-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="25043-106">Description</span></span> |
|---|---|
| <span data-ttu-id="25043-107">**TOUCH_HIT_TESTING_DEFAULT** </dt> <dt>0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="25043-107">**TOUCH_HIT_TESTING_DEFAULT**</dt> <dt>0 (0x0)</span></span> | <span data-ttu-id="25043-108">Gibt an, dass [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) -Nachrichten nicht an das Zielfenster gesendet, sondern an untergeordnete Fenster gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="25043-108">Indicates that [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) messages are not sent to the target window but are sent to child windows.</span></span><br/> |
| <span data-ttu-id="25043-109">**TOUCH_HIT_TESTING_CLIENT** </dt> <dt>1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="25043-109">**TOUCH_HIT_TESTING_CLIENT**</dt> <dt>1 (0x1)</span></span>    | <span data-ttu-id="25043-110">Gibt an, dass [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) -Nachrichten an das Zielfenster gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="25043-110">Indicates that [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) messages are sent to the target window.</span></span><br/>                                   |
| <span data-ttu-id="25043-111">**TOUCH_HIT_TESTING_NONE** </dt> <dt>2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="25043-111">**TOUCH_HIT_TESTING_NONE**</dt> <dt>2 (0x2)</span></span>          | <span data-ttu-id="25043-112">Gibt an, dass [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) -Nachrichten nicht an das Zielfenster oder die untergeordneten Fenster gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="25043-112">Indicates that [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) messages are not sent to the target window or child windows.</span></span><br/>              |

## <a name="requirements"></a><span data-ttu-id="25043-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25043-113">Requirements</span></span>

| <span data-ttu-id="25043-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25043-114">Requirement</span></span> | <span data-ttu-id="25043-115">Wert</span><span class="sxs-lookup"><span data-stu-id="25043-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="25043-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="25043-116">Minimum supported client</span></span><br/> | <span data-ttu-id="25043-117">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25043-117">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="25043-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="25043-118">Minimum supported server</span></span><br/> | <span data-ttu-id="25043-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="25043-119">None supported</span></span><br/>                                                            |
| <span data-ttu-id="25043-120">Header</span><span class="sxs-lookup"><span data-stu-id="25043-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="25043-121"><dt>Winuser. h</span><span class="sxs-lookup"><span data-stu-id="25043-121"><dt>Winuser.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="25043-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25043-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25043-123">Konstanten</span><span class="sxs-lookup"><span data-stu-id="25043-123">Constants</span></span>](constants.md)
