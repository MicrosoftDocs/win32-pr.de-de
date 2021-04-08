---
title: SB_SETMINHEIGHT Meldung (kommstrg. h)
description: Legt die Mindesthöhe für den Zeichnungs Bereich eines Status Fensters fest.
ms.assetid: 346fe654-f808-4191-9c3d-f9a4def08df1
keywords:
- Windows-Steuerelemente für SB_SETMINHEIGHT Meldung
topic_type:
- apiref
api_name:
- SB_SETMINHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bcad3bf0cb4d11567e82aae4ef46a95fefe3890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956885"
---
# <a name="sb_setminheight-message"></a><span data-ttu-id="d15b0-104">SB- \_ setMinHeight-Nachricht</span><span class="sxs-lookup"><span data-stu-id="d15b0-104">SB\_SETMINHEIGHT message</span></span>

<span data-ttu-id="d15b0-105">Legt die Mindesthöhe für den Zeichnungs Bereich eines Status Fensters fest.</span><span class="sxs-lookup"><span data-stu-id="d15b0-105">Sets the minimum height of a status window's drawing area.</span></span>

## <a name="parameters"></a><span data-ttu-id="d15b0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d15b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d15b0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d15b0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d15b0-108">Mindesthöhe des Fensters in Pixel.</span><span class="sxs-lookup"><span data-stu-id="d15b0-108">Minimum height, in pixels, of the window.</span></span>

</dd> <dt>

<span data-ttu-id="d15b0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d15b0-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d15b0-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="d15b0-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d15b0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d15b0-111">Return value</span></span>

<span data-ttu-id="d15b0-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="d15b0-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d15b0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d15b0-113">Remarks</span></span>

<span data-ttu-id="d15b0-114">Die Mindesthöhe ist die Summe von *wParam* und die doppelte Breite des vertikalen Rahmens des Status Fensters in Pixel.</span><span class="sxs-lookup"><span data-stu-id="d15b0-114">The minimum height is the sum of *wParam* and twice the width, in pixels, of the vertical border of the status window.</span></span> <span data-ttu-id="d15b0-115">Eine Anwendung muss die [**WM- \_ Größen**](/windows/desktop/winmsg/wm-size) Nachricht an das Statusfenster senden, um das Fenster neu zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="d15b0-115">An application must send the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message to the status window to redraw the window.</span></span> <span data-ttu-id="d15b0-116">Der *wParam* -Parameter und der *LPARAM* -Parameter der **WM- \_ Größen** Nachricht sollten auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d15b0-116">The *wParam* and *lParam* parameters of the **WM\_SIZE** message should be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="d15b0-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d15b0-117">Requirements</span></span>



| <span data-ttu-id="d15b0-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d15b0-118">Requirement</span></span> | <span data-ttu-id="d15b0-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d15b0-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d15b0-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d15b0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d15b0-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d15b0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d15b0-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d15b0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d15b0-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d15b0-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d15b0-124">Header</span><span class="sxs-lookup"><span data-stu-id="d15b0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d15b0-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d15b0-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

