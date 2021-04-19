---
title: PSM_SETHEADERTITLE Meldung (prsht. h)
description: Legt den Titeltext für den Header der inneren Seite eines Assistenten fest. Sie können diese Nachricht explizit senden oder das propsheet-" \_ .
ms.assetid: 19d4badf-d99d-4a28-92d4-33bcf5d23944
keywords:
- Windows-Steuerelemente für PSM_SETHEADERTITLE Meldung
topic_type:
- apiref
api_name:
- PSM_SETHEADERTITLE
- PSM_SETHEADERTITLEA
- PSM_SETHEADERTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8140eef4aa09e9dd19d8baaf8193a836b105482e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342403"
---
# <a name="psm_setheadertitle-message"></a><span data-ttu-id="128fc-105">PSM-Einstellungs \_ Titel Meldung</span><span class="sxs-lookup"><span data-stu-id="128fc-105">PSM\_SETHEADERTITLE message</span></span>

<span data-ttu-id="128fc-106">Legt den Titeltext für den Header der inneren Seite eines Assistenten fest.</span><span class="sxs-lookup"><span data-stu-id="128fc-106">Sets the title text for the header of a wizard's interior page.</span></span> <span data-ttu-id="128fc-107">Sie können diese Nachricht explizit senden oder das [**propsheet- \_**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadertitle) ".</span><span class="sxs-lookup"><span data-stu-id="128fc-107">You can send this message explicitly or use the [**PropSheet\_SetHeaderTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadertitle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="128fc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="128fc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="128fc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="128fc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="128fc-110">Der null basierte Index der Seite des Assistenten.</span><span class="sxs-lookup"><span data-stu-id="128fc-110">Zero-based index of the wizard's page.</span></span>

</dd> <dt>

<span data-ttu-id="128fc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="128fc-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="128fc-112">Neuer Header Untertitel.</span><span class="sxs-lookup"><span data-stu-id="128fc-112">New header subtitle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="128fc-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="128fc-113">Return value</span></span>

<span data-ttu-id="128fc-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="128fc-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="128fc-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="128fc-115">Remarks</span></span>

<span data-ttu-id="128fc-116">Wenn Sie die aktuelle Seite angeben, wird Sie sofort neu gezeichnet, um den neuen Titel anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="128fc-116">If you specify the current page, it will immediately be repainted to display the new title.</span></span>

## <a name="requirements"></a><span data-ttu-id="128fc-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="128fc-117">Requirements</span></span>



| <span data-ttu-id="128fc-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="128fc-118">Requirement</span></span> | <span data-ttu-id="128fc-119">Wert</span><span class="sxs-lookup"><span data-stu-id="128fc-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="128fc-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="128fc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="128fc-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="128fc-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="128fc-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="128fc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="128fc-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="128fc-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="128fc-124">Header</span><span class="sxs-lookup"><span data-stu-id="128fc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="128fc-125"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="128fc-125"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="128fc-126">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="128fc-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="128fc-127">**PSM \_ "Sderadertitlew** " (Unicode) und "PSM"-"Setup" (ANSI) **\_**</span><span class="sxs-lookup"><span data-stu-id="128fc-127">**PSM\_SETHEADERTITLEW** (Unicode) and **PSM\_SETHEADERTITLEA** (ANSI)</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="128fc-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="128fc-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="128fc-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="128fc-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="128fc-130">**PSM \_ hwndumindex**</span><span class="sxs-lookup"><span data-stu-id="128fc-130">**PSM\_HWNDTOINDEX**</span></span>](psm-hwndtoindex.md)
</dt> <dt>

[<span data-ttu-id="128fc-131">**PSM \_ idumindex**</span><span class="sxs-lookup"><span data-stu-id="128fc-131">**PSM\_IDTOINDEX**</span></span>](psm-idtoindex.md)
</dt> <dt>

[<span data-ttu-id="128fc-132">**PSM- \_ pageumindex**</span><span class="sxs-lookup"><span data-stu-id="128fc-132">**PSM\_PAGETOINDEX**</span></span>](psm-pagetoindex.md)
</dt> </dl>

 

 





