---
title: Iagentcharacter getvisibilitycause
description: Iagentcharacter getvisibilitycause
ms.assetid: 46f681de-1c99-4f90-a3fe-aae04bb75339
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6013385144b82b79a0f17ae6443b094a9d9c8a4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388809"
---
# <a name="iagentcharactergetvisibilitycause"></a><span data-ttu-id="906b1-103">Iagentcharacter:: getvisibilitycause</span><span class="sxs-lookup"><span data-stu-id="906b1-103">IAgentCharacter::GetVisibilityCause</span></span>

<span data-ttu-id="906b1-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="906b1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisibilityCause(
   long * pdwCause  // address of variable for cause of character visible state
);
```

<span data-ttu-id="906b1-105">Ruft die Ursache für den sichtbaren Zustand des Zeichens ab.</span><span class="sxs-lookup"><span data-stu-id="906b1-105">Retrieves the cause of the character's visible state.</span></span>

-   <span data-ttu-id="906b1-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="906b1-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="906b1-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwcause*</span><span class="sxs-lookup"><span data-stu-id="906b1-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span></span>
</dt> <dd>

<span data-ttu-id="906b1-108">Adresse einer Variablen, die die Ursache der letzten Änderung des Status der Sichtbarkeit des Zeichens empfängt und eine der folgenden ist:</span><span class="sxs-lookup"><span data-stu-id="906b1-108">Address of a variable that receives the cause of the character's last visibility state change and will be one of the following:</span></span>



| <span data-ttu-id="906b1-109">Wert</span><span class="sxs-lookup"><span data-stu-id="906b1-109">Value</span></span>                                                                   | <span data-ttu-id="906b1-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="906b1-110">Description</span></span>                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="906b1-111">Konstante ohne Vorzeichen, **nicht signiert** **= 0;**</span><span class="sxs-lookup"><span data-stu-id="906b1-111">**const unsigned short** **NeverShown = 0;**</span></span><br/>                 | <span data-ttu-id="906b1-112">Das Zeichen wurde nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="906b1-112">Character has not been shown.</span></span>                                                               |
| <span data-ttu-id="906b1-113">" **Ganzzahl ohne Vorzeichen Short** **userhid = 1;".**</span><span class="sxs-lookup"><span data-stu-id="906b1-113">**const unsigned short** **UserHid = 1;**</span></span><br/>                    | <span data-ttu-id="906b1-114">Der Benutzer hat das Zeichen mit dem Popup Menü des Task leisten Symbols oder mithilfe von Spracheingaben versteckt.</span><span class="sxs-lookup"><span data-stu-id="906b1-114">User hid the character with the character's taskbar icon pop-up menu or using speech input.</span></span> |
| <span data-ttu-id="906b1-115">"Konstante **Ganzzahl ohne Vorzeichen Short** **userhat = 2;** "</span><span class="sxs-lookup"><span data-stu-id="906b1-115">**const unsigned short** **UserShowed = 2;**</span></span><br/>                 | <span data-ttu-id="906b1-116">Der Benutzer hat das Zeichen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="906b1-116">User showed the character.</span></span>                                                                  |
| <span data-ttu-id="906b1-117">Konstante " **Ganzzahl ohne Vorzeichen Short** **Program HID = 3;** "</span><span class="sxs-lookup"><span data-stu-id="906b1-117">**const unsigned short** **ProgramHid = 3;**</span></span><br/>                 | <span data-ttu-id="906b1-118">Die Anwendung hat das Zeichen verborgen.</span><span class="sxs-lookup"><span data-stu-id="906b1-118">Your application hid the character.</span></span>                                                         |
| <span data-ttu-id="906b1-119">"Konstante **Ganzzahl ohne Vorzeichen Short** **Program" = 4;**</span><span class="sxs-lookup"><span data-stu-id="906b1-119">**const unsigned short** **ProgramShowed = 4;**</span></span><br/>              | <span data-ttu-id="906b1-120">Die Anwendung hat das Zeichen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="906b1-120">Your application showed the character.</span></span>                                                      |
| <span data-ttu-id="906b1-121">Konstante **Ganzzahl ohne Vorzeichen Short** **otherprogramhid = 5;**</span><span class="sxs-lookup"><span data-stu-id="906b1-121">**const unsigned short** **OtherProgramHid = 5;**</span></span><br/>            | <span data-ttu-id="906b1-122">Eine andere Anwendung hat das Zeichen verborgen.</span><span class="sxs-lookup"><span data-stu-id="906b1-122">Another application hid the character.</span></span>                                                      |
| <span data-ttu-id="906b1-123">" **Ganzzahl ohne Vorzeichen Short** otherprogram" in "Ganzzahl ohne Vorzeichen" **= 6;**</span><span class="sxs-lookup"><span data-stu-id="906b1-123">**const unsigned short** **OtherProgramShowed = 6;**</span></span><br/>         | <span data-ttu-id="906b1-124">Das Zeichen wurde in einer anderen Anwendung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="906b1-124">Another application showed the character.</span></span>                                                   |
| <span data-ttu-id="906b1-125">" **Ganzzahl ohne Vorzeichen Short" für "Ganzzahl ohne Vorzeichen Short** **userhidviacharactermenu = 7** "</span><span class="sxs-lookup"><span data-stu-id="906b1-125">**const unsigned short** **UserHidViaCharacterMenu = 7**</span></span><br/>     | <span data-ttu-id="906b1-126">Der Benutzer hat das Zeichen mit dem Popupmenü des Zeichens verborgen.</span><span class="sxs-lookup"><span data-stu-id="906b1-126">User hid the character with the character's pop-up menu.</span></span>                                    |
| <span data-ttu-id="906b1-127">Konstante **Ganzzahl ohne Vorzeichen Short** **userhidviataskbaricon = userhid**</span><span class="sxs-lookup"><span data-stu-id="906b1-127">**const unsigned short** **UserHidViaTaskbarIcon = UserHid**</span></span><br/> | <span data-ttu-id="906b1-128">Der Benutzer hat das Zeichen mit dem Popup Menü des Task leisten Symbols oder mithilfe von Spracheingaben versteckt.</span><span class="sxs-lookup"><span data-stu-id="906b1-128">User hid the character with the character's taskbar icon pop-up menu or using speech input.</span></span> |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="906b1-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="906b1-129">See Also</span></span>

[<span data-ttu-id="906b1-130">**Iagentnotifysink:: visiblestate**</span><span class="sxs-lookup"><span data-stu-id="906b1-130">**IAgentNotifySink::VisibleState**</span></span>](iagentnotifysink--visiblestate.md)


 

 





