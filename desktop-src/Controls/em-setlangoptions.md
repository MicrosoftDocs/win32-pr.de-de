---
title: EM_SETLANGOPTIONS Meldung (RichEdit. h)
description: Legt Optionen für den Eingabemethoden-Editor (IME) und die Unterstützung für asiatische Sprachen in einem Rich Edit-Steuerelement fest.
ms.assetid: d42d0512-3339-471d-a91a-114151554799
keywords:
- Windows-Steuerelemente für EM_SETLANGOPTIONS Meldung
topic_type:
- apiref
api_name:
- EM_SETLANGOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e5095c599dfa78740ce4cb081e4d52c33b2debd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949776"
---
# <a name="em_setlangoptions-message"></a><span data-ttu-id="afaf1-104">EM \_ setlangoptions-Meldung</span><span class="sxs-lookup"><span data-stu-id="afaf1-104">EM\_SETLANGOPTIONS message</span></span>

<span data-ttu-id="afaf1-105">Legt Optionen für den Eingabemethoden-Editor (IME) und die Unterstützung für asiatische Sprachen in einem Rich Edit-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="afaf1-105">Sets options for Input Method Editor (IME) and Asian language support in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="afaf1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="afaf1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afaf1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="afaf1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="afaf1-108">Dieser Parameter wird nicht verwendet. Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="afaf1-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="afaf1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="afaf1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="afaf1-110">Gibt die Sprachoptionen an.</span><span class="sxs-lookup"><span data-stu-id="afaf1-110">Specifies the language options.</span></span> <span data-ttu-id="afaf1-111">Eine Liste möglicher Werte finden Sie unter [**EM \_ getlangoptions**](em-getlangoptions.md).</span><span class="sxs-lookup"><span data-stu-id="afaf1-111">For a list of possible values, see [**EM\_GETLANGOPTIONS**](em-getlangoptions.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afaf1-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="afaf1-112">Return value</span></span>

<span data-ttu-id="afaf1-113">Diese Meldung gibt den Wert 1 zurück.</span><span class="sxs-lookup"><span data-stu-id="afaf1-113">This message returns a value of 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="afaf1-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="afaf1-114">Remarks</span></span>

<span data-ttu-id="afaf1-115">Die **\_ gesetlangoptions** -Nachricht steuert Folgendes:</span><span class="sxs-lookup"><span data-stu-id="afaf1-115">The **EM\_SETLANGOPTIONS** message controls the following:</span></span>

-   <span data-ttu-id="afaf1-116">Automatische Schriftart Bindung.</span><span class="sxs-lookup"><span data-stu-id="afaf1-116">Automatic font binding.</span></span>
-   <span data-ttu-id="afaf1-117">Automatischer Tastatur Wechsel.</span><span class="sxs-lookup"><span data-stu-id="afaf1-117">Automatic keyboard switching.</span></span>
-   <span data-ttu-id="afaf1-118">Automatische Anpassung der Schriftart Größe.</span><span class="sxs-lookup"><span data-stu-id="afaf1-118">Automatic font size adjustment.</span></span>
-   <span data-ttu-id="afaf1-119">Verwendung von Standard Schriftarten von Benutzeroberflächen anstelle von Dokument Standard Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="afaf1-119">Use of user-interface default fonts instead of document default fonts.</span></span>
-   <span data-ttu-id="afaf1-120">Benachrichtigungen an den Client während der IME-Komposition.</span><span class="sxs-lookup"><span data-stu-id="afaf1-120">Notifications to client during IME composition.</span></span>
-   <span data-ttu-id="afaf1-121">Gibt an, wie IME den Kompositions Modus abbricht.</span><span class="sxs-lookup"><span data-stu-id="afaf1-121">How IME aborts composition mode.</span></span>
-   <span data-ttu-id="afaf1-122">Rechtschreibprüfungs-, AutoCorrect-und Berührungs Tastatur Vorhersage.</span><span class="sxs-lookup"><span data-stu-id="afaf1-122">Spell checking, autocorrect, and touch keyboard prediction.</span></span>

<span data-ttu-id="afaf1-123">Diese Meldung legt die Werte aller sprachflags fest.</span><span class="sxs-lookup"><span data-stu-id="afaf1-123">This message sets the values of all language option flags.</span></span> <span data-ttu-id="afaf1-124">Um eine Teilmenge der Flags zu ändern, senden Sie die [**EM \_ getlangoptions**](em-getlangoptions.md) -Nachricht, um die aktuellen Options-Flags zu erhalten, ändern Sie die Flags, die Sie ändern müssen, und senden Sie dann die **EM \_ setlangoptions** -Nachricht mit dem Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="afaf1-124">To change a subset of the flags, send the [**EM\_GETLANGOPTIONS**](em-getlangoptions.md) message to get the current option flags, change the flags that you need to change, and then send the **EM\_SETLANGOPTIONS** message with the result.</span></span>

## <a name="requirements"></a><span data-ttu-id="afaf1-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="afaf1-125">Requirements</span></span>



| <span data-ttu-id="afaf1-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="afaf1-126">Requirement</span></span> | <span data-ttu-id="afaf1-127">Wert</span><span class="sxs-lookup"><span data-stu-id="afaf1-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="afaf1-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="afaf1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="afaf1-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="afaf1-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="afaf1-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="afaf1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="afaf1-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="afaf1-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="afaf1-132">Header</span><span class="sxs-lookup"><span data-stu-id="afaf1-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="afaf1-133"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="afaf1-133"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afaf1-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="afaf1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afaf1-135">**EM \_ getlangoptions**</span><span class="sxs-lookup"><span data-stu-id="afaf1-135">**EM\_GETLANGOPTIONS**</span></span>](em-getlangoptions.md)
</dt> </dl>

 

 





