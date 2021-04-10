---
title: EM_GETREDONAME Meldung (RichEdit. h)
description: Ruft den Typ der nächsten Aktion (sofern vorhanden) in der Wiederholungs Warteschlange des Rich-Edit-Steuer Elements ab.
ms.assetid: 8649236f-32dc-45d3-847e-c9f65ffba44c
keywords:
- Windows-Steuerelemente für EM_GETREDONAME Meldung
topic_type:
- apiref
api_name:
- EM_GETREDONAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ea44257344b9ebdb8ffe91ad97e939aae0db9b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956580"
---
# <a name="em_getredoname-message"></a><span data-ttu-id="63c72-104">EM \_ getredoname-Meldung</span><span class="sxs-lookup"><span data-stu-id="63c72-104">EM\_GETREDONAME message</span></span>

<span data-ttu-id="63c72-105">Ruft den Typ der nächsten Aktion (sofern vorhanden) in der Wiederholungs Warteschlange des Rich-Edit-Steuer Elements ab.</span><span class="sxs-lookup"><span data-stu-id="63c72-105">Retrieves the type of the next action, if any, in the rich edit control's redo queue.</span></span>

## <a name="parameters"></a><span data-ttu-id="63c72-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="63c72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63c72-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="63c72-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63c72-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="63c72-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="63c72-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="63c72-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63c72-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="63c72-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63c72-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="63c72-111">Return value</span></span>

<span data-ttu-id="63c72-112">Wenn die Wiederholungs Warteschlange für das Steuerelement nicht leer ist, ist der zurückgegebene Wert ein [**undonameid**](/windows/desktop/api/Richedit/ne-richedit-undonameid) -Enumerationswert, der den Typ der nächsten Aktion in der Wiederholungs Warteschlange des Steuer Elements angibt.</span><span class="sxs-lookup"><span data-stu-id="63c72-112">If the redo queue for the control is not empty, the value returned is an [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) enumeration value that indicates the type of the next action in the control's redo queue.</span></span>

<span data-ttu-id="63c72-113">Wenn keine Redoable-Aktionen vorhanden sind oder der Typ der nächsten Redoable-Aktion unbekannt ist, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="63c72-113">If there are no redoable actions or the type of the next redoable action is unknown, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="63c72-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="63c72-114">Remarks</span></span>

<span data-ttu-id="63c72-115">Die Typen von Aktionen, die rückgängig gemacht oder wiederholt werden können, sind das eingeben, löschen, Drag-Drop-, Ausschneide-und Einfügevorgänge.</span><span class="sxs-lookup"><span data-stu-id="63c72-115">The types of actions that can be undone or redone include typing, delete, drag-drop, cut, and paste operations.</span></span> <span data-ttu-id="63c72-116">Diese Informationen können für Anwendungen nützlich sein, die eine erweiterte Benutzeroberfläche für Rückgängigvorgänge und Wiederholungs Vorgänge bereitstellen, z. b. ein Dropdown-Listenfeld mit Redoable-Aktionen.</span><span class="sxs-lookup"><span data-stu-id="63c72-116">This information can be useful for applications that provide an extended user interface for undo and redo operations, such as a drop-down list box of redoable actions.</span></span>

## <a name="requirements"></a><span data-ttu-id="63c72-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63c72-117">Requirements</span></span>



| <span data-ttu-id="63c72-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63c72-118">Requirement</span></span> | <span data-ttu-id="63c72-119">Wert</span><span class="sxs-lookup"><span data-stu-id="63c72-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="63c72-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="63c72-120">Minimum supported client</span></span><br/> | <span data-ttu-id="63c72-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="63c72-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="63c72-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="63c72-122">Minimum supported server</span></span><br/> | <span data-ttu-id="63c72-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="63c72-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="63c72-124">Header</span><span class="sxs-lookup"><span data-stu-id="63c72-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="63c72-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="63c72-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63c72-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63c72-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="63c72-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="63c72-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="63c72-128">**EM \_ getundoname**</span><span class="sxs-lookup"><span data-stu-id="63c72-128">**EM\_GETUNDONAME**</span></span>](em-getundoname.md)
</dt> <dt>

[<span data-ttu-id="63c72-129">**EM- \_ Wiederholung**</span><span class="sxs-lookup"><span data-stu-id="63c72-129">**EM\_REDO**</span></span>](em-redo.md)
</dt> <dt>

[<span data-ttu-id="63c72-130">**EM \_ rückgängig machen**</span><span class="sxs-lookup"><span data-stu-id="63c72-130">**EM\_UNDO**</span></span>](em-undo.md)
</dt> <dt>

[<span data-ttu-id="63c72-131">**Undonameid**</span><span class="sxs-lookup"><span data-stu-id="63c72-131">**UNDONAMEID**</span></span>](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 





