---
title: Iagentnotifysink visiblestate
description: Iagentnotifysink visiblestate
ms.assetid: b0346296-74e9-448f-aa6d-a9fb1e645f05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3525c079ecd1b566ac2230f06e3effa1ceb7a694
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337389"
---
# <a name="iagentnotifysinkvisiblestate"></a><span data-ttu-id="d2071-103">Iagentnotifysink:: visiblestate</span><span class="sxs-lookup"><span data-stu-id="d2071-103">IAgentNotifySink::VisibleState</span></span>

<span data-ttu-id="d2071-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="d2071-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT VisibleState(
   long dwCharID,  // character ID
   long bVisible,  // visibility flag
   long dwCause,   // cause of visible state
);                          
```

<span data-ttu-id="d2071-105">Benachrichtigt eine Client Anwendung, wenn sich der Sichtbarkeits Zustand des Zeichens ändert.</span><span class="sxs-lookup"><span data-stu-id="d2071-105">Notifies a client application when the visibility state of the character changes.</span></span>

-   <span data-ttu-id="d2071-106">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="d2071-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="d2071-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwcharid*</span><span class="sxs-lookup"><span data-stu-id="d2071-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="d2071-108">Der Bezeichner des Zeichens, dessen Sichtbarkeits Zustand geändert wird.</span><span class="sxs-lookup"><span data-stu-id="d2071-108">Identifier of the character whose visibility state is changed.</span></span>

</dd> <dt>

<span data-ttu-id="d2071-109"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bvisible*</span><span class="sxs-lookup"><span data-stu-id="d2071-109"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="d2071-110">Sichtbarkeits Kennzeichen.</span><span class="sxs-lookup"><span data-stu-id="d2071-110">Visibility flag.</span></span> <span data-ttu-id="d2071-111">Dieser boolesche Wert ist **true** , wenn das Zeichen sichtbar wird, und **false** , wenn das Zeichen ausgeblendet wird.</span><span class="sxs-lookup"><span data-stu-id="d2071-111">This Boolean value is **True** when character becomes visible and **False** when the character becomes hidden.</span></span>

</dd> <dt>

<span data-ttu-id="d2071-112"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwcause*</span><span class="sxs-lookup"><span data-stu-id="d2071-112"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span></span>
</dt> <dd>

<span data-ttu-id="d2071-113">Ursache der letzten Änderung des Sichtbarkeits Zustands des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="d2071-113">Cause of last change to the character's visibility state.</span></span> <span data-ttu-id="d2071-114">Der Parameter kann eines der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="d2071-114">The parameter may be one of the following:</span></span>



| <span data-ttu-id="d2071-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d2071-115">Value</span></span>                                                                   | <span data-ttu-id="d2071-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2071-116">Description</span></span>                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2071-117">Konstante ohne Vorzeichen, **nicht signiert** **= 0;**</span><span class="sxs-lookup"><span data-stu-id="d2071-117">**const unsigned short** **NeverShown = 0;**</span></span><br/>                 | <span data-ttu-id="d2071-118">Das Zeichen wurde nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d2071-118">Character has not been shown.</span></span>                                                               |
| <span data-ttu-id="d2071-119">" **Ganzzahl ohne Vorzeichen Short** **userhid = 1;".**</span><span class="sxs-lookup"><span data-stu-id="d2071-119">**const unsigned short** **UserHid = 1;**</span></span><br/>                    | <span data-ttu-id="d2071-120">Der Benutzer hat das Zeichen mit dem Popup Menü des Task leisten Symbols oder mit der Spracheingabe ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="d2071-120">User hid the character with the character's taskbar icon pop-up menu or with speech input..</span></span> |
| <span data-ttu-id="d2071-121">"Konstante **Ganzzahl ohne Vorzeichen Short** **userhat = 2;** "</span><span class="sxs-lookup"><span data-stu-id="d2071-121">**const unsigned short** **UserShowed = 2;**</span></span><br/>                 | <span data-ttu-id="d2071-122">Der Benutzer hat das Zeichen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d2071-122">User showed the character.</span></span>                                                                  |
| <span data-ttu-id="d2071-123">Konstante " **Ganzzahl ohne Vorzeichen Short** **Program HID = 3;** "</span><span class="sxs-lookup"><span data-stu-id="d2071-123">**const unsigned short** **ProgramHid = 3;**</span></span><br/>                 | <span data-ttu-id="d2071-124">Die Anwendung hat das Zeichen verborgen.</span><span class="sxs-lookup"><span data-stu-id="d2071-124">Your application hid the character.</span></span>                                                         |
| <span data-ttu-id="d2071-125">"Konstante **Ganzzahl ohne Vorzeichen Short** **Program" = 4;**</span><span class="sxs-lookup"><span data-stu-id="d2071-125">**const unsigned short** **ProgramShowed = 4;**</span></span><br/>              | <span data-ttu-id="d2071-126">Die Anwendung hat das Zeichen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d2071-126">Your application showed the character.</span></span>                                                      |
| <span data-ttu-id="d2071-127">Konstante **Ganzzahl ohne Vorzeichen Short** **otherprogramhid = 5;**</span><span class="sxs-lookup"><span data-stu-id="d2071-127">**const unsigned short** **OtherProgramHid = 5;**</span></span><br/>            | <span data-ttu-id="d2071-128">Eine andere Anwendung hat das Zeichen verborgen.</span><span class="sxs-lookup"><span data-stu-id="d2071-128">Another application hid the character.</span></span>                                                      |
| <span data-ttu-id="d2071-129">" **Ganzzahl ohne Vorzeichen Short** otherprogram" in "Ganzzahl ohne Vorzeichen" **= 6;**</span><span class="sxs-lookup"><span data-stu-id="d2071-129">**const unsigned short** **OtherProgramShowed = 6;**</span></span><br/>         | <span data-ttu-id="d2071-130">Das Zeichen wurde in einer anderen Anwendung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d2071-130">Another application showed the character.</span></span>                                                   |
| <span data-ttu-id="d2071-131">" **Ganzzahl ohne Vorzeichen Short" für "Ganzzahl ohne Vorzeichen Short** **userhidviacharactermenu = 7** "</span><span class="sxs-lookup"><span data-stu-id="d2071-131">**const unsigned short** **UserHidViaCharacterMenu = 7**</span></span><br/>     | <span data-ttu-id="d2071-132">Der Benutzer hat das Zeichen mit dem Popupmenü des Zeichens verborgen.</span><span class="sxs-lookup"><span data-stu-id="d2071-132">User hid the character with the character's pop-up menu.</span></span>                                    |
| <span data-ttu-id="d2071-133">Konstante **Ganzzahl ohne Vorzeichen Short** **userhidviataskbaricon = userhid**</span><span class="sxs-lookup"><span data-stu-id="d2071-133">**const unsigned short** **UserHidViaTaskbarIcon = UserHid**</span></span><br/> | <span data-ttu-id="d2071-134">Der Benutzer hat das Zeichen mit dem Popup Menü des Task leisten Symbols oder mithilfe von Spracheingaben versteckt.</span><span class="sxs-lookup"><span data-stu-id="d2071-134">User hid the character with the character's taskbar icon pop-up menu or using speech input.</span></span> |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="d2071-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d2071-135">See Also</span></span>

<span data-ttu-id="d2071-136">[**Iagentcharacter:: getVisible**](iagentcharacter--getvisible.md), [ **iagentcharacter:: getvisibilitycause**](iagentcharacter--getvisibilitycause.md)</span><span class="sxs-lookup"><span data-stu-id="d2071-136">[**IAgentCharacter::GetVisible**](iagentcharacter--getvisible.md), [**IAgentCharacter::GetVisibilityCause**](iagentcharacter--getvisibilitycause.md)</span></span>


 

 





