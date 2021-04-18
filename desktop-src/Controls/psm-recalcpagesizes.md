---
title: PSM_RECALCPAGESIZES Meldung (prsht. h)
description: Berechnet die Seitengröße eines Standard-oder Assistenten-Eigenschaften Blatts neu, nachdem Seiten hinzugefügt oder entfernt wurden. Sie können diese Nachricht explizit senden oder das propsheet \_ recalcpagesizes-Makro verwenden.
ms.assetid: 42257ea3-0471-4c67-adcd-01cd2669a51e
keywords:
- Windows-Steuerelemente für PSM_RECALCPAGESIZES Meldung
topic_type:
- apiref
api_name:
- PSM_RECALCPAGESIZES
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ae2030f432e8c52ed6208be34d429b4579edb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338779"
---
# <a name="psm_recalcpagesizes-message"></a><span data-ttu-id="63a19-105">PSM- \_ Nachricht "recalcpagesizes"</span><span class="sxs-lookup"><span data-stu-id="63a19-105">PSM\_RECALCPAGESIZES message</span></span>

<span data-ttu-id="63a19-106">Berechnet die Seitengröße eines Standard-oder Assistenten-Eigenschaften Blatts neu, nachdem Seiten hinzugefügt oder entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="63a19-106">Recalculates the page size of a standard or wizard property sheet after pages have been added or removed.</span></span> <span data-ttu-id="63a19-107">Sie können diese Nachricht explizit senden oder das [**propsheet \_ recalcpagesizes**](/windows/desktop/api/Prsht/nf-prsht-propsheet_recalcpagesizes) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="63a19-107">You can send this message explicitly or use the [**PropSheet\_RecalcPageSizes**](/windows/desktop/api/Prsht/nf-prsht-propsheet_recalcpagesizes) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="63a19-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="63a19-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63a19-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="63a19-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63a19-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="63a19-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="63a19-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="63a19-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63a19-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="63a19-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63a19-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="63a19-113">Return value</span></span>

<span data-ttu-id="63a19-114">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="63a19-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="63a19-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="63a19-115">Remarks</span></span>

<span data-ttu-id="63a19-116">Wenn ein Eigenschaften Blatt erstellt wird, wird es an seine anfängliche Auflistung von Seiten angepasst.</span><span class="sxs-lookup"><span data-stu-id="63a19-116">When a property sheet is created, it is sized to fit its initial collection of pages.</span></span> <span data-ttu-id="63a19-117">Um die Kompatibilität mit früheren Versionen der allgemeinen Steuerelemente aufrechtzuerhalten, ändern sich Eigenschaften Blätter und Assistenten nicht automatisch selbst, wenn Seiten später hinzugefügt oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="63a19-117">In order to maintain compatibility with previous versions of the common controls, property sheets and wizards do not automatically resize themselves when pages are subsequently added or removed.</span></span> <span data-ttu-id="63a19-118">Mit der Common Controls- [Version 5,80](common-control-versions.md)sollten Anwendungen nach dem Hinzufügen oder Entfernen von Seiten mit [**PSM \_ addPage**](psm-addpage.md), [**PSM \_ insertpage**](psm-insertpage.md), [**PSM \_ RemovePage**](psm-removepage.md)oder Ihren äquivalenten Makros eine PSM-Nachricht " **\_ recalcpagesizes** " senden.</span><span class="sxs-lookup"><span data-stu-id="63a19-118">With common controls [version 5.80](common-control-versions.md), applications should send a **PSM\_RECALCPAGESIZES** message after adding or removing pages with [**PSM\_ADDPAGE**](psm-addpage.md), [**PSM\_INSERTPAGE**](psm-insertpage.md), [**PSM\_REMOVEPAGE**](psm-removepage.md), or their equivalent macros.</span></span> <span data-ttu-id="63a19-119">Dadurch wird sichergestellt, dass das Eigenschaften Blatt für die aktuelle Auflistung von Seiten ordnungsgemäß vergrößert wird.</span><span class="sxs-lookup"><span data-stu-id="63a19-119">It ensures that the property sheet is properly sized for its current collection of pages.</span></span> <span data-ttu-id="63a19-120">Wenn diese Nachricht nicht gesendet wird, können einige Eigenschaften Blattseiten abgeschnitten oder zu groß sein.</span><span class="sxs-lookup"><span data-stu-id="63a19-120">If this message is not sent, some property sheet pages may be truncated or too large.</span></span>

> [!Note]  
> <span data-ttu-id="63a19-121">Diese Meldung wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="63a19-121">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="63a19-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63a19-122">Requirements</span></span>



| <span data-ttu-id="63a19-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63a19-123">Requirement</span></span> | <span data-ttu-id="63a19-124">Wert</span><span class="sxs-lookup"><span data-stu-id="63a19-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="63a19-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="63a19-125">Minimum supported client</span></span><br/> | <span data-ttu-id="63a19-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="63a19-126">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="63a19-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="63a19-127">Minimum supported server</span></span><br/> | <span data-ttu-id="63a19-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="63a19-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="63a19-129">Header</span><span class="sxs-lookup"><span data-stu-id="63a19-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="63a19-130"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="63a19-130"><dt>Prsht.h</dt></span></span> </dl> |



 

 





