---
title: EM_STOPGROUPTYPING Meldung (RichEdit. h)
description: Beendet ein Rich-Edit-Steuerelement, das zusätzliche Typisierungsaktionen in der aktuellen Rückgängig-Aktion sammelt. Das Steuerelement speichert die nächste Typisierungsaktion, sofern vorhanden, in eine neue Aktion in der Rückgängig-Warteschlange.
ms.assetid: 3059826f-84d1-4b7b-b4a8-da17d5f41013
keywords:
- Windows-Steuerelemente für EM_STOPGROUPTYPING Meldung
topic_type:
- apiref
api_name:
- EM_STOPGROUPTYPING
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eced7ff12526296552e4adcc38c927ae94ee0502
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741233"
---
# <a name="em_stopgrouptyping-message"></a><span data-ttu-id="b6e02-105">EM \_ stopgrouptypismeldungs</span><span class="sxs-lookup"><span data-stu-id="b6e02-105">EM\_STOPGROUPTYPING message</span></span>

<span data-ttu-id="b6e02-106">Beendet ein Rich-Edit-Steuerelement, das zusätzliche Typisierungsaktionen in der aktuellen Rückgängig-Aktion sammelt.</span><span class="sxs-lookup"><span data-stu-id="b6e02-106">Stops a rich edit control from collecting additional typing actions into the current undo action.</span></span> <span data-ttu-id="b6e02-107">Das Steuerelement speichert die nächste Typisierungsaktion, sofern vorhanden, in eine neue Aktion in der Rückgängig-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="b6e02-107">The control stores the next typing action, if any, into a new action in the undo queue.</span></span>

## <a name="parameters"></a><span data-ttu-id="b6e02-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6e02-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6e02-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b6e02-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6e02-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="b6e02-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b6e02-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6e02-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6e02-112">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="b6e02-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6e02-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b6e02-113">Return value</span></span>

<span data-ttu-id="b6e02-114">Der Rückgabewert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="b6e02-114">The return value is zero.</span></span> <span data-ttu-id="b6e02-115">Diese Meldung kann nicht fehlerhaft sein.</span><span class="sxs-lookup"><span data-stu-id="b6e02-115">This message cannot fail.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6e02-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6e02-116">Remarks</span></span>

<span data-ttu-id="b6e02-117">Ein Rich Edit-Steuerelement gruppiert aufeinander folgende Typisierungsaktionen, einschließlich Zeichen, die mithilfe des **Backspace** -Schlüssels gelöscht wurden, in eine einzelne Rückgängig-Aktion, bis eines der folgenden Ereignisse eintritt:</span><span class="sxs-lookup"><span data-stu-id="b6e02-117">A rich edit control groups consecutive typing actions, including characters deleted by using the **BackSpace** key, into a single undo action until one of the following events occurs:</span></span>

-   <span data-ttu-id="b6e02-118">Das-Steuerelement empfängt eine **EM \_ stopgrouptypisnachricht** .</span><span class="sxs-lookup"><span data-stu-id="b6e02-118">The control receives an **EM\_STOPGROUPTYPING** message.</span></span>
-   <span data-ttu-id="b6e02-119">Das Steuerelement verliert den Fokus.</span><span class="sxs-lookup"><span data-stu-id="b6e02-119">The control loses focus.</span></span>
-   <span data-ttu-id="b6e02-120">Der Benutzer verschiebt die aktuelle Auswahl entweder mithilfe der Pfeiltasten oder durch Klicken auf die Maus.</span><span class="sxs-lookup"><span data-stu-id="b6e02-120">The user moves the current selection, either by using the arrow keys or by clicking the mouse.</span></span>
-   <span data-ttu-id="b6e02-121">Der Benutzer drückt die ENTF **-Taste.**</span><span class="sxs-lookup"><span data-stu-id="b6e02-121">The user presses the **Delete** key.</span></span>
-   <span data-ttu-id="b6e02-122">Der Benutzer führt eine beliebige andere Aktion aus, z. b. einen Einfügevorgang, der **keine** Eingabe erfordert.</span><span class="sxs-lookup"><span data-stu-id="b6e02-122">The user performs any other action, such as a paste operation that does **not** involve typing.</span></span>

<span data-ttu-id="b6e02-123">Sie können die **EM \_ stopgrouptypisnachricht** senden, um aufeinander folgende Typisierungsaktionen in kleinere rückgängig-Gruppen zu unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="b6e02-123">You can send the **EM\_STOPGROUPTYPING** message to break consecutive typing actions into smaller undo groups.</span></span> <span data-ttu-id="b6e02-124">Sie könnten z. b. **EM \_ stopgrouptypisierung** nach jedem Zeichen oder bei jedem Wort Umbruch senden.</span><span class="sxs-lookup"><span data-stu-id="b6e02-124">For example, you could send **EM\_STOPGROUPTYPING** after each character or at each word break.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6e02-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6e02-125">Requirements</span></span>



| <span data-ttu-id="b6e02-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6e02-126">Requirement</span></span> | <span data-ttu-id="b6e02-127">Wert</span><span class="sxs-lookup"><span data-stu-id="b6e02-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b6e02-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b6e02-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b6e02-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6e02-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b6e02-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b6e02-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b6e02-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6e02-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b6e02-132">Header</span><span class="sxs-lookup"><span data-stu-id="b6e02-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6e02-133"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6e02-133"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6e02-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6e02-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6e02-135">**EM \_ rückgängig machen**</span><span class="sxs-lookup"><span data-stu-id="b6e02-135">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 





