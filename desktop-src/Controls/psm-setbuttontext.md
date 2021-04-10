---
title: PSM_SETBUTTONTEXT Meldung (prsht. h)
description: Legt den Text auf einer Schaltfläche in einem Aero-Assistenten fest. Sie können diese Nachricht explizit oder mithilfe des propsheet- \_ Makros SetButtonText senden.
ms.assetid: 30b7afd1-5094-430f-9c48-d87832d96050
keywords:
- Windows-Steuerelemente für PSM_SETBUTTONTEXT Meldung
topic_type:
- apiref
api_name:
- PSM_SETBUTTONTEXT
- PSM_SETBUTTONTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41a0b55f73fc7084e89f54c1e741d12000b0f949
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040500"
---
# <a name="psm_setbuttontext-message"></a><span data-ttu-id="624d4-105">PSM- \_ SetButtonText-Nachricht</span><span class="sxs-lookup"><span data-stu-id="624d4-105">PSM\_SETBUTTONTEXT message</span></span>

<span data-ttu-id="624d4-106">Legt den Text auf einer Schaltfläche in einem Aero-Assistenten fest.</span><span class="sxs-lookup"><span data-stu-id="624d4-106">Sets the text on a button in an Aero wizard.</span></span> <span data-ttu-id="624d4-107">Sie können diese Nachricht explizit oder mithilfe des [**propsheet-Makros \_ SetButtonText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext) senden.</span><span class="sxs-lookup"><span data-stu-id="624d4-107">You can send this message explicitly or by using the [**PropSheet\_SetButtonText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="624d4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="624d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="624d4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="624d4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="624d4-110">Einer der folgenden Werte, der die Schaltfläche angibt, deren Text festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="624d4-110">One of the following values specifying the button whose text is set.</span></span>



| <span data-ttu-id="624d4-111">Wert</span><span class="sxs-lookup"><span data-stu-id="624d4-111">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="624d4-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="624d4-112">Meaning</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <span data-ttu-id="624d4-113"><dt>**pswizb \_ zurück**</dt></span><span class="sxs-lookup"><span data-stu-id="624d4-113"><dt>**PSWIZB\_BACK**</dt></span></span> </dl>                               | <span data-ttu-id="624d4-114">Die Schaltfläche " **zurück** ".</span><span class="sxs-lookup"><span data-stu-id="624d4-114">The **Back** button.</span></span><br/>   |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <span data-ttu-id="624d4-115"><dt>**pswizb- \_ Abbruch**</dt></span><span class="sxs-lookup"><span data-stu-id="624d4-115"><dt>**PSWIZB\_CANCEL**</dt></span></span> </dl>                         | <span data-ttu-id="624d4-116">Die Schaltfläche " **Abbrechen** ".</span><span class="sxs-lookup"><span data-stu-id="624d4-116">The **Cancel** button.</span></span><br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <span data-ttu-id="624d4-117"><dt>**pswizb \_ disabledfinish**</dt></span><span class="sxs-lookup"><span data-stu-id="624d4-117"><dt>**PSWIZB\_DISABLEDFINISH**</dt></span></span> </dl> | <span data-ttu-id="624d4-118">Die Schaltfläche **Fertig** stellen.</span><span class="sxs-lookup"><span data-stu-id="624d4-118">The **Finish** button.</span></span><br/> |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <span data-ttu-id="624d4-119"><dt>**pswizb- \_ Fertigstellen**</dt></span><span class="sxs-lookup"><span data-stu-id="624d4-119"><dt>**PSWIZB\_FINISH**</dt></span></span> </dl>                         | <span data-ttu-id="624d4-120">Die Schaltfläche **Fertig** stellen.</span><span class="sxs-lookup"><span data-stu-id="624d4-120">The **Finish** button.</span></span><br/> |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <span data-ttu-id="624d4-121"><dt>**pswizb \_ als nächstes**</dt></span><span class="sxs-lookup"><span data-stu-id="624d4-121"><dt>**PSWIZB\_NEXT**</dt></span></span> </dl>                               | <span data-ttu-id="624d4-122">Die Schaltfläche **weiter** .</span><span class="sxs-lookup"><span data-stu-id="624d4-122">The **Next** button.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="624d4-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="624d4-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="624d4-124">Der festzulegende Text.</span><span class="sxs-lookup"><span data-stu-id="624d4-124">The text to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="624d4-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="624d4-125">Return value</span></span>

<span data-ttu-id="624d4-126">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="624d4-126">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="624d4-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="624d4-127">Requirements</span></span>



| <span data-ttu-id="624d4-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="624d4-128">Requirement</span></span> | <span data-ttu-id="624d4-129">Wert</span><span class="sxs-lookup"><span data-stu-id="624d4-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="624d4-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="624d4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="624d4-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="624d4-131">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="624d4-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="624d4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="624d4-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="624d4-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="624d4-134">Header</span><span class="sxs-lookup"><span data-stu-id="624d4-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="624d4-135"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="624d4-135"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="624d4-136">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="624d4-136">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="624d4-137">**PSM \_ Setbuttontextw** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="624d4-137">**PSM\_SETBUTTONTEXTW** (Unicode)</span></span><br/>                                       |



 

 





