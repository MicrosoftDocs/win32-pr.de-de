---
title: EM_GETUNDONAME Meldung (RichEdit. h)
description: Microsoft Rich Edit 2,0 und höher ruft ggf. den Typ der nächsten Rückgängig-Aktion ab. Microsoft Rich Edit 1,0 diese Meldung wird nicht unterstützt.
ms.assetid: 43351909-f8bc-425a-9d9b-655e3b47eb75
keywords:
- Windows-Steuerelemente für EM_GETUNDONAME Meldung
topic_type:
- apiref
api_name:
- EM_GETUNDONAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c29b5815da5569059ba80c007d6af39d1e389f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956900"
---
# <a name="em_getundoname-message"></a><span data-ttu-id="f653d-104">EM \_ getundoname-Meldung</span><span class="sxs-lookup"><span data-stu-id="f653d-104">EM\_GETUNDONAME message</span></span>

<span data-ttu-id="f653d-105">Microsoft Rich Edit 2,0 und höher: Ruft den Typ der nächsten Rückgängig-Aktion ab, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f653d-105">Microsoft Rich Edit 2.0 and later: Retrieves the type of the next undo action, if any.</span></span>

<span data-ttu-id="f653d-106">Microsoft Rich Edit 1,0: Diese Meldung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f653d-106">Microsoft Rich Edit 1.0: This message is not supported.</span></span>

## <a name="parameters"></a><span data-ttu-id="f653d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f653d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f653d-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f653d-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f653d-109">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="f653d-109">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f653d-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f653d-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f653d-111">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="f653d-111">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f653d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f653d-112">Return value</span></span>

<span data-ttu-id="f653d-113">Wenn eine Rückgängig-Aktion vorliegt, ist der zurückgegebene Wert ein [**undonameid**](/windows/desktop/api/Richedit/ne-richedit-undonameid) -Enumerationswert, der den Typ der nächsten Aktion in der Rückgängig-Warteschlange des Steuer Elements angibt.</span><span class="sxs-lookup"><span data-stu-id="f653d-113">If there is an undo action, the value returned is an [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) enumeration value that indicates the type of the next action in the control's undo queue.</span></span>

<span data-ttu-id="f653d-114">Wenn keine Aktionen vorhanden sind, die rückgängig gemacht werden können, oder der Typ der nächsten Rückgängig-Aktion unbekannt ist, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f653d-114">If there are no actions that can be undone or the type of the next undo action is unknown, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f653d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f653d-115">Remarks</span></span>

<span data-ttu-id="f653d-116">Die Typen von Aktionen, die rückgängig gemacht oder wiederholt werden können, sind das eingeben, löschen, ziehen, ablegen, Ausschneiden und einfügen.</span><span class="sxs-lookup"><span data-stu-id="f653d-116">The types of actions that can be undone or redone include typing, delete, drag, drop, cut, and paste operations.</span></span> <span data-ttu-id="f653d-117">Diese Informationen können für Anwendungen nützlich sein, die eine erweiterte Benutzeroberfläche für Rückgängigvorgänge und Wiederholungs Vorgänge bereitstellen, z. b. ein Dropdown-Listenfeld mit Aktionen, die rückgängig gemacht werden können.</span><span class="sxs-lookup"><span data-stu-id="f653d-117">This information can be useful for applications that provide an extended user interface for undo and redo operations, such as a drop-down list box of actions that can be undone.</span></span>

## <a name="requirements"></a><span data-ttu-id="f653d-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f653d-118">Requirements</span></span>



| <span data-ttu-id="f653d-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f653d-119">Requirement</span></span> | <span data-ttu-id="f653d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f653d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f653d-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f653d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f653d-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f653d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f653d-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f653d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f653d-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f653d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f653d-125">Header</span><span class="sxs-lookup"><span data-stu-id="f653d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f653d-126"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f653d-126"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f653d-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f653d-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="f653d-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="f653d-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f653d-129">**EM \_ getredoname**</span><span class="sxs-lookup"><span data-stu-id="f653d-129">**EM\_GETREDONAME**</span></span>](em-getredoname.md)
</dt> <dt>

[<span data-ttu-id="f653d-130">**EM- \_ Wiederholung**</span><span class="sxs-lookup"><span data-stu-id="f653d-130">**EM\_REDO**</span></span>](em-redo.md)
</dt> <dt>

[<span data-ttu-id="f653d-131">**EM \_ rückgängig machen**</span><span class="sxs-lookup"><span data-stu-id="f653d-131">**EM\_UNDO**</span></span>](em-undo.md)
</dt> <dt>

[<span data-ttu-id="f653d-132">**Undonameid**</span><span class="sxs-lookup"><span data-stu-id="f653d-132">**UNDONAMEID**</span></span>](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 





