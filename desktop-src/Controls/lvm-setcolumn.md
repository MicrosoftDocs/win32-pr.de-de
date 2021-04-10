---
title: LVM_SETCOLUMN Meldung (kommstrg. h)
description: Legt die Attribute einer Listen Ansichts Spalte fest. Sie können diese Nachricht explizit oder mithilfe des ListView- \_ Makros SetColumn senden.
ms.assetid: 8ca1c269-fd86-4561-940d-b75f8ca2b731
keywords:
- Windows-Steuerelemente für LVM_SETCOLUMN Meldung
topic_type:
- apiref
api_name:
- LVM_SETCOLUMN
- LVM_SETCOLUMNW
- LVM_SETCOLUMNW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7251da70c7ac1e2cb7bbcf7b3e220a2f6cdf055f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956504"
---
# <a name="lvm_setcolumn-message"></a><span data-ttu-id="a277a-105">LVM- \_ SetColumn-Nachricht</span><span class="sxs-lookup"><span data-stu-id="a277a-105">LVM\_SETCOLUMN message</span></span>

<span data-ttu-id="a277a-106">Legt die Attribute einer Listen Ansichts Spalte fest.</span><span class="sxs-lookup"><span data-stu-id="a277a-106">Sets the attributes of a list-view column.</span></span> <span data-ttu-id="a277a-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView-Makros \_ SetColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumn) senden.</span><span class="sxs-lookup"><span data-stu-id="a277a-107">You can send this message explicitly or by using the [**ListView\_SetColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumn) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a277a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a277a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a277a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a277a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a277a-110">Der Index der Spalte.</span><span class="sxs-lookup"><span data-stu-id="a277a-110">Index of the column.</span></span>

</dd> <dt>

<span data-ttu-id="a277a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a277a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a277a-112">Zeiger auf eine [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) -Struktur, die die neuen Spalten Attribute enthält.</span><span class="sxs-lookup"><span data-stu-id="a277a-112">Pointer to an [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) structure that contains the new column attributes.</span></span> <span data-ttu-id="a277a-113">Der **Mask** -Member gibt an, welche Spalten Attribute festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a277a-113">The **mask** member specifies which column attributes to set.</span></span> <span data-ttu-id="a277a-114">Wenn das **Mask** -Element den "lvcf" \_ -Textwert angibt, ist das **pszText** -Element die Adresse einer auf NULL endenden Zeichenfolge, und der **cchtextmax** -Member wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a277a-114">If the **mask** member specifies the LVCF\_TEXT value, the **pszText** member is the address of a null-terminated string and the **cchTextMax** member is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a277a-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a277a-115">Return value</span></span>

<span data-ttu-id="a277a-116">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="a277a-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a277a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a277a-117">Requirements</span></span>



| <span data-ttu-id="a277a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a277a-118">Requirement</span></span> | <span data-ttu-id="a277a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a277a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a277a-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a277a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a277a-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a277a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a277a-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a277a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a277a-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a277a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a277a-124">Header</span><span class="sxs-lookup"><span data-stu-id="a277a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a277a-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a277a-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="a277a-126">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="a277a-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a277a-127">**LVM \_ Setcolumnw** (Unicode) und **LVM \_ setcolumnw** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a277a-127">**LVM\_SETCOLUMNW** (Unicode) and **LVM\_SETCOLUMNW** (ANSI)</span></span><br/>               |



 

 





