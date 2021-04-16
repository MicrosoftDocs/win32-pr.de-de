---
title: PSM_PRESSBUTTON Meldung (prsht. h)
description: Simuliert die Auswahl einer Eigenschaften Blatt Schaltfläche. Sie können diese Nachricht explizit oder mithilfe des-propsheet- \_ pressbutton-Makros senden.
ms.assetid: 82a55a29-d916-47ee-b0a0-f685a3a386d9
keywords:
- Windows-Steuerelemente für PSM_PRESSBUTTON Meldung
topic_type:
- apiref
api_name:
- PSM_PRESSBUTTON
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b54b04dcc7b1263019f49ff8c1de0d2c21a12a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479410"
---
# <a name="psm_pressbutton-message"></a><span data-ttu-id="79f16-105">PSM- \_ pressbutton-Meldung</span><span class="sxs-lookup"><span data-stu-id="79f16-105">PSM\_PRESSBUTTON message</span></span>

<span data-ttu-id="79f16-106">Simuliert die Auswahl einer Eigenschaften Blatt Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="79f16-106">Simulates the selection of a property sheet button.</span></span> <span data-ttu-id="79f16-107">Sie können diese Nachricht explizit oder mithilfe des- [**propsheet- \_ pressbutton**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pressbutton) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="79f16-107">You can send this message explicitly or by using the [**PropSheet\_PressButton**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pressbutton) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="79f16-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="79f16-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79f16-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="79f16-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="79f16-110">Index der auszuwählen Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="79f16-110">Index of the button to select.</span></span> <span data-ttu-id="79f16-111">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="79f16-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="79f16-112">Wert</span><span class="sxs-lookup"><span data-stu-id="79f16-112">Value</span></span>                                                                                                                                                            | <span data-ttu-id="79f16-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="79f16-113">Meaning</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PSBTN_APPLYNOW"></span><span id="psbtn_applynow"></span><dl> <span data-ttu-id="79f16-114"><dt>**psbtn \_ applynow**</dt></span><span class="sxs-lookup"><span data-stu-id="79f16-114"><dt>**PSBTN\_APPLYNOW**</dt></span></span> </dl> | <span data-ttu-id="79f16-115">Wählt die **Schalt** Fläche übernehmen aus.</span><span class="sxs-lookup"><span data-stu-id="79f16-115">Selects the **Apply** button.</span></span> <span data-ttu-id="79f16-116">Dieser Wert ist nicht gültig, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="79f16-116">This value is not valid when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span><br/> |
| <span id="PSBTN_BACK"></span><span id="psbtn_back"></span><dl> <span data-ttu-id="79f16-117"><dt>**psbtn \_ zurück**</dt></span><span class="sxs-lookup"><span data-stu-id="79f16-117"><dt>**PSBTN\_BACK**</dt></span></span> </dl>             | <span data-ttu-id="79f16-118">Wählt die Schaltfläche **zurück** aus.</span><span class="sxs-lookup"><span data-stu-id="79f16-118">Selects the **Back** button.</span></span><br/>                                                                                                         |
| <span id="PSBTN_CANCEL"></span><span id="psbtn_cancel"></span><dl> <span data-ttu-id="79f16-119"><dt>**psbtn \_ Abbrechen**</dt></span><span class="sxs-lookup"><span data-stu-id="79f16-119"><dt>**PSBTN\_CANCEL**</dt></span></span> </dl>       | <span data-ttu-id="79f16-120">Wählt die Schaltfläche **Abbrechen** aus.</span><span class="sxs-lookup"><span data-stu-id="79f16-120">Selects the **Cancel** button.</span></span><br/>                                                                                                       |
| <span id="PSBTN_FINISH"></span><span id="psbtn_finish"></span><dl> <span data-ttu-id="79f16-121"><dt>**psbtn- \_ Fertigstellen**</dt></span><span class="sxs-lookup"><span data-stu-id="79f16-121"><dt>**PSBTN\_FINISH**</dt></span></span> </dl>       | <span data-ttu-id="79f16-122">Wählt die Schaltfläche **Fertig** stellen aus.</span><span class="sxs-lookup"><span data-stu-id="79f16-122">Selects the **Finish** button.</span></span><br/>                                                                                                       |
| <span id="PSBTN_HELP"></span><span id="psbtn_help"></span><dl> <span data-ttu-id="79f16-123"><dt>**psbtn- \_ Hilfe**</dt></span><span class="sxs-lookup"><span data-stu-id="79f16-123"><dt>**PSBTN\_HELP**</dt></span></span> </dl>             | <span data-ttu-id="79f16-124">Wählt die Schaltfläche **Hilfe** aus.</span><span class="sxs-lookup"><span data-stu-id="79f16-124">Selects the **Help** button.</span></span> <span data-ttu-id="79f16-125">Dieser Wert ist nicht gültig, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="79f16-125">This value is not valid when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span><br/>  |
| <span id="PSBTN_NEXT"></span><span id="psbtn_next"></span><dl> <span data-ttu-id="79f16-126"><dt>**psbtn \_ als nächstes**</dt></span><span class="sxs-lookup"><span data-stu-id="79f16-126"><dt>**PSBTN\_NEXT**</dt></span></span> </dl>             | <span data-ttu-id="79f16-127">Wählt die Schaltfläche **weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="79f16-127">Selects the **Next** button.</span></span><br/>                                                                                                         |
| <span id="PSBTN_OK"></span><span id="psbtn_ok"></span><dl> <span data-ttu-id="79f16-128"><dt>**psbtn \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="79f16-128"><dt>**PSBTN\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="79f16-129">Wählt die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="79f16-129">Selects the **OK** button.</span></span> <span data-ttu-id="79f16-130">Dieser Wert ist nicht gültig, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="79f16-130">This value is not valid when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="79f16-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="79f16-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="79f16-132">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="79f16-132">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79f16-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="79f16-133">Return value</span></span>

<span data-ttu-id="79f16-134">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="79f16-134">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="79f16-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79f16-135">Requirements</span></span>



| <span data-ttu-id="79f16-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79f16-136">Requirement</span></span> | <span data-ttu-id="79f16-137">Wert</span><span class="sxs-lookup"><span data-stu-id="79f16-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="79f16-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="79f16-138">Minimum supported client</span></span><br/> | <span data-ttu-id="79f16-139">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79f16-139">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="79f16-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="79f16-140">Minimum supported server</span></span><br/> | <span data-ttu-id="79f16-141">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79f16-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="79f16-142">Header</span><span class="sxs-lookup"><span data-stu-id="79f16-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="79f16-143"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="79f16-143"><dt>Prsht.h</dt></span></span> </dl> |



 

 





