---
title: BCM_GETSPLITINFO Meldung (kommstrg. h)
description: Ruft Informationen für ein unterteilte Schaltflächen Steuerelement ab. Senden Sie diese Nachricht explizit oder mithilfe des Schaltflächen \_ getsplitinfo-Makros.
ms.assetid: d608440d-b8d8-4e32-9128-08b7566b185c
keywords:
- Windows-Steuerelemente für BCM_GETSPLITINFO Meldung
topic_type:
- apiref
api_name:
- BCM_GETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 162c5522fcb432e3d512f688ae24aa12d4d0d8e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956544"
---
# <a name="bcm_getsplitinfo-message"></a><span data-ttu-id="291cf-105">BCM \_ getsplitinfo-Meldung</span><span class="sxs-lookup"><span data-stu-id="291cf-105">BCM\_GETSPLITINFO message</span></span>

<span data-ttu-id="291cf-106">Ruft Informationen für ein unterteilte Schaltflächen Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="291cf-106">Gets information for a split button control.</span></span> <span data-ttu-id="291cf-107">Senden Sie diese Nachricht explizit oder mithilfe des [**Schaltflächen \_ getsplitinfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo) -Makros.</span><span class="sxs-lookup"><span data-stu-id="291cf-107">Send this message explicitly or by using the [**Button\_GetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="291cf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="291cf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="291cf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="291cf-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="291cf-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="291cf-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="291cf-111">*LPARAM* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="291cf-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="291cf-112">Ein Zeiger auf eine [**\_ splitinfo**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) -Struktur der Schaltfläche, um Informationen über die Schaltfläche zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="291cf-112">A pointer to a [**BUTTON\_SPLITINFO**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) structure to receive information on the button.</span></span> <span data-ttu-id="291cf-113">Der Aufrufer ist dafür verantwortlich, den Arbeitsspeicher für die Struktur zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="291cf-113">The caller is responsible for allocating the memory for the structure.</span></span> <span data-ttu-id="291cf-114">Legen Sie den **Mask** -Member dieser Struktur fest, um zu bestimmen, welche Informationen empfangen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="291cf-114">Set the **mask** member of this structure to determine what information to receive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="291cf-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="291cf-115">Return value</span></span>

<span data-ttu-id="291cf-116">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="291cf-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="291cf-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="291cf-117">Remarks</span></span>

<span data-ttu-id="291cf-118">Verwenden Sie diese Meldung nur mit den Schaltflächen Stilen [**\_ SplitButton**](button-styles.md) und [**SB \_ defsplitbutton**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="291cf-118">Use this message only with the [**BS\_SPLITBUTTON**](button-styles.md) and [**BS\_DEFSPLITBUTTON**](button-styles.md) button styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="291cf-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="291cf-119">Requirements</span></span>



| <span data-ttu-id="291cf-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="291cf-120">Requirement</span></span> | <span data-ttu-id="291cf-121">Wert</span><span class="sxs-lookup"><span data-stu-id="291cf-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="291cf-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="291cf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="291cf-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="291cf-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="291cf-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="291cf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="291cf-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="291cf-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="291cf-126">Header</span><span class="sxs-lookup"><span data-stu-id="291cf-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="291cf-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="291cf-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="291cf-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="291cf-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="291cf-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="291cf-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="291cf-130">Schaltflächenstile</span><span class="sxs-lookup"><span data-stu-id="291cf-130">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="291cf-131">**Licher**</span><span class="sxs-lookup"><span data-stu-id="291cf-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="291cf-132">Schaltflächentypen</span><span class="sxs-lookup"><span data-stu-id="291cf-132">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 





