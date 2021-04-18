---
title: Player. Fullscreen
description: Mit der FullScreen-Eigenschaft wird ein Wert angegeben oder abgerufen, der angibt, ob Videoinhalte im Vollbildmodus wiedergegeben werden.
ms.assetid: 43eeeddd-13a6-44d8-9cff-a60e976fc189
keywords:
- Player. Fullscreen-Fenster Media Player
topic_type:
- apiref
api_name:
- Player.fullScreen
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3f71b4100c359effd95f79c574a52b5a5bae28c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358243"
---
# <a name="playerfullscreen"></a><span data-ttu-id="151c9-104">Player. Fullscreen</span><span class="sxs-lookup"><span data-stu-id="151c9-104">Player.fullScreen</span></span>

<span data-ttu-id="151c9-105">Mit der **Fullscreen** -Eigenschaft wird ein Wert angegeben oder abgerufen, der angibt, ob Videoinhalte im Vollbildmodus wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="151c9-105">The **fullScreen** property specifies or retrieves a value indicating whether video content is played back in full-screen mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="151c9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="151c9-106">Syntax</span></span>

<span data-ttu-id="151c9-107">*Player* . **Vollbild**</span><span class="sxs-lookup"><span data-stu-id="151c9-107">*player* .**fullScreen**</span></span>

## <a name="possible-values"></a><span data-ttu-id="151c9-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="151c9-108">Possible Values</span></span>

<span data-ttu-id="151c9-109">Diese Eigenschaft ist ein **boolescher** Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="151c9-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="151c9-110">Wert</span><span class="sxs-lookup"><span data-stu-id="151c9-110">Value</span></span> | <span data-ttu-id="151c9-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="151c9-111">Description</span></span>                                                    |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="151c9-112">true</span><span class="sxs-lookup"><span data-stu-id="151c9-112">true</span></span>  | <span data-ttu-id="151c9-113">Video Inhalte werden im Vollbildmodus wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="151c9-113">Video content is played back in full-screen mode.</span></span>              |
| <span data-ttu-id="151c9-114">false</span><span class="sxs-lookup"><span data-stu-id="151c9-114">false</span></span> | <span data-ttu-id="151c9-115">Standard.</span><span class="sxs-lookup"><span data-stu-id="151c9-115">Default.</span></span> <span data-ttu-id="151c9-116">Video Inhalte werden im Vollbildmodus nicht wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="151c9-116">Video content is not played back in full-screen mode.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="151c9-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="151c9-117">Remarks</span></span>

<span data-ttu-id="151c9-118">Damit der Vollbildmodus beim Einbetten des Windows Media Player-Steuer Elements ordnungsgemäß funktioniert, muss der Videoanzeige Bereich eine Höhe und Breite von mindestens einem Pixel aufweisen.</span><span class="sxs-lookup"><span data-stu-id="151c9-118">For full-screen mode to work properly when embedding the Windows Media Player control, the video display area must have a height and width of at least one pixel.</span></span> <span data-ttu-id="151c9-119">Wenn **uiMode** auf "Mini" oder "Full" festgelegt ist, muss die Höhe des Steuer Elements auf 65 oder höher festgelegt sein, um zusätzlich zur Benutzeroberfläche den Videoanzeige Bereich aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="151c9-119">If **uiMode** is set to "mini" or "full", the height of the control itself must be 65 or greater to accommodate the video display area in addition to the user interface.</span></span>

<span data-ttu-id="151c9-120">Wenn **uiMode** auf "unsichtbar" festgelegt ist, löst das Festlegen dieser Eigenschaft auf true einen Fehler aus und wirkt sich nicht auf das Verhalten des Steuer Elements aus.</span><span class="sxs-lookup"><span data-stu-id="151c9-120">If **uiMode** is set to "invisible", then setting this property to true raises an error and does not affect the behavior of the control.</span></span>

<span data-ttu-id="151c9-121">Während der Vollbildwiedergabe blendet Windows Media Player den Mauszeiger aus, wenn **enablecontextmenu** den Wert false hat und **uiMode** den Wert "None" hat.</span><span class="sxs-lookup"><span data-stu-id="151c9-121">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

<span data-ttu-id="151c9-122">Wenn **uiMode** auf "Full" oder "Mini" festgelegt ist, zeigt Windows Media Player Transport Steuerelemente im Vollbildmodus an, wenn der Mauszeiger bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="151c9-122">If **uiMode** is set to "full" or "mini", Windows Media Player displays transport controls in full-screen mode when the mouse cursor moves.</span></span> <span data-ttu-id="151c9-123">Nach einem kurzen Intervall ohne Mausbewegung werden die Transport Steuerelemente ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="151c9-123">After a brief interval of no mouse movement, the transport controls are hidden.</span></span> <span data-ttu-id="151c9-124">Wenn **uiMode** auf "None" festgelegt ist, werden keine Steuerelemente im Vollbildmodus angezeigt.</span><span class="sxs-lookup"><span data-stu-id="151c9-124">If **uiMode** is set to "none", no controls are displayed in full-screen mode.</span></span>

<span data-ttu-id="151c9-125">**Hinweis**</span><span class="sxs-lookup"><span data-stu-id="151c9-125">**Note**</span></span>

<span data-ttu-id="151c9-126">Zum Anzeigen von Transport Steuerelementen im Vollbildmodus ist das Betriebssystem Windows XP erforderlich.</span><span class="sxs-lookup"><span data-stu-id="151c9-126">Displaying transport controls in full-screen mode requires the Windows XP operating system.</span></span>

<span data-ttu-id="151c9-127">Wenn Transport Steuerelemente nicht im Vollbildmodus angezeigt werden, beendet Windows Media Player den Vollbildmodus automatisch, wenn die Wiedergabe angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="151c9-127">If transport controls are not displayed in full-screen mode, then Windows Media Player automatically exits full-screen mode when playback stops.</span></span>

<span data-ttu-id="151c9-128">**Hinweis**</span><span class="sxs-lookup"><span data-stu-id="151c9-128">**Note**</span></span>

<span data-ttu-id="151c9-129">Stellen Sie sicher, dass Sie den Benutzer darüber informieren, wie Sie den Vollbildmodus zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="151c9-129">Always be sure to inform the user how to return from full-screen mode.</span></span>

## <a name="examples"></a><span data-ttu-id="151c9-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="151c9-130">Examples</span></span>

<span data-ttu-id="151c9-131">Im folgenden Beispiel wird eine HTML-Eingabe Schaltfläche erstellt, die *Player* verwendet. **Vollbild** , um ein eingebettetes Player-Objekt in den Vollbildmodus zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="151c9-131">The following example creates an HTML input button that uses *Player*.**fullScreen** to switch an embedded player object to full-screen mode.</span></span> <span data-ttu-id="151c9-132">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="151c9-132">The **Player** object was created with ID = "Player".</span></span>


```
<INPUT type = button 
       value = "Full Screen" 
       name = FSBUTTON
       onclick = "
               /* Check to be sure the player is playing. */
               if (Player.playState == 3) 
                  Player.fullScreen = 'true';
               ">
```



## <a name="requirements"></a><span data-ttu-id="151c9-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="151c9-133">Requirements</span></span>



| <span data-ttu-id="151c9-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="151c9-134">Requirement</span></span> | <span data-ttu-id="151c9-135">Wert</span><span class="sxs-lookup"><span data-stu-id="151c9-135">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="151c9-136">Version</span><span class="sxs-lookup"><span data-stu-id="151c9-136">Version</span></span><br/> | <span data-ttu-id="151c9-137">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="151c9-137">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="151c9-138">DLL</span><span class="sxs-lookup"><span data-stu-id="151c9-138">DLL</span></span><br/>     | <dl> <span data-ttu-id="151c9-139"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="151c9-139"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="151c9-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="151c9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="151c9-141">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="151c9-141">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





