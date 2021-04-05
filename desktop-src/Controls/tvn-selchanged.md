---
title: TVN_SELCHANGED Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass sich die Auswahl von einem Element in ein anderes geändert hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 682170d3-5843-4d92-afeb-c37f3502ed5d
keywords:
- Windows-Steuerelemente für TVN_SELCHANGED Benachrichtigungs
topic_type:
- apiref
api_name:
- TVN_SELCHANGED
- TVN_SELCHANGEDA
- TVN_SELCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a564ec039e179d03dda9edc19d6de3412cd5361a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859231"
---
# <a name="tvn_selchanged-notification-code"></a><span data-ttu-id="5314b-105">Geänderter TVN- \_ Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="5314b-105">TVN\_SELCHANGED notification code</span></span>

<span data-ttu-id="5314b-106">Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass sich die Auswahl von einem Element in ein anderes geändert hat.</span><span class="sxs-lookup"><span data-stu-id="5314b-106">Notifies a tree-view control's parent window that the selection has changed from one item to another.</span></span> <span data-ttu-id="5314b-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="5314b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_SELCHANGED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="5314b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5314b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5314b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5314b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5314b-110">Zeiger auf eine [**nmtreeview**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="5314b-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="5314b-111">Die **itemold** -und **itemnew** -Member der **nmtreeview** -Struktur sind [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Strukturen, die Informationen über das zuvor ausgewählte Element und das neu ausgewählte Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="5314b-111">The **itemOld** and **itemNew** members of the **NMTREEVIEW** structure are [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structures that contain information about the previously selected item and the newly selected item.</span></span> <span data-ttu-id="5314b-112">Nur die Member " **Mask**", " **Hitem**", " **State**" und " **LPARAM** " sind gültig.</span><span class="sxs-lookup"><span data-stu-id="5314b-112">Only the **mask**, **hItem**, **state**, and **lParam** members of these structures are valid.</span></span> <span data-ttu-id="5314b-113">Die " **Status Ask** "-Member der **tvitem** -Strukturen, die von **itemold** und **itemnew** angegeben werden, sind bei der Eingabe nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="5314b-113">The **stateMask** members of the **TVITEM** structures specified by **itemOld** and **itemNew** are undefined on input.</span></span> <span data-ttu-id="5314b-114">Der **Action** -Member der **nmtreeview** -Struktur gibt den Typ der Aktion an, die bewirkt hat, dass die Auswahl geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="5314b-114">The **action** member of the **NMTREEVIEW** structure indicates the type of action that caused the selection to change.</span></span> <span data-ttu-id="5314b-115">Es kann sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="5314b-115">It can be one of the following values:</span></span>



| <span data-ttu-id="5314b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5314b-116">Requirement</span></span> | <span data-ttu-id="5314b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="5314b-117">Value</span></span> |
|-----------------|-------------------|
| <span data-ttu-id="5314b-118">TVC- \_ bykeyboard</span><span class="sxs-lookup"><span data-stu-id="5314b-118">TVC\_BYKEYBOARD</span></span> | <span data-ttu-id="5314b-119">Per Tastatureingabe.</span><span class="sxs-lookup"><span data-stu-id="5314b-119">By a keystroke.</span></span>   |
| <span data-ttu-id="5314b-120">TVC- \_ bymouse</span><span class="sxs-lookup"><span data-stu-id="5314b-120">TVC\_BYMOUSE</span></span>    | <span data-ttu-id="5314b-121">Per Mausklick.</span><span class="sxs-lookup"><span data-stu-id="5314b-121">By a mouse click.</span></span> |
| <span data-ttu-id="5314b-122">TVC \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="5314b-122">TVC\_UNKNOWN</span></span>    | <span data-ttu-id="5314b-123">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="5314b-123">Unknown.</span></span>          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5314b-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5314b-124">Return value</span></span>

<span data-ttu-id="5314b-125">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5314b-125">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="5314b-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5314b-126">Requirements</span></span>



| <span data-ttu-id="5314b-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5314b-127">Requirement</span></span> | <span data-ttu-id="5314b-128">Wert</span><span class="sxs-lookup"><span data-stu-id="5314b-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5314b-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5314b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5314b-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5314b-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5314b-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5314b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5314b-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5314b-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5314b-133">Header</span><span class="sxs-lookup"><span data-stu-id="5314b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="5314b-134"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="5314b-134"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="5314b-135">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="5314b-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5314b-136">**TVN \_ Selchangedw** (Unicode) und **TVN \_ selchangeda** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5314b-136">**TVN\_SELCHANGEDW** (Unicode) and **TVN\_SELCHANGEDA** (ANSI)</span></span><br/>             |



 

 





