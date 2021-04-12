---
title: HDM_SETITEM Meldung (kommstrg. h)
description: Legt die Attribute des angegebenen Elements in einem Header Steuerelement fest. Sie können diese Nachricht explizit senden oder das Header-"*"- \_ Makro verwenden.
ms.assetid: c8f0d526-3ebe-48c5-8aea-ea3703e2d983
keywords:
- Windows-Steuerelemente für HDM_SETITEM Meldung
topic_type:
- apiref
api_name:
- HDM_SETITEM
- HDM_SETITEMA
- HDM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71b03a05b909cf8c7887edd2031f5346c419f1cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478267"
---
# <a name="hdm_setitem-message"></a><span data-ttu-id="2d5e4-105">HDM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="2d5e4-105">HDM\_SETITEM message</span></span>

<span data-ttu-id="2d5e4-106">Legt die Attribute des angegebenen Elements in einem Header Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="2d5e4-106">Sets the attributes of the specified item in a header control.</span></span> <span data-ttu-id="2d5e4-107">Sie können diese Nachricht explizit senden oder das Header-"\*"-Makro verwenden. [**\_**](/windows/desktop/api/Commctrl/nf-commctrl-header_setitem)</span><span class="sxs-lookup"><span data-stu-id="2d5e4-107">You can send this message explicitly or use the [**Header\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_setitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2d5e4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d5e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d5e4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2d5e4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2d5e4-110">Der aktuelle Index des Elements, dessen Attribute geändert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2d5e4-110">The current index of the item whose attributes are to be changed.</span></span>

</dd> <dt>

<span data-ttu-id="2d5e4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2d5e4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2d5e4-112">Ein Zeiger auf eine [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) -Struktur, die Element Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="2d5e4-112">A pointer to an [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure that contains item information.</span></span> <span data-ttu-id="2d5e4-113">Wenn diese Nachricht gesendet wird, muss der **Mask** -Member der-Struktur festgelegt werden, um anzugeben, welche Attribute festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2d5e4-113">When this message is sent, the **mask** member of the structure must be set to indicate which attributes are being set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d5e4-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2d5e4-114">Return value</span></span>

<span data-ttu-id="2d5e4-115">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="2d5e4-115">Returns nonzero upon success, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d5e4-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d5e4-116">Remarks</span></span>

<span data-ttu-id="2d5e4-117">Die [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) -Struktur, die diese Meldung unterstützt, unterstützt Element Reihenfolge-und Bildlisten Informationen</span><span class="sxs-lookup"><span data-stu-id="2d5e4-117">The [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure that supports this message supports item order and image list information.</span></span> <span data-ttu-id="2d5e4-118">Mithilfe dieser Member können Sie die Reihenfolge steuern, in der Elemente angezeigt werden, und Bilder angeben, die mit Elementen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2d5e4-118">By using these members, you can control the order in which items are displayed and specify images to appear with items.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d5e4-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d5e4-119">Requirements</span></span>



| <span data-ttu-id="2d5e4-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d5e4-120">Requirement</span></span> | <span data-ttu-id="2d5e4-121">Wert</span><span class="sxs-lookup"><span data-stu-id="2d5e4-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2d5e4-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2d5e4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2d5e4-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2d5e4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2d5e4-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2d5e4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2d5e4-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2d5e4-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2d5e4-126">Header</span><span class="sxs-lookup"><span data-stu-id="2d5e4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d5e4-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d5e4-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="2d5e4-128">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="2d5e4-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2d5e4-129">**HDM \_** "S" (Unicode) und " **HDM \_** " (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2d5e4-129">**HDM\_SETITEMW** (Unicode) and **HDM\_SETITEMA** (ANSI)</span></span><br/>                   |



 

 





