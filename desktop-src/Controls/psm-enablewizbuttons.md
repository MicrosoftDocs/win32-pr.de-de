---
title: PSM_ENABLEWIZBUTTONS Meldung (prsht. h)
description: Aktiviert oder deaktiviert alle Standard Schaltflächen in einem Aero-Assistenten. Sie können diese Nachricht explizit senden oder das propsheet \_ enablewizbuttons-Makro verwenden.
ms.assetid: 9e8ff2dc-c0e7-4754-8be2-2c7b65a524f4
keywords:
- Windows-Steuerelemente für PSM_ENABLEWIZBUTTONS Meldung
topic_type:
- apiref
api_name:
- PSM_ENABLEWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01fb30fa3337aed369c2cd24a1296785bd6b3a79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956718"
---
# <a name="psm_enablewizbuttons-message"></a><span data-ttu-id="bf7cb-105">PSM \_ enablewizbuttons-Meldung</span><span class="sxs-lookup"><span data-stu-id="bf7cb-105">PSM\_ENABLEWIZBUTTONS message</span></span>

<span data-ttu-id="bf7cb-106">Aktiviert oder deaktiviert alle Standard Schaltflächen in einem Aero-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="bf7cb-106">Enables or disables any of the standard buttons in an Aero wizard.</span></span> <span data-ttu-id="bf7cb-107">Sie können diese Nachricht explizit senden oder das [**propsheet \_ enablewizbuttons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="bf7cb-107">You can send this message explicitly or use the [**PropSheet\_EnableWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bf7cb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf7cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf7cb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bf7cb-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf7cb-110">Einer oder mehrere der folgenden Werte, die angeben, welche Eigenschaften Blatt Schaltflächen aktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bf7cb-110">One or more of the following values that specify which property sheet buttons are to be enabled.</span></span> <span data-ttu-id="bf7cb-111">Wenn ein Schaltflächen Wert sowohl in diesem Parameter als auch in *LPARAM* enthalten ist, wird er aktiviert.</span><span class="sxs-lookup"><span data-stu-id="bf7cb-111">If a button value is included in both this parameter and *lParam*, it is enabled.</span></span>



| <span data-ttu-id="bf7cb-112">Wert</span><span class="sxs-lookup"><span data-stu-id="bf7cb-112">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="bf7cb-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="bf7cb-113">Meaning</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <span data-ttu-id="bf7cb-114"><dt>**pswizb \_ zurück**</dt></span><span class="sxs-lookup"><span data-stu-id="bf7cb-114"><dt>**PSWIZB\_BACK**</dt></span></span> </dl>                               | <span data-ttu-id="bf7cb-115">Die Schaltfläche " **zurück** ".</span><span class="sxs-lookup"><span data-stu-id="bf7cb-115">The **Back** button.</span></span><br/>   |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <span data-ttu-id="bf7cb-116"><dt>**pswizb- \_ Abbruch**</dt></span><span class="sxs-lookup"><span data-stu-id="bf7cb-116"><dt>**PSWIZB\_CANCEL**</dt></span></span> </dl>                         | <span data-ttu-id="bf7cb-117">Die Schaltfläche " **Abbrechen** ".</span><span class="sxs-lookup"><span data-stu-id="bf7cb-117">The **Cancel** button.</span></span><br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <span data-ttu-id="bf7cb-118"><dt>**pswizb \_ disabledfinish**</dt></span><span class="sxs-lookup"><span data-stu-id="bf7cb-118"><dt>**PSWIZB\_DISABLEDFINISH**</dt></span></span> </dl> | <span data-ttu-id="bf7cb-119">Die Schaltfläche **Fertig** stellen.</span><span class="sxs-lookup"><span data-stu-id="bf7cb-119">The **Finish** button.</span></span><br/> |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <span data-ttu-id="bf7cb-120"><dt>**pswizb- \_ Fertigstellen**</dt></span><span class="sxs-lookup"><span data-stu-id="bf7cb-120"><dt>**PSWIZB\_FINISH**</dt></span></span> </dl>                         | <span data-ttu-id="bf7cb-121">Die Schaltfläche **Fertig** stellen.</span><span class="sxs-lookup"><span data-stu-id="bf7cb-121">The **Finish** button.</span></span><br/> |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <span data-ttu-id="bf7cb-122"><dt>**pswizb \_ als nächstes**</dt></span><span class="sxs-lookup"><span data-stu-id="bf7cb-122"><dt>**PSWIZB\_NEXT**</dt></span></span> </dl>                               | <span data-ttu-id="bf7cb-123">Die Schaltfläche **weiter** .</span><span class="sxs-lookup"><span data-stu-id="bf7cb-123">The **Next** button.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="bf7cb-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bf7cb-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf7cb-125">Mindestens einer der in *wParam* verwendeten Werte, der angibt, welche Schaltflächen von diesem-Befehl betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="bf7cb-125">One or more of the same values used in *wParam*, specifying which buttons are affected by this call.</span></span> <span data-ttu-id="bf7cb-126">Wenn ein Schaltflächen Wert in diesem Parameter, aber nicht in *wParam* angezeigt wird, weist dies darauf hin, dass die Schaltfläche deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bf7cb-126">If a button value appears in this parameter but not in *wParam*, it indicates that the button should be disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf7cb-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bf7cb-127">Return value</span></span>

<span data-ttu-id="bf7cb-128">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="bf7cb-128">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf7cb-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bf7cb-129">Requirements</span></span>



| <span data-ttu-id="bf7cb-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bf7cb-130">Requirement</span></span> | <span data-ttu-id="bf7cb-131">Wert</span><span class="sxs-lookup"><span data-stu-id="bf7cb-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bf7cb-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bf7cb-132">Minimum supported client</span></span><br/> | <span data-ttu-id="bf7cb-133">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bf7cb-133">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bf7cb-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bf7cb-134">Minimum supported server</span></span><br/> | <span data-ttu-id="bf7cb-135">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bf7cb-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bf7cb-136">Header</span><span class="sxs-lookup"><span data-stu-id="bf7cb-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf7cb-137"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf7cb-137"><dt>Prsht.h</dt></span></span> </dl> |



 

 





