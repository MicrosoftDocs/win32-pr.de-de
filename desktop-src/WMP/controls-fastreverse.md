---
title: Controls. fastreverse-Methode
description: Die fastreverse-Methode startet die schnelle Überprüfung des Medien Elements in umgekehrter Richtung.
ms.assetid: 4fc61739-9006-4d62-b2c1-2b8e8830f2d9
keywords:
- fastreverse-Methode, Windows-Media Player
- fastreverse-Methode, Windows Media Player, Controls-Klasse
- Steuerelemente-Klasse, Windows Media Player, fastreverse-Methode
topic_type:
- apiref
api_name:
- Controls.fastReverse
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73e5a63c4299bf08c25e36e2d61924f3fb171792
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370049"
---
# <a name="controlsfastreverse-method"></a><span data-ttu-id="e58f4-106">Controls. fastreverse-Methode</span><span class="sxs-lookup"><span data-stu-id="e58f4-106">Controls.fastReverse method</span></span>

<span data-ttu-id="e58f4-107">Die **fastreverse** -Methode startet die schnelle Überprüfung des Medien Elements in umgekehrter Richtung.</span><span class="sxs-lookup"><span data-stu-id="e58f4-107">The **fastReverse** method starts fast scanning of the media item in the reverse direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="e58f4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e58f4-108">Syntax</span></span>


```JScript
Controls.fastReverse()
```



## <a name="parameters"></a><span data-ttu-id="e58f4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e58f4-109">Parameters</span></span>

<span data-ttu-id="e58f4-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e58f4-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e58f4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e58f4-111">Return value</span></span>

<span data-ttu-id="e58f4-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e58f4-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e58f4-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e58f4-113">Remarks</span></span>

<span data-ttu-id="e58f4-114">Die **fastreverse** -Methode scannt den Clip in umgekehrter Reihenfolge mit dem fünfmal normalen Tempo und zeigt nur die Keyframes an, wenn es sich um eine Videodatei handelt.</span><span class="sxs-lookup"><span data-stu-id="e58f4-114">The **fastReverse** method scans the clip in reverse at five times the normal speed, displaying only the key frames if it is a video file.</span></span> <span data-ttu-id="e58f4-115">Durch Aufrufen von **fastreverse** werden die *Einstellungen* geändert. **bewerten** Sie die-Eigenschaft auf 5,0.</span><span class="sxs-lookup"><span data-stu-id="e58f4-115">Invoking **fastReverse** changes the *Settings*.**rate** property to  5.0.</span></span> <span data-ttu-id="e58f4-116">Wenn die **Rate** anschließend geändert wird **oder wenn "** wiedergeben" oder " **Beenden** " aufgerufen wird, wird Windows Media Player schnell umkehren.</span><span class="sxs-lookup"><span data-stu-id="e58f4-116">If **rate** is subsequently changed, or if **play** or **stop** is called, Windows Media Player will cease fast reverse.</span></span>

<span data-ttu-id="e58f4-117">Wenn das Element Teil einer Wiedergabeliste ist, wird **fastreverse** am Anfang der aktuellen Spur angehalten. Wenn sich beispielsweise Track 3 in **fastreverse** befindet und der Anfang von Track 3 erreicht wird, wechselt Windows Media Player nicht mehr zu Track 2.</span><span class="sxs-lookup"><span data-stu-id="e58f4-117">If the item is part of a playlist, **fastReverse** stops at the beginning of the current track. For instance, if track 3 is in **fastReverse**, when the beginning of track 3 is reached, Windows Media Player will not go to track 2.</span></span> <span data-ttu-id="e58f4-118">Die Wiedergabe Anzahl wird beim Aufrufen von **fastreverse** nicht inkrementiert.</span><span class="sxs-lookup"><span data-stu-id="e58f4-118">The play count is not incremented when calling **fastReverse**.</span></span>

<span data-ttu-id="e58f4-119">Wenn Sie **FastForward** aufzurufen, während **fastreverse** wirksam ist, wird **fastreverse** angehalten, und **FastForward** wird begonnen.</span><span class="sxs-lookup"><span data-stu-id="e58f4-119">If you call **fastForward** while **fastReverse** is in effect, **fastReverse** will be stopped and **fastForward** will begin.</span></span>

<span data-ttu-id="e58f4-120">Diese Methode funktioniert nicht für Live-Übertragungen und bestimmte Medientypen.</span><span class="sxs-lookup"><span data-stu-id="e58f4-120">This method does not work for live broadcasts and certain media types.</span></span> <span data-ttu-id="e58f4-121">Um zu ermitteln, ob Sie fast Reverse in einem Clip verwenden können, nennen Sie **IsAvailable**("fastreverse").</span><span class="sxs-lookup"><span data-stu-id="e58f4-121">To determine whether you can use fast reverse in a clip, call **isAvailable**("FastReverse").</span></span>

## <a name="examples"></a><span data-ttu-id="e58f4-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e58f4-122">Examples</span></span>

<span data-ttu-id="e58f4-123">Im folgenden Beispiel wird ein HTML-Schaltflächen Element erstellt, das **fastreverse** verwendet, um den schnellen umgekehrten Wiedergabe des Medien Elements zu starten.</span><span class="sxs-lookup"><span data-stu-id="e58f4-123">The following example creates an HTML BUTTON element that uses **fastReverse** to start fast-reverse play of the media item.</span></span> <span data-ttu-id="e58f4-124">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="e58f4-124">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "REW"  NAME = "REW"  VALUE = "<<"  

    /* Run JScript when the BUTTON is clicked. 
       Check first to make sure fast-reverse mode is available
       for this particular media item */
    onClick = "if (Player.controls.isAvailable('FastReverse'))
        Player.controls.fastReverse();
">
```



## <a name="requirements"></a><span data-ttu-id="e58f4-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e58f4-125">Requirements</span></span>



| <span data-ttu-id="e58f4-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e58f4-126">Requirement</span></span> | <span data-ttu-id="e58f4-127">Wert</span><span class="sxs-lookup"><span data-stu-id="e58f4-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e58f4-128">Version</span><span class="sxs-lookup"><span data-stu-id="e58f4-128">Version</span></span><br/> | <span data-ttu-id="e58f4-129">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="e58f4-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="e58f4-130">DLL</span><span class="sxs-lookup"><span data-stu-id="e58f4-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="e58f4-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e58f4-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e58f4-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e58f4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e58f4-133">**Controls-Objekt**</span><span class="sxs-lookup"><span data-stu-id="e58f4-133">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="e58f4-134">**Controls. FastForward**</span><span class="sxs-lookup"><span data-stu-id="e58f4-134">**Controls.fastForward**</span></span>](controls-fastforward.md)
</dt> <dt>

[<span data-ttu-id="e58f4-135">**Controls. IsAvailable**</span><span class="sxs-lookup"><span data-stu-id="e58f4-135">**Controls.isAvailable**</span></span>](controls-isavailable.md)
</dt> <dt>

[<span data-ttu-id="e58f4-136">**Controls. Play**</span><span class="sxs-lookup"><span data-stu-id="e58f4-136">**Controls.play**</span></span>](controls-play.md)
</dt> <dt>

[<span data-ttu-id="e58f4-137">**Controls. Pause**</span><span class="sxs-lookup"><span data-stu-id="e58f4-137">**Controls.stop**</span></span>](controls-stop.md)
</dt> <dt>

[<span data-ttu-id="e58f4-138">**"Settings. Rate"**</span><span class="sxs-lookup"><span data-stu-id="e58f4-138">**Settings.rate**</span></span>](settings-rate.md)
</dt> </dl>

 

 





