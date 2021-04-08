---
title: EM_HIDESELECTION Meldung (RichEdit. h)
description: In der EM \_ HideSelection-Meldung wird die Auswahl in einem Rich-Edit-Steuerelement ausgeblendet oder angezeigt.
ms.assetid: 1245618f-c9e6-4876-9133-6009370cdb97
keywords:
- Windows-Steuerelemente für EM_HIDESELECTION Meldung
topic_type:
- apiref
api_name:
- EM_HIDESELECTION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a5690e52c2a25f5a359de205ac1584e1ef45ed4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949490"
---
# <a name="em_hideselection-message"></a><span data-ttu-id="06c2e-104">EM \_ HideSelection-Meldung</span><span class="sxs-lookup"><span data-stu-id="06c2e-104">EM\_HIDESELECTION message</span></span>

<span data-ttu-id="06c2e-105">In der **EM \_ HideSelection** -Meldung wird die Auswahl in einem Rich-Edit-Steuerelement ausgeblendet oder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="06c2e-105">The **EM\_HIDESELECTION** message hides or shows the selection in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="06c2e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="06c2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06c2e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="06c2e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06c2e-108">Ein Wert, der angibt, ob die Auswahl ausgeblendet oder angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="06c2e-108">Value specifying whether to hide or show the selection.</span></span> <span data-ttu-id="06c2e-109">Wenn dieser Parameter 0 (null) ist, wird die Auswahl angezeigt.</span><span class="sxs-lookup"><span data-stu-id="06c2e-109">If this parameter is zero, the selection is shown.</span></span> <span data-ttu-id="06c2e-110">Andernfalls wird die Auswahl ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="06c2e-110">Otherwise, the selection is hidden.</span></span>

</dd> <dt>

<span data-ttu-id="06c2e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="06c2e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06c2e-112">Dieser Parameter wird nicht verwendet. Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="06c2e-112">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06c2e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="06c2e-113">Return value</span></span>

<span data-ttu-id="06c2e-114">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="06c2e-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="06c2e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06c2e-115">Requirements</span></span>



| <span data-ttu-id="06c2e-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06c2e-116">Requirement</span></span> | <span data-ttu-id="06c2e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="06c2e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06c2e-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="06c2e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="06c2e-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06c2e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="06c2e-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="06c2e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="06c2e-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06c2e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="06c2e-122">Header</span><span class="sxs-lookup"><span data-stu-id="06c2e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="06c2e-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="06c2e-123"><dt>Richedit.h</dt></span></span> </dl> |



 

 





