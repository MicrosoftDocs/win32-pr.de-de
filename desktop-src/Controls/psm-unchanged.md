---
title: PSM_UNCHANGED Meldung (prsht. h)
description: Teilt einem Eigenschaften Blatt mit, dass die Informationen in einer Seite in den zuvor gespeicherten Zustand zurückversetzt wurden. Sie können diese Nachricht explizit oder mithilfe des unveränderten propsheet- \_ Makros senden.
ms.assetid: 61c15dec-40d0-4720-a117-4eed765c8819
keywords:
- Windows-Steuerelemente für PSM_UNCHANGED Meldung
topic_type:
- apiref
api_name:
- PSM_UNCHANGED
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb1d6216f94afd610bb49710a3e84b4c21a673f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213740"
---
# <a name="psm_unchanged-message"></a><span data-ttu-id="cf420-105">PSM- \_ Nachricht unverändert</span><span class="sxs-lookup"><span data-stu-id="cf420-105">PSM\_UNCHANGED message</span></span>

<span data-ttu-id="cf420-106">Teilt einem Eigenschaften Blatt mit, dass die Informationen in einer Seite in den zuvor gespeicherten Zustand zurückversetzt wurden.</span><span class="sxs-lookup"><span data-stu-id="cf420-106">Informs a property sheet that information in a page has reverted to the previously saved state.</span></span> <span data-ttu-id="cf420-107">Sie können diese Nachricht explizit oder mithilfe des [**\_ unveränderten propsheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_unchanged) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="cf420-107">You can send this message explicitly or by using the [**PropSheet\_UnChanged**](/windows/desktop/api/Prsht/nf-prsht-propsheet_unchanged) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cf420-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf420-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf420-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cf420-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf420-110">Handle für die Seite, die in den zuvor gespeicherten Zustand zurückversetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="cf420-110">Handle to the page that has reverted to the previously saved state.</span></span>

</dd> <dt>

<span data-ttu-id="cf420-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cf420-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf420-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="cf420-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf420-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf420-113">Return value</span></span>

<span data-ttu-id="cf420-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="cf420-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf420-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf420-115">Remarks</span></span>

<span data-ttu-id="cf420-116">Auf dem Eigenschaften Blatt wird die Schaltfläche **anwenden** deaktiviert, wenn keine anderen Seiten Änderungen mit dem Eigenschaften Blatt registriert haben.</span><span class="sxs-lookup"><span data-stu-id="cf420-116">The property sheet disables the **Apply** button if no other pages have registered changes with the property sheet.</span></span>

> [!Note]  
> <span data-ttu-id="cf420-117">Diese Meldung wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cf420-117">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cf420-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf420-118">Requirements</span></span>



| <span data-ttu-id="cf420-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf420-119">Requirement</span></span> | <span data-ttu-id="cf420-120">Wert</span><span class="sxs-lookup"><span data-stu-id="cf420-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cf420-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cf420-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cf420-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf420-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cf420-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cf420-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cf420-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf420-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cf420-125">Header</span><span class="sxs-lookup"><span data-stu-id="cf420-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf420-126"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf420-126"><dt>Prsht.h</dt></span></span> </dl> |



 

 





