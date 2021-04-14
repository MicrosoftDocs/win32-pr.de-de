---
title: LVM_GETISEARCHSTRING Meldung (kommstrg. h)
description: Ruft die inkrementelle Such Zeichenfolge eines Listenansicht-Steuer Elements ab. Sie können diese Nachricht explizit oder mithilfe des ListView \_ getisearchstring-Makros senden.
ms.assetid: e953c4a0-0556-4987-8abf-3276e787fe49
keywords:
- Windows-Steuerelemente für LVM_GETISEARCHSTRING Meldung
topic_type:
- apiref
api_name:
- LVM_GETISEARCHSTRING
- LVM_GETISEARCHSTRINGA
- LVM_GETISEARCHSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9040cf96c5c483b29764b1ccfb67e0e4fff3f897
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478525"
---
# <a name="lvm_getisearchstring-message"></a><span data-ttu-id="04a46-105">LVM- \_ getisearchstring-Nachricht</span><span class="sxs-lookup"><span data-stu-id="04a46-105">LVM\_GETISEARCHSTRING message</span></span>

<span data-ttu-id="04a46-106">Ruft die inkrementelle Such Zeichenfolge eines Listenansicht-Steuer Elements ab.</span><span class="sxs-lookup"><span data-stu-id="04a46-106">Retrieves the incremental search string of a list-view control.</span></span> <span data-ttu-id="04a46-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ getisearchstring**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getisearchstring) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="04a46-107">You can send this message explicitly or by using the [**ListView\_GetISearchString**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getisearchstring) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="04a46-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="04a46-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04a46-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="04a46-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="04a46-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="04a46-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="04a46-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="04a46-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="04a46-112">Zeiger auf einen Puffer, der die inkrementelle Such Zeichenfolge empfängt</span><span class="sxs-lookup"><span data-stu-id="04a46-112">Pointer to a buffer that receives the incremental search string.</span></span> <span data-ttu-id="04a46-113">Legen Sie *LPARAM* auf **null** fest, um die Länge der Zeichenfolge abzurufen.</span><span class="sxs-lookup"><span data-stu-id="04a46-113">To just retrieve the length of the string, set *lParam* to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04a46-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="04a46-114">Return value</span></span>

<span data-ttu-id="04a46-115">Gibt die Anzahl der Zeichen in der inkrementellen Such Zeichenfolge zurück, ohne das abschließende Null-Zeichen, oder 0 (null), wenn sich das Listenansicht-Steuerelement nicht im inkrementellen</span><span class="sxs-lookup"><span data-stu-id="04a46-115">Returns the number of characters in the incremental search string, not including the terminating NULL character, or zero if the list-view control is not in incremental search mode.</span></span>

## <a name="remarks"></a><span data-ttu-id="04a46-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04a46-116">Remarks</span></span>

<span data-ttu-id="04a46-117">**Sicherheitswarnung:** Wenn Sie diese Meldung falsch verwenden, kann dies die Sicherheit des Programms beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="04a46-117">**Security Warning:** Using this message incorrectly might compromise the security of your program.</span></span> <span data-ttu-id="04a46-118">Diese Meldung bietet keine Möglichkeit, die Größe des Puffers zu kennen.</span><span class="sxs-lookup"><span data-stu-id="04a46-118">This message does not provide a way for you to know the size of the buffer.</span></span> <span data-ttu-id="04a46-119">Wenn Sie diese Meldung verwenden, müssen Sie zuerst die Nachricht mit der Übergabe von **null** im *LPARAM*-Element aufzurufen. Dadurch wird die Anzahl der Zeichen zurückgegeben, ausgenommen **null** .</span><span class="sxs-lookup"><span data-stu-id="04a46-119">If you use this message, first call the message passing **NULL** in the *lParam*, this returns the number of characters, excluding **NULL** that are required.</span></span> <span data-ttu-id="04a46-120">Rufen Sie dann die Nachricht ein zweites Mal auf, um die Zeichenfolge abzurufen.</span><span class="sxs-lookup"><span data-stu-id="04a46-120">Then call the message a second time to retrieve the string.</span></span> <span data-ttu-id="04a46-121">Überprüfen Sie die [Sicherheitsaspekte: Microsoft Windows](sec-comctls.md) -Steuerelemente, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="04a46-121">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="04a46-122">Die *inkrementelle Such Zeichenfolge* ist die Zeichenfolge, die der Benutzer eingibt, während die Listenansicht den Eingabefokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="04a46-122">The *incremental search string* is the character sequence that the user types while the list view has the input focus.</span></span> <span data-ttu-id="04a46-123">Jedes Mal, wenn der Benutzer ein Zeichen eingibt, fügt das System das Zeichen an die Such Zeichenfolge an und sucht dann nach einem entsprechenden Element.</span><span class="sxs-lookup"><span data-stu-id="04a46-123">Each time the user types a character, the system appends the character to the search string and then searches for a matching item.</span></span> <span data-ttu-id="04a46-124">Wenn das System eine Entsprechung findet, wählt es das Element aus und führt ggf. einen Bildlauf in die Ansicht aus.</span><span class="sxs-lookup"><span data-stu-id="04a46-124">If the system finds a match, it selects the item and, if necessary, scrolls it into view.</span></span>

<span data-ttu-id="04a46-125">Jedem Zeichen, das der Benutzer eingibt, wird ein Timeout Zeitraum zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="04a46-125">A time-out period is associated with each character that the user types.</span></span> <span data-ttu-id="04a46-126">Wenn die Timeout Spanne abläuft, bevor der Benutzer ein anderes Zeichen eingibt, wird die Zeichenfolge für die inkrementelle Suche zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="04a46-126">If the time-out period elapses before the user types another character, the incremental search string is reset.</span></span>

<span data-ttu-id="04a46-127">Stellen Sie sicher, dass der Puffer groß genug ist, um die Zeichenfolge und das abschließende Null-Zeichen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="04a46-127">Make sure that the buffer is large enough to hold the string and the terminating NULL character.</span></span> <span data-ttu-id="04a46-128">Wenn es zu klein ist, wird ein sofortiger ungültiger Seiten Fehler zurückzuführen.</span><span class="sxs-lookup"><span data-stu-id="04a46-128">If it is too small, an immediate invalid page fault will result.</span></span>

## <a name="requirements"></a><span data-ttu-id="04a46-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04a46-129">Requirements</span></span>



| <span data-ttu-id="04a46-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04a46-130">Requirement</span></span> | <span data-ttu-id="04a46-131">Wert</span><span class="sxs-lookup"><span data-stu-id="04a46-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="04a46-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="04a46-132">Minimum supported client</span></span><br/> | <span data-ttu-id="04a46-133">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="04a46-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="04a46-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="04a46-134">Minimum supported server</span></span><br/> | <span data-ttu-id="04a46-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="04a46-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="04a46-136">Header</span><span class="sxs-lookup"><span data-stu-id="04a46-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="04a46-137"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="04a46-137"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="04a46-138">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="04a46-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="04a46-139">**LVM \_ Getisearchstringw** (Unicode) und **LVM \_ getisearchstrauinga** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="04a46-139">**LVM\_GETISEARCHSTRINGW** (Unicode) and **LVM\_GETISEARCHSTRINGA** (ANSI)</span></span><br/> |



 

 





