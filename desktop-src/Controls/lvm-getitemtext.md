---
title: LVM_GETITEMTEXT Meldung (kommstrg. h)
description: Ruft den Text eines Listen Ansichts Elements oder unter Elements ab. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetItemText-Makros senden.
ms.assetid: 5711ed18-a766-4e7f-9e9d-b9203231b369
keywords:
- Windows-Steuerelemente für LVM_GETITEMTEXT Meldung
topic_type:
- apiref
api_name:
- LVM_GETITEMTEXT
- LVM_GETITEMTEXTA
- LVM_GETITEMTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c71eec6b9dab4c649b11da5b24568eea816774ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105501"
---
# <a name="lvm_getitemtext-message"></a><span data-ttu-id="eaa6f-105">LVM- \_ GetItemText-Nachricht</span><span class="sxs-lookup"><span data-stu-id="eaa6f-105">LVM\_GETITEMTEXT message</span></span>

<span data-ttu-id="eaa6f-106">Ruft den Text eines Listen Ansichts Elements oder unter Elements ab.</span><span class="sxs-lookup"><span data-stu-id="eaa6f-106">Retrieves the text of a list-view item or subitem.</span></span> <span data-ttu-id="eaa6f-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="eaa6f-107">You can send this message explicitly or by using the [**ListView\_GetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="eaa6f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="eaa6f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaa6f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eaa6f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eaa6f-110">Der Index des Listen Ansichts Elements.</span><span class="sxs-lookup"><span data-stu-id="eaa6f-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="eaa6f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eaa6f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eaa6f-112">Zeiger auf eine [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="eaa6f-112">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span> <span data-ttu-id="eaa6f-113">Um den Element Text abzurufen, legen Sie **iSubItem** auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="eaa6f-113">To retrieve the item text, set **iSubItem** to zero.</span></span> <span data-ttu-id="eaa6f-114">Um den Text eines unter Elements abzurufen, legen Sie **iSubItem** auf den Index des unter Elements fest.</span><span class="sxs-lookup"><span data-stu-id="eaa6f-114">To retrieve the text of a subitem, set **iSubItem** to the subitem's index.</span></span> <span data-ttu-id="eaa6f-115">Der **pszText** -Member verweist auf einen Puffer, der den Text empfängt.</span><span class="sxs-lookup"><span data-stu-id="eaa6f-115">The **pszText** member points to a buffer that receives the text.</span></span> <span data-ttu-id="eaa6f-116">Der **cchtextmax** -Member gibt die Anzahl der Zeichen im Puffer an.</span><span class="sxs-lookup"><span data-stu-id="eaa6f-116">The **cchTextMax** member specifies the number of characters in the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaa6f-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eaa6f-117">Return value</span></span>

<span data-ttu-id="eaa6f-118">Wenn Sie diese Meldung explizit senden, wird die Anzahl der Zeichen im **pszText** -Member der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="eaa6f-118">If you send this message explicitly, it returns the number of characters in the **pszText** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="eaa6f-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eaa6f-119">Remarks</span></span>

<span data-ttu-id="eaa6f-120">Sie können diese Nachricht auch senden, indem Sie das [**ListView \_ GetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) -Makro aufrufen.</span><span class="sxs-lookup"><span data-stu-id="eaa6f-120">You can also send this message by calling the [**ListView\_GetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) macro.</span></span> <span data-ttu-id="eaa6f-121">Dieses Makro gibt jedoch nicht die Länge der Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="eaa6f-121">However, this macro does not return the string length.</span></span>

<span data-ttu-id="eaa6f-122">**LVM \_ GetItemText** wird unter dem [**LVS-Besitzer \_ Daten**](list-view-window-styles.md) Stil nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eaa6f-122">**LVM\_GETITEMTEXT** is not supported under the [**LVS\_OWNERDATA**](list-view-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaa6f-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eaa6f-123">Requirements</span></span>



| <span data-ttu-id="eaa6f-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eaa6f-124">Requirement</span></span> | <span data-ttu-id="eaa6f-125">Wert</span><span class="sxs-lookup"><span data-stu-id="eaa6f-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eaa6f-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eaa6f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="eaa6f-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eaa6f-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eaa6f-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eaa6f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="eaa6f-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eaa6f-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eaa6f-130">Header</span><span class="sxs-lookup"><span data-stu-id="eaa6f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="eaa6f-131"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="eaa6f-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="eaa6f-132">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="eaa6f-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="eaa6f-133">**LVM \_ Getitemtextw** (Unicode) und **LVM \_ getitemtexta** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="eaa6f-133">**LVM\_GETITEMTEXTW** (Unicode) and **LVM\_GETITEMTEXTA** (ANSI)</span></span><br/>           |



 

 





