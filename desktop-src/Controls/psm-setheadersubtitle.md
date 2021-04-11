---
title: PSM_SETHEADERSUBTITLE Meldung (prsht. h)
description: Legt den Untertitel Text für den Header der inneren Seite eines Assistenten fest. Sie können diese Nachricht explizit senden oder das propsheet-unter \_ Titel-Makro verwenden.
ms.assetid: 6ef3017b-8a20-4d62-a604-135410d8bdf7
keywords:
- Windows-Steuerelemente für PSM_SETHEADERSUBTITLE Meldung
topic_type:
- apiref
api_name:
- PSM_SETHEADERSUBTITLE
- PSM_SETHEADERSUBTITLEA
- PSM_SETHEADERSUBTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d73376b5ed35f20b43c743b31a4a78d3a4fa809
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949817"
---
# <a name="psm_setheadersubtitle-message"></a><span data-ttu-id="02b0d-105">PSM- \_ abadertitel-Nachricht</span><span class="sxs-lookup"><span data-stu-id="02b0d-105">PSM\_SETHEADERSUBTITLE message</span></span>

<span data-ttu-id="02b0d-106">Legt den Untertitel Text für den Header der inneren Seite eines Assistenten fest.</span><span class="sxs-lookup"><span data-stu-id="02b0d-106">Sets the subtitle text for the header of a wizard's interior page.</span></span> <span data-ttu-id="02b0d-107">Sie können diese Nachricht explizit senden oder das [**propsheet-unter \_ Titel**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadersubtitle) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="02b0d-107">You can send this message explicitly or use the [**PropSheet\_SetHeaderSubTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadersubtitle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="02b0d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="02b0d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02b0d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="02b0d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="02b0d-110">Der null basierte Index der Seite des Assistenten.</span><span class="sxs-lookup"><span data-stu-id="02b0d-110">Zero-based index of the wizard's page.</span></span>

</dd> <dt>

<span data-ttu-id="02b0d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="02b0d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="02b0d-112">Neuer Header Untertitel.</span><span class="sxs-lookup"><span data-stu-id="02b0d-112">New header subtitle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02b0d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02b0d-113">Return value</span></span>

<span data-ttu-id="02b0d-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="02b0d-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="02b0d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02b0d-115">Remarks</span></span>

<span data-ttu-id="02b0d-116">Wenn Sie die aktuelle Seite angeben, wird Sie sofort neu gezeichnet, um den neuen Untertitel anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="02b0d-116">If you specify the current page, it will immediately be repainted to display the new subtitle.</span></span>

> [!Note]  
> <span data-ttu-id="02b0d-117">Diese Meldung wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="02b0d-117">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="02b0d-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02b0d-118">Requirements</span></span>



| <span data-ttu-id="02b0d-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02b0d-119">Requirement</span></span> | <span data-ttu-id="02b0d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="02b0d-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02b0d-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="02b0d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="02b0d-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02b0d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="02b0d-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="02b0d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="02b0d-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02b0d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="02b0d-125">Header</span><span class="sxs-lookup"><span data-stu-id="02b0d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="02b0d-126"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="02b0d-126"><dt>Prsht.h</dt></span></span> </dl>      |
| <span data-ttu-id="02b0d-127">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="02b0d-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="02b0d-128">**PSM \_ "SDer adersubtitlew** (Unicode)" und "PSM"-"Setup" (ANSI) **\_**</span><span class="sxs-lookup"><span data-stu-id="02b0d-128">**PSM\_SETHEADERSUBTITLEW** (Unicode) and **PSM\_SETHEADERSUBTITLEA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="02b0d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02b0d-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="02b0d-130">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="02b0d-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="02b0d-131">**PSM \_ hwndumindex**</span><span class="sxs-lookup"><span data-stu-id="02b0d-131">**PSM\_HWNDTOINDEX**</span></span>](psm-hwndtoindex.md)
</dt> <dt>

[<span data-ttu-id="02b0d-132">**PSM \_ idumindex**</span><span class="sxs-lookup"><span data-stu-id="02b0d-132">**PSM\_IDTOINDEX**</span></span>](psm-idtoindex.md)
</dt> <dt>

[<span data-ttu-id="02b0d-133">**PSM- \_ pageumindex**</span><span class="sxs-lookup"><span data-stu-id="02b0d-133">**PSM\_PAGETOINDEX**</span></span>](psm-pagetoindex.md)
</dt> </dl>

 

 





