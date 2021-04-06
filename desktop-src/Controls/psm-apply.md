---
title: PSM_APPLY Meldung (prsht. h)
description: Simuliert die Auswahl der Schaltfläche anwenden und gibt an, dass sich mindestens eine Seite geändert hat und die Änderungen überprüft und aufgezeichnet werden müssen.
ms.assetid: 2948fb66-ad77-4552-88b6-455418515e4c
keywords:
- Windows-Steuerelemente für PSM_APPLY Meldung
topic_type:
- apiref
api_name:
- PSM_APPLY
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67d798d4a9a2f780ac81cc84c90a57d0efd4e299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859122"
---
# <a name="psm_apply-message"></a><span data-ttu-id="812af-104">PSM- \_ Nachricht anwenden</span><span class="sxs-lookup"><span data-stu-id="812af-104">PSM\_APPLY message</span></span>

<span data-ttu-id="812af-105">Simuliert die Auswahl der Schaltfläche **anwenden** und gibt an, dass sich mindestens eine Seite geändert hat und die Änderungen überprüft und aufgezeichnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="812af-105">Simulates the selection of the **Apply** button, indicating that one or more pages have changed and the changes need to be validated and recorded.</span></span>

## <a name="parameters"></a><span data-ttu-id="812af-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="812af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="812af-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="812af-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="812af-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="812af-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="812af-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="812af-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="812af-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="812af-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="812af-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="812af-111">Return value</span></span>

<span data-ttu-id="812af-112">Gibt **true** zurück, wenn alle Seiten die Änderungen erfolgreich angewendet haben, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="812af-112">Returns **TRUE** if all pages successfully applied the changes, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="812af-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="812af-113">Remarks</span></span>

<span data-ttu-id="812af-114">Das Eigenschaften Blatt sendet den Benachrichtigungs Code " [PSN \_ killactive](psn-killactive.md) " an die aktuelle Seite.</span><span class="sxs-lookup"><span data-stu-id="812af-114">The property sheet sends the [PSN\_KILLACTIVE](psn-killactive.md) notification code to the current page.</span></span> <span data-ttu-id="812af-115">Wenn die aktuelle Seite **false** zurückgibt, sendet das Eigenschaften Blatt den " [PSN \_ Apply](psn-apply.md) "-Benachrichtigungs Code auf alle aktiven Seiten.</span><span class="sxs-lookup"><span data-stu-id="812af-115">If the current page returns **FALSE**, the property sheet sends the [PSN\_APPLY](psn-apply.md) notification code to all active pages.</span></span> <span data-ttu-id="812af-116">Sie können die PSM-Anwendungs \_ Nachricht explizit oder mithilfe des [**propsheet \_ Apply**](/windows/desktop/api/Prsht/nf-prsht-propsheet_apply) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="812af-116">You can send the PSM\_APPLY message explicitly or by using the [**PropSheet\_Apply**](/windows/desktop/api/Prsht/nf-prsht-propsheet_apply) macro.</span></span>

> [!Note]  
> <span data-ttu-id="812af-117">Diese Meldung wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="812af-117">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="812af-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="812af-118">Requirements</span></span>



| <span data-ttu-id="812af-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="812af-119">Requirement</span></span> | <span data-ttu-id="812af-120">Wert</span><span class="sxs-lookup"><span data-stu-id="812af-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="812af-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="812af-121">Minimum supported client</span></span><br/> | <span data-ttu-id="812af-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="812af-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="812af-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="812af-123">Minimum supported server</span></span><br/> | <span data-ttu-id="812af-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="812af-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="812af-125">Header</span><span class="sxs-lookup"><span data-stu-id="812af-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="812af-126"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="812af-126"><dt>Prsht.h</dt></span></span> </dl> |



 

 





