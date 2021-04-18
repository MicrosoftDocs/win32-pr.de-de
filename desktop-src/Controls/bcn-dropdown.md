---
title: BCN_DROPDOWN Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn der Benutzer auf einen Dropdown Pfeil auf einer Schaltfläche klickt. Das übergeordnete Fenster des Steuer Elements empfängt diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung.
ms.assetid: 61503b8d-193e-4855-b9eb-35c0dc636c02
keywords:
- Windows-Steuerelemente für BCN_DROPDOWN Benachrichtigungs
topic_type:
- apiref
api_name:
- BCN_DROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e78512419f62beaa82aff42ccaf951d34130fe3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338137"
---
# <a name="bcn_dropdown-notification-code"></a><span data-ttu-id="53988-105">BCN- \_ Dropdown-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="53988-105">BCN\_DROPDOWN notification code</span></span>

<span data-ttu-id="53988-106">Wird gesendet, wenn der Benutzer auf einen Dropdown Pfeil auf einer Schaltfläche klickt.</span><span class="sxs-lookup"><span data-stu-id="53988-106">Sent when the user clicks a drop down arrow on a button.</span></span> <span data-ttu-id="53988-107">Das übergeordnete Fenster des Steuer Elements empfängt diesen Benachrichtigungs Code in Form einer [**WM \_**](wm-notify.md) -Benachrichtigungs Meldung.</span><span class="sxs-lookup"><span data-stu-id="53988-107">The parent window of the control receives this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
BCN_DROPDOWN
        
    pnmdropdown = (NMBCDROPDOWN*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="53988-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="53988-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53988-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53988-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53988-110">Ein Zeiger auf eine [**nmbcdropdown**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="53988-110">A pointer to a [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) structure.</span></span> <span data-ttu-id="53988-111">Der **rcbutton** -Member wird so festgelegt, dass der Dropdown Bereich beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="53988-111">The **rcButton** member is set to describe the drop-down area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53988-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="53988-112">Return value</span></span>

<span data-ttu-id="53988-113">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="53988-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="53988-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53988-114">Remarks</span></span>

<span data-ttu-id="53988-115">Der Benachrichtigungs Empfänger wandelt **LPARAM** ein, um die [**nmbcdropdown**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) -Struktur abzurufen.</span><span class="sxs-lookup"><span data-stu-id="53988-115">The notification receiver casts **LPARAM** to retrieve the [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) structure.</span></span> <span data-ttu-id="53988-116">**WParam** enthält die ID des Steuer Elements, das diese Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="53988-116">**WPARAM** contains the ID of the control that sends this message.</span></span> <span data-ttu-id="53988-117">Das Schaltflächen-Steuerelement muss einen Dropdown-Schaltflächen Stil aufweisen.</span><span class="sxs-lookup"><span data-stu-id="53988-117">The button control must have a drop-down button style.</span></span>

## <a name="requirements"></a><span data-ttu-id="53988-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53988-118">Requirements</span></span>



| <span data-ttu-id="53988-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53988-119">Requirement</span></span> | <span data-ttu-id="53988-120">Wert</span><span class="sxs-lookup"><span data-stu-id="53988-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53988-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="53988-121">Minimum supported client</span></span><br/> | <span data-ttu-id="53988-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53988-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="53988-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="53988-123">Minimum supported server</span></span><br/> | <span data-ttu-id="53988-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53988-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="53988-125">Header</span><span class="sxs-lookup"><span data-stu-id="53988-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="53988-126"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="53988-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





