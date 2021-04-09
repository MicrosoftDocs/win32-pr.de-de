---
title: TCM_SETITEM Meldung (kommstrg. h)
description: Legt einige oder alle Attribute einer Registerkarte fest. Sie können diese Nachricht explizit oder mithilfe des tabctrl-Elements tabctrl senden \_ .
ms.assetid: 1d9c6607-d8ec-4644-a714-22bc2677aa78
keywords:
- Windows-Steuerelemente für TCM_SETITEM Meldung
topic_type:
- apiref
api_name:
- TCM_SETITEM
- TCM_SETITEMA
- TCM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee86cd0737c3c50c89a97d3881e2cdfd3850f481
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739888"
---
# <a name="tcm_setitem-message"></a><span data-ttu-id="a6cff-105">TCM-Element \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="a6cff-105">TCM\_SETITEM message</span></span>

<span data-ttu-id="a6cff-106">Legt einige oder alle Attribute einer Registerkarte fest.</span><span class="sxs-lookup"><span data-stu-id="a6cff-106">Sets some or all of a tab's attributes.</span></span> <span data-ttu-id="a6cff-107">Sie können diese Nachricht explizit oder mithilfe des [**tabctrl-Elements \_ tabctrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitem) senden.</span><span class="sxs-lookup"><span data-stu-id="a6cff-107">You can send this message explicitly or by using the [**TabCtrl\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a6cff-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6cff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6cff-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a6cff-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6cff-110">Der Index des Elements.</span><span class="sxs-lookup"><span data-stu-id="a6cff-110">Index of the item.</span></span>

</dd> <dt>

<span data-ttu-id="a6cff-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a6cff-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6cff-112">Zeiger auf eine [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) -Struktur, die die neuen Element Attribute enthält.</span><span class="sxs-lookup"><span data-stu-id="a6cff-112">Pointer to a [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure that contains the new item attributes.</span></span> <span data-ttu-id="a6cff-113">Der **Mask** -Member gibt an, welche Attribute festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a6cff-113">The **mask** member specifies which attributes to set.</span></span> <span data-ttu-id="a6cff-114">Wenn das **Mask** -Element den tcif \_ -Textwert angibt, ist das **pszText** -Element die Adresse einer auf NULL endenden Zeichenfolge, und der **cchtextmax** -Member wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a6cff-114">If the **mask** member specifies the TCIF\_TEXT value, the **pszText** member is the address of a null-terminated string and the **cchTextMax** member is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6cff-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6cff-115">Return value</span></span>

<span data-ttu-id="a6cff-116">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="a6cff-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6cff-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6cff-117">Requirements</span></span>



| <span data-ttu-id="a6cff-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6cff-118">Requirement</span></span> | <span data-ttu-id="a6cff-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a6cff-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a6cff-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a6cff-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a6cff-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6cff-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a6cff-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a6cff-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a6cff-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6cff-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a6cff-124">Header</span><span class="sxs-lookup"><span data-stu-id="a6cff-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6cff-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6cff-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="a6cff-126">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="a6cff-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a6cff-127">**TCM \_** "S" (Unicode) und " **TCM \_** " (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a6cff-127">**TCM\_SETITEMW** (Unicode) and **TCM\_SETITEMA** (ANSI)</span></span><br/>                   |



 

 





