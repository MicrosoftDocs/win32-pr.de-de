---
title: TCM_INSERTITEM Meldung (kommstrg. h)
description: Fügt eine neue Registerkarte in ein Registerkarten-Steuerelement ein. Sie können diese Nachricht explizit oder mithilfe des tabctrl \_ InsertItem-Makros senden.
ms.assetid: e547c49a-699c-4137-8680-20391d138d54
keywords:
- Windows-Steuerelemente für TCM_INSERTITEM Meldung
topic_type:
- apiref
api_name:
- TCM_INSERTITEM
- TCM_INSERTITEMA
- TCM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58002006944a221571e37c37d25259d0aaa74fc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343873"
---
# <a name="tcm_insertitem-message"></a><span data-ttu-id="e2cc2-105">TCM \_ InsertItem-Nachricht</span><span class="sxs-lookup"><span data-stu-id="e2cc2-105">TCM\_INSERTITEM message</span></span>

<span data-ttu-id="e2cc2-106">Fügt eine neue Registerkarte in ein Registerkarten-Steuerelement ein.</span><span class="sxs-lookup"><span data-stu-id="e2cc2-106">Inserts a new tab in a tab control.</span></span> <span data-ttu-id="e2cc2-107">Sie können diese Nachricht explizit oder mithilfe des [**tabctrl \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_insertitem) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="e2cc2-107">You can send this message explicitly or by using the [**TabCtrl\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_insertitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e2cc2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2cc2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2cc2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e2cc2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2cc2-110">Index der neuen Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="e2cc2-110">Index of the new tab.</span></span>

</dd> <dt>

<span data-ttu-id="e2cc2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2cc2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2cc2-112">Ein Zeiger auf eine [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) -Struktur, die die Attribute der Registerkarte angibt. Die Member **dwstate** und **dwstatemask** dieser Struktur werden von dieser Nachricht ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e2cc2-112">Pointer to a [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure that specifies the attributes of the tab. The **dwState** and **dwStateMask** members of this structure are ignored by this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2cc2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2cc2-113">Return value</span></span>

<span data-ttu-id="e2cc2-114">Gibt den Index der neuen Registerkarte zurück, wenn erfolgreich, andernfalls-1.</span><span class="sxs-lookup"><span data-stu-id="e2cc2-114">Returns the index of the new tab if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2cc2-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2cc2-115">Requirements</span></span>



| <span data-ttu-id="e2cc2-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2cc2-116">Requirement</span></span> | <span data-ttu-id="e2cc2-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e2cc2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2cc2-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e2cc2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e2cc2-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2cc2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e2cc2-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e2cc2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e2cc2-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2cc2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e2cc2-122">Header</span><span class="sxs-lookup"><span data-stu-id="e2cc2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2cc2-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2cc2-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="e2cc2-124">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="e2cc2-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e2cc2-125">**TCM \_ Insertitemw** (Unicode) und **TCM \_ insertitema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e2cc2-125">**TCM\_INSERTITEMW** (Unicode) and **TCM\_INSERTITEMA** (ANSI)</span></span><br/>             |



 

 





