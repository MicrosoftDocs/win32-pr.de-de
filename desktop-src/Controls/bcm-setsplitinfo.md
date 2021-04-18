---
title: BCM_SETSPLITINFO Meldung (kommstrg. h)
description: Legt Informationen für ein unterteilte Schaltflächen Steuerelement fest. Senden Sie diese Nachricht explizit oder mithilfe der Schaltfläche \_ setsplitinfo-Makro.
ms.assetid: 609b8972-9616-4850-a72c-2f87ce19f563
keywords:
- Windows-Steuerelemente für BCM_SETSPLITINFO Meldung
topic_type:
- apiref
api_name:
- BCM_SETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac40f2d1ef016ee76ab21ccf2dc4733d0ff427f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340794"
---
# <a name="bcm_setsplitinfo-message"></a><span data-ttu-id="0904c-105">BCM- \_ setsplitinfo-Meldung</span><span class="sxs-lookup"><span data-stu-id="0904c-105">BCM\_SETSPLITINFO message</span></span>

<span data-ttu-id="0904c-106">Legt Informationen für ein unterteilte Schaltflächen Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="0904c-106">Sets information for a split button control.</span></span> <span data-ttu-id="0904c-107">Senden Sie diese Nachricht explizit oder mithilfe der [**Schaltfläche \_ setsplitinfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) -Makro.</span><span class="sxs-lookup"><span data-stu-id="0904c-107">Send this message explicitly or by using the [**Button\_SetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0904c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0904c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0904c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0904c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0904c-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="0904c-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="0904c-111">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0904c-111">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0904c-112">Ein Zeiger auf eine [**\_ splitinfo**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) -Struktur der Schaltfläche, die Informationen über die unterteilte Schaltfläche enthält.</span><span class="sxs-lookup"><span data-stu-id="0904c-112">A pointer to a [**BUTTON\_SPLITINFO**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) structure containing information about the split button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0904c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0904c-113">Return value</span></span>

<span data-ttu-id="0904c-114">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="0904c-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0904c-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0904c-115">Remarks</span></span>

<span data-ttu-id="0904c-116">Verwenden Sie diese Meldung nur mit den Schaltflächen Stilen [**\_ SplitButton**](button-styles.md) und [**SB \_ defsplitbutton**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="0904c-116">Use this message only with the [**BS\_SPLITBUTTON**](button-styles.md) and [**BS\_DEFSPLITBUTTON**](button-styles.md) button styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="0904c-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0904c-117">Requirements</span></span>



| <span data-ttu-id="0904c-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0904c-118">Requirement</span></span> | <span data-ttu-id="0904c-119">Wert</span><span class="sxs-lookup"><span data-stu-id="0904c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0904c-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0904c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0904c-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0904c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0904c-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0904c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0904c-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0904c-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0904c-124">Header</span><span class="sxs-lookup"><span data-stu-id="0904c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0904c-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="0904c-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0904c-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0904c-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="0904c-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="0904c-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0904c-128">Schaltflächenstile</span><span class="sxs-lookup"><span data-stu-id="0904c-128">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="0904c-129">**Licher**</span><span class="sxs-lookup"><span data-stu-id="0904c-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0904c-130">Schaltflächentypen</span><span class="sxs-lookup"><span data-stu-id="0904c-130">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 





