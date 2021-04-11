---
title: TB_SETPADDING Meldung (kommstrg. h)
description: Legt die Auffüll Zeichen für ein Symbolleisten-Steuerelement fest.
ms.assetid: a18c4efb-1140-4149-8dce-dfc1f03bb61a
keywords:
- Windows-Steuerelemente für TB_SETPADDING Meldung
topic_type:
- apiref
api_name:
- TB_SETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65fae53f7e7702528915af7631bd675f11188b71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105752"
---
# <a name="tb_setpadding-message"></a><span data-ttu-id="c1278-104">TB- \_ setPadding-Meldung</span><span class="sxs-lookup"><span data-stu-id="c1278-104">TB\_SETPADDING message</span></span>

<span data-ttu-id="c1278-105">Legt die Auffüll Zeichen für ein Symbolleisten-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="c1278-105">Sets the padding for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c1278-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1278-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1278-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c1278-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1278-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="c1278-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c1278-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c1278-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1278-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt den horizontalen Abstand in Pixel an.</span><span class="sxs-lookup"><span data-stu-id="c1278-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the horizontal padding, in pixels.</span></span> <span data-ttu-id="c1278-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den vertikalen Abstand in Pixel an.</span><span class="sxs-lookup"><span data-stu-id="c1278-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the vertical padding, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1278-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c1278-112">Return value</span></span>

<span data-ttu-id="c1278-113">Gibt einen **DWORD** -Wert zurück, der den vorherigen horizontalen Auffüllung im [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) und den vorherigen vertikalen Abstand im [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))in Pixel enthält.</span><span class="sxs-lookup"><span data-stu-id="c1278-113">Returns a **DWORD** value that contains the previous horizontal padding in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the previous vertical padding in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)), in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1278-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1278-114">Remarks</span></span>

<span data-ttu-id="c1278-115">Die Auffüll Werte werden verwendet, um einen leeren Bereich zwischen dem Rand der Schaltfläche und dem Bild und/oder Text der Schaltfläche zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c1278-115">The padding values are used to create a blank area between the edge of the button and the button's image and/or text.</span></span> <span data-ttu-id="c1278-116">Wo und wie groß die Auffüll Zeichen tatsächlich angewendet werden, hängt vom Typ der Schaltfläche und davon ab, ob Sie über ein Bild verfügt.</span><span class="sxs-lookup"><span data-stu-id="c1278-116">Where and how much padding is actually applied depends on the type of the button and whether it has an image.</span></span> <span data-ttu-id="c1278-117">Der horizontale Abstand wird auf die Rechte und linke Seite der Schaltfläche angewendet, und die vertikale Auffüll Fläche wird auf den oberen und unteren Rand der Schaltfläche angewendet.</span><span class="sxs-lookup"><span data-stu-id="c1278-117">The horizontal padding is applied to both the right and left of the button, and the vertical padding is applied to both the top and bottom of the button.</span></span> <span data-ttu-id="c1278-118">Auffüll Zeichen werden nur auf Schaltflächen angewendet, die den tbstyle-Stil für die [**\_ Automatische Größe**](toolbar-control-and-button-styles.md) aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c1278-118">Padding is only applied to buttons that have the [**TBSTYLE\_AUTOSIZE**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1278-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1278-119">Requirements</span></span>



| <span data-ttu-id="c1278-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1278-120">Requirement</span></span> | <span data-ttu-id="c1278-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c1278-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c1278-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c1278-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c1278-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1278-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c1278-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c1278-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c1278-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1278-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c1278-126">Header</span><span class="sxs-lookup"><span data-stu-id="c1278-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1278-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1278-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1278-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1278-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1278-129">**TB \_ getpadding**</span><span class="sxs-lookup"><span data-stu-id="c1278-129">**TB\_GETPADDING**</span></span>](tb-getpadding.md)
</dt> </dl>

 

