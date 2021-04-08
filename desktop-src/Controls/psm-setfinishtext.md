---
title: PSM_SETFINISHTEXT Meldung (prsht. h)
description: Legt den Text der Schaltfläche Fertigstellen in einem Assistenten fest, zeigt die Schaltfläche an und aktiviert Sie und blendet die Schaltflächen weiter und zurück aus. Sie können diese Nachricht explizit oder mithilfe des propsheet- \_ Makros setfinishtext senden.
ms.assetid: fa89c6d7-9ab7-4e7c-ba08-d665420492a3
keywords:
- Windows-Steuerelemente für PSM_SETFINISHTEXT Meldung
topic_type:
- apiref
api_name:
- PSM_SETFINISHTEXT
- PSM_SETFINISHTEXTA
- PSM_SETFINISHTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08195cddc96c8b92f403be6940f31099e21151f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740097"
---
# <a name="psm_setfinishtext-message"></a><span data-ttu-id="f0510-105">PSM \_ setfinishtext-Nachricht</span><span class="sxs-lookup"><span data-stu-id="f0510-105">PSM\_SETFINISHTEXT message</span></span>

<span data-ttu-id="f0510-106">Legt den Text der Schaltfläche **Fertig** stellen in einem Assistenten fest, zeigt die Schaltfläche an und aktiviert Sie und blendet die Schaltflächen **weiter** und **zurück** aus.</span><span class="sxs-lookup"><span data-stu-id="f0510-106">Sets the text of the **Finish** button in a wizard, shows and enables the button, and hides the **Next** and **Back** buttons.</span></span> <span data-ttu-id="f0510-107">Sie können diese Nachricht explizit oder mithilfe des [**propsheet-Makros \_ setfinishtext**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext) senden.</span><span class="sxs-lookup"><span data-stu-id="f0510-107">You can send this message explicitly or by using the [**PropSheet\_SetFinishText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f0510-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0510-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0510-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f0510-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0510-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="f0510-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f0510-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f0510-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0510-112">Zeiger auf den neuen Text für die Schaltfläche **Fertig** stellen.</span><span class="sxs-lookup"><span data-stu-id="f0510-112">Pointer to the new text for the **Finish** button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0510-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0510-113">Return value</span></span>

<span data-ttu-id="f0510-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="f0510-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0510-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f0510-115">Remarks</span></span>

<span data-ttu-id="f0510-116">Standardmäßig verfügt die Schaltfläche **Fertig** stellen nicht über eine Tastatur Beschleunigung.</span><span class="sxs-lookup"><span data-stu-id="f0510-116">By default, the **Finish** button does not have a keyboard accelerator.</span></span> <span data-ttu-id="f0510-117">Sie können eine Zugriffstaste mit dieser Meldung erstellen, indem Sie in die Text Zeichenfolge, die Sie *LPARAM* zuweisen, ein kaufmännisches und-Zeichen (&) einschließen.</span><span class="sxs-lookup"><span data-stu-id="f0510-117">You can create a keyboard accelerator with this message by including an ampersand (&) in the text string that you assign to *lParam*.</span></span> <span data-ttu-id="f0510-118">Beispielsweise definiert "&Finish" F als Zugriffstaste.</span><span class="sxs-lookup"><span data-stu-id="f0510-118">For example, "&Finish" defines F as the accelerator key.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0510-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0510-119">Requirements</span></span>



| <span data-ttu-id="f0510-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0510-120">Requirement</span></span> | <span data-ttu-id="f0510-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f0510-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f0510-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f0510-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f0510-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0510-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f0510-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f0510-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f0510-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0510-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f0510-126">Header</span><span class="sxs-lookup"><span data-stu-id="f0510-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0510-127"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0510-127"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="f0510-128">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="f0510-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f0510-129">**PSM \_ Setfinishtextw** (Unicode) und **PSM \_ setfinishtexta** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f0510-129">**PSM\_SETFINISHTEXTW** (Unicode) and **PSM\_SETFINISHTEXTA** (ANSI)</span></span><br/>    |



 

 





