---
title: PSM_CHANGED Meldung (prsht. h)
description: Teilt einem Eigenschaften Blatt mit, dass sich die Informationen in einer Seite geändert haben. Sie können diese Nachricht explizit oder mithilfe des von propsheet \_ geänderten Makros senden.
ms.assetid: b092969f-31dc-4e3c-9100-d15f1bdd5aa5
keywords:
- Windows-Steuerelemente für PSM_CHANGED Meldung
topic_type:
- apiref
api_name:
- PSM_CHANGED
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57f931db5e25f816f7ea164ca5871a4e3e7757a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338759"
---
# <a name="psm_changed-message"></a><span data-ttu-id="67e5e-105">PSM- \_ geänderte Nachricht</span><span class="sxs-lookup"><span data-stu-id="67e5e-105">PSM\_CHANGED message</span></span>

<span data-ttu-id="67e5e-106">Teilt einem Eigenschaften Blatt mit, dass sich die Informationen in einer Seite geändert haben.</span><span class="sxs-lookup"><span data-stu-id="67e5e-106">Informs a property sheet that information in a page has changed.</span></span> <span data-ttu-id="67e5e-107">Sie können diese Nachricht explizit oder mithilfe des von [**propsheet \_ geänderten**](/windows/desktop/api/Prsht/nf-prsht-propsheet_changed) Makros senden.</span><span class="sxs-lookup"><span data-stu-id="67e5e-107">You can send this message explicitly or by using the [**PropSheet\_Changed**](/windows/desktop/api/Prsht/nf-prsht-propsheet_changed) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="67e5e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="67e5e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67e5e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="67e5e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67e5e-110">Handle der Seite, die geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="67e5e-110">Handle to the page that has changed.</span></span>

</dd> <dt>

<span data-ttu-id="67e5e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="67e5e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67e5e-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="67e5e-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67e5e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="67e5e-113">Return value</span></span>

<span data-ttu-id="67e5e-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="67e5e-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="67e5e-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67e5e-115">Remarks</span></span>

<span data-ttu-id="67e5e-116">Auf dem Eigenschaften Blatt wird die Schaltfläche **anwenden** aktiviert.</span><span class="sxs-lookup"><span data-stu-id="67e5e-116">The property sheet will enable the **Apply** button.</span></span>

> [!Note]  
> <span data-ttu-id="67e5e-117">Diese Meldung wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="67e5e-117">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="67e5e-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67e5e-118">Requirements</span></span>



| <span data-ttu-id="67e5e-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67e5e-119">Requirement</span></span> | <span data-ttu-id="67e5e-120">Wert</span><span class="sxs-lookup"><span data-stu-id="67e5e-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="67e5e-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="67e5e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="67e5e-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67e5e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="67e5e-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="67e5e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="67e5e-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67e5e-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="67e5e-125">Header</span><span class="sxs-lookup"><span data-stu-id="67e5e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="67e5e-126"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="67e5e-126"><dt>Prsht.h</dt></span></span> </dl> |



 

 





