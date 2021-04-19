---
title: CBEM_GETITEM Meldung (kommstrg. h)
description: Ruft Element Informationen für ein bestimmtes ComboBoxEx-Element ab.
ms.assetid: 2df07ae8-fa84-487c-a4a7-90244dfdb40e
keywords:
- Windows-Steuerelemente für CBEM_GETITEM Meldung
topic_type:
- apiref
api_name:
- CBEM_GETITEM
- CBEM_GETITEMA
- CBEM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 940bbf7aea8ec93dd0f808937d959477c964df96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342870"
---
# <a name="cbem_getitem-message"></a><span data-ttu-id="c92a6-104">CBEM \_ GetItem-Meldung</span><span class="sxs-lookup"><span data-stu-id="c92a6-104">CBEM\_GETITEM message</span></span>

<span data-ttu-id="c92a6-105">Ruft Element Informationen für ein bestimmtes ComboBoxEx-Element ab.</span><span class="sxs-lookup"><span data-stu-id="c92a6-105">Gets item information for a given ComboBoxEx item.</span></span>

## <a name="parameters"></a><span data-ttu-id="c92a6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c92a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c92a6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c92a6-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c92a6-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="c92a6-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c92a6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c92a6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c92a6-110">Ein Zeiger auf eine [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) -Struktur, die die Element Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="c92a6-110">A pointer to a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure that receives the item information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c92a6-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c92a6-111">Return value</span></span>

<span data-ttu-id="c92a6-112">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="c92a6-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c92a6-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c92a6-113">Remarks</span></span>

<span data-ttu-id="c92a6-114">Wenn die Nachricht gesendet wird, müssen die Member **iItem** und **Mask** der Struktur festgelegt werden, um den Index des Ziel Elements und den Typ der abzurufenden Informationen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c92a6-114">When the message is sent, the **iItem** and **mask** members of the structure must be set to indicate the index of the target item and the type of information to be retrieved.</span></span> <span data-ttu-id="c92a6-115">Andere Mitglieder werden nach Bedarf festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c92a6-115">Other members are set as needed.</span></span> <span data-ttu-id="c92a6-116">Zum Abrufen von Text müssen Sie z. b. das cbeif \_ -textflag in **Mask** festlegen und **cchtextmax** einen Wert zuweisen.</span><span class="sxs-lookup"><span data-stu-id="c92a6-116">For example, to retrieve text, you must set the CBEIF\_TEXT flag in **mask**, and assign a value to **cchTextMax**.</span></span> <span data-ttu-id="c92a6-117">Wenn Sie den **iItem** -Member auf-1 festlegen, wird das im Bearbeitungs Steuerelement angezeigte Element abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c92a6-117">Setting the **iItem** member to -1 will retrieve the item displayed in the edit control.</span></span>

<span data-ttu-id="c92a6-118">Wenn das cbeif- \_ textflag im **Mask** -Member der [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) -Struktur festgelegt ist, kann das Steuerelement den **pszText** -Member der Struktur so ändern, dass er auf den neuen Text verweist, anstatt den Puffer mit dem angeforderten Text zu füllen.</span><span class="sxs-lookup"><span data-stu-id="c92a6-118">If the CBEIF\_TEXT flag is set in the **mask** member of the [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure, the control may change the **pszText** member of the structure to point to the new text instead of filling the buffer with the requested text.</span></span> <span data-ttu-id="c92a6-119">Anwendungen sollten nicht davon ausgehen, dass der Text immer in den angeforderten Puffer eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="c92a6-119">Applications should not assume that the text will always be placed in the requested buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="c92a6-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c92a6-120">Requirements</span></span>



| <span data-ttu-id="c92a6-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c92a6-121">Requirement</span></span> | <span data-ttu-id="c92a6-122">Wert</span><span class="sxs-lookup"><span data-stu-id="c92a6-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c92a6-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c92a6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c92a6-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c92a6-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c92a6-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c92a6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c92a6-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c92a6-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c92a6-127">Header</span><span class="sxs-lookup"><span data-stu-id="c92a6-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c92a6-128"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c92a6-128"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="c92a6-129">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="c92a6-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c92a6-130">**CBEM \_ Getitemw** (Unicode) und **CBEM \_ getitema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c92a6-130">**CBEM\_GETITEMW** (Unicode) and **CBEM\_GETITEMA** (ANSI)</span></span><br/>                 |



 

 





