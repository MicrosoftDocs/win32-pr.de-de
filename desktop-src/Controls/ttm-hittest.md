---
title: TTM_HITTEST Meldung (kommstrg. h)
description: Testet einen Punkt, um zu bestimmen, ob er sich innerhalb des umgebenden Rechtecks des angegebenen Tools befindet, und ruft, wenn dies der Fall ist, Informationen über das Tool ab.
ms.assetid: d4dcc29b-c64c-41b8-a153-300df68ecdf5
keywords:
- Windows-Steuerelemente für TTM_HITTEST Meldung
topic_type:
- apiref
api_name:
- TTM_HITTEST
- TTM_HITTESTA
- TTM_HITTESTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b515ccb5c283b66760f24c02749368e424e6fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476782"
---
# <a name="ttm_hittest-message"></a><span data-ttu-id="1d1e8-104">TTM- \_ HitTest-Meldung</span><span class="sxs-lookup"><span data-stu-id="1d1e8-104">TTM\_HITTEST message</span></span>

<span data-ttu-id="1d1e8-105">Testet einen Punkt, um zu bestimmen, ob er sich innerhalb des umgebenden Rechtecks des angegebenen Tools befindet, und ruft, wenn dies der Fall ist, Informationen über das Tool ab.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-105">Tests a point to determine whether it is within the bounding rectangle of the specified tool and, if it is, retrieves information about the tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="1d1e8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d1e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d1e8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1d1e8-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1d1e8-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1d1e8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1d1e8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d1e8-110">Zeiger auf eine [**tthittestinfo**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-110">Pointer to a [**TTHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa) structure.</span></span> <span data-ttu-id="1d1e8-111">Beim Senden der Nachricht muss der **HWND** -Member das Handle für ein Tool angeben, und der **PT** -Member muss die Koordinaten eines Punkts angeben.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-111">When sending the message, the **hwnd** member must specify the handle to a tool and the **pt** member must specify the coordinates of a point.</span></span> <span data-ttu-id="1d1e8-112">Wenn der Rückgabewert **true** ist, erhält der **TI** -Member (eine [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur) Informationen über das Tool, das den Punkt einnimmt.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-112">If the return value is **TRUE**, the **ti** member (a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure) receives information about the tool that occupies the point.</span></span> <span data-ttu-id="1d1e8-113">Der **CBSIZE** -Member der **TI** -Struktur muss ausgefüllt werden, bevor diese Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-113">The **cbSize** member of the **ti** structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d1e8-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1d1e8-114">Return value</span></span>

<span data-ttu-id="1d1e8-115">Gibt **true** zurück, wenn das Tool den angegebenen Punkt einnimmt, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="1d1e8-115">Returns **TRUE** if the tool occupies the specified point, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d1e8-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d1e8-116">Remarks</span></span>

<span data-ttu-id="1d1e8-117">Diese Nachricht muss gesendet werden, wenn für das Tool das "ttf Track"- \_ Flag festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-117">This message must be sent when the tool has the TTF\_TRACK flag set.</span></span> <span data-ttu-id="1d1e8-118">Weitere Informationen zu diesem Flag finden Sie unter [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa).</span><span class="sxs-lookup"><span data-stu-id="1d1e8-118">For more information on this flag, see [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa).</span></span> <span data-ttu-id="1d1e8-119">Bei TTM \_ HitTest tritt ein Fehler \_ auf, wenn "ttf Track" nicht festgelegt ist, unabhängig davon, ob sich der Treffer Punkt im Tool Rechteck befindet oder nicht.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-119">TTM\_HITTEST will fail if TTF\_TRACK is not set, regardless if the hit point is in the tools rectangle or not.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d1e8-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d1e8-120">Requirements</span></span>



| <span data-ttu-id="1d1e8-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d1e8-121">Requirement</span></span> | <span data-ttu-id="1d1e8-122">Wert</span><span class="sxs-lookup"><span data-stu-id="1d1e8-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1d1e8-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1d1e8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1d1e8-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d1e8-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1d1e8-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1d1e8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1d1e8-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d1e8-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1d1e8-127">Header</span><span class="sxs-lookup"><span data-stu-id="1d1e8-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d1e8-128"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d1e8-128"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="1d1e8-129">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="1d1e8-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1d1e8-130">**TTM \_ Hittestw** (Unicode) und **TTM \_ hittesta** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1d1e8-130">**TTM\_HITTESTW** (Unicode) and **TTM\_HITTESTA** (ANSI)</span></span><br/>                   |



 

 





