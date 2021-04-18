---
title: PGM_SETBUTTONSIZE Meldung (kommstrg. h)
description: Legt die aktuelle Schaltflächen Größe für das Pager-Steuerelement fest. Sie können diese Nachricht explizit senden oder das Pager- \_ setbuttonsize-Makro verwenden.
ms.assetid: b31960f8-87c2-4209-8213-df75ac883e11
keywords:
- Windows-Steuerelemente für PGM_SETBUTTONSIZE Meldung
topic_type:
- apiref
api_name:
- PGM_SETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecf8c164ed960675c1a68be36acfe0eff40f972f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517645"
---
# <a name="pgm_setbuttonsize-message"></a><span data-ttu-id="43659-105">PGM- \_ setbuttonsize-Meldung</span><span class="sxs-lookup"><span data-stu-id="43659-105">PGM\_SETBUTTONSIZE message</span></span>

<span data-ttu-id="43659-106">Legt die aktuelle Schaltflächen Größe für das Pager-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="43659-106">Sets the current button size for the pager control.</span></span> <span data-ttu-id="43659-107">Sie können diese Nachricht explizit senden oder das [**Pager- \_ setbuttonsize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="43659-107">You can send this message explicitly or use the [**Pager\_SetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="43659-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="43659-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43659-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="43659-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="43659-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="43659-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="43659-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="43659-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43659-112">Der Wert vom Typ **int** , der die neue Schaltflächen Größe in Pixel enthält.</span><span class="sxs-lookup"><span data-stu-id="43659-112">Value of type **int** that contains the new button size, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43659-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43659-113">Return value</span></span>

<span data-ttu-id="43659-114">Gibt einen **int** -Wert zurück, der die vorherige Schaltflächen Größe in Pixel enthält.</span><span class="sxs-lookup"><span data-stu-id="43659-114">Returns an **int** value that contains the previous button size, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="43659-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43659-115">Remarks</span></span>

<span data-ttu-id="43659-116">Wenn das Pager-Steuerelement den [**PGS- \_ Horz**](pager-control-styles.md) -Stil hat, bestimmt die Schaltflächen Größe die Breite der Pager-Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="43659-116">If the pager control has the [**PGS\_HORZ**](pager-control-styles.md) style, the button size determines the width of the pager buttons.</span></span> <span data-ttu-id="43659-117">Wenn das Pager-Steuerelement den [**PGS \_**](pager-control-styles.md) -Stil hat, bestimmt die Schaltflächen Größe die Höhe der Pager-Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="43659-117">If the pager control has the [**PGS\_VERT**](pager-control-styles.md) style, the button size determines the height of the pager buttons.</span></span> <span data-ttu-id="43659-118">Standardmäßig legt das Pager-Steuerelement seine Schaltflächen Größe auf drei Zehntel der Breite der Bild Lauf Leiste fest.</span><span class="sxs-lookup"><span data-stu-id="43659-118">By default, the pager control sets its button size to three-fourths of the width of the scroll bar.</span></span>

<span data-ttu-id="43659-119">Es gibt eine Mindestgröße für die Pager-Schaltfläche, derzeit 12 Pixel.</span><span class="sxs-lookup"><span data-stu-id="43659-119">There is a minimum size to the pager button, currently 12 pixels.</span></span> <span data-ttu-id="43659-120">Dies kann sich jedoch ändern, sodass Sie nicht von diesem Wert abhängig sein sollten.</span><span class="sxs-lookup"><span data-stu-id="43659-120">However, this can change so you should not depend on this value.</span></span>

## <a name="requirements"></a><span data-ttu-id="43659-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43659-121">Requirements</span></span>



| <span data-ttu-id="43659-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43659-122">Requirement</span></span> | <span data-ttu-id="43659-123">Wert</span><span class="sxs-lookup"><span data-stu-id="43659-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43659-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="43659-124">Minimum supported client</span></span><br/> | <span data-ttu-id="43659-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43659-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="43659-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="43659-126">Minimum supported server</span></span><br/> | <span data-ttu-id="43659-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43659-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="43659-128">Header</span><span class="sxs-lookup"><span data-stu-id="43659-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="43659-129"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="43659-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43659-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43659-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43659-131">**PGM \_ getbuttonsize**</span><span class="sxs-lookup"><span data-stu-id="43659-131">**PGM\_GETBUTTONSIZE**</span></span>](pgm-getbuttonsize.md)
</dt> </dl>

 

 





