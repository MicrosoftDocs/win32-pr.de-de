---
title: Controls. FastForward-Methode
description: Die FastForward-Methode startet die schnelle Wiedergabe des Medien Elements in Vorwärtsrichtung. | Controls. FastForward-Methode
ms.assetid: 69cee803-f76b-4a8c-a2c2-1870665afaf9
keywords:
- FastForward-Methoden Fenster Media Player
- FastForward-Methode, Windows Media Player, Controls-Klasse
- Steuerelemente-Klasse, Windows Media Player, FastForward-Methode
topic_type:
- apiref
api_name:
- Controls.fastForward
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20d033b8b025955e57a9c3ebed00a6d7a92a666e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357640"
---
# <a name="controlsfastforward-method"></a><span data-ttu-id="29d82-107">Controls. FastForward-Methode</span><span class="sxs-lookup"><span data-stu-id="29d82-107">Controls.fastForward method</span></span>

<span data-ttu-id="29d82-108">Die **FastForward** -Methode startet die schnelle Wiedergabe des Medien Elements in Vorwärtsrichtung.</span><span class="sxs-lookup"><span data-stu-id="29d82-108">The **fastForward** method starts fast play of the media item in the forward direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="29d82-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="29d82-109">Syntax</span></span>


```JScript
Controls.fastForward()
```



## <a name="parameters"></a><span data-ttu-id="29d82-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="29d82-110">Parameters</span></span>

<span data-ttu-id="29d82-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="29d82-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="29d82-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="29d82-112">Return value</span></span>

<span data-ttu-id="29d82-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="29d82-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="29d82-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29d82-114">Remarks</span></span>

<span data-ttu-id="29d82-115">Die **FastForward** -Methode gibt den Clip mit dem fünf fachen der normalen Geschwindigkeit wieder.</span><span class="sxs-lookup"><span data-stu-id="29d82-115">The **fastForward** method plays the clip back at five times the normal speed.</span></span> <span data-ttu-id="29d82-116">Durch Aufrufen von **FastForward** werden die *Einstellungen* geändert. **bewerten** Sie die-Eigenschaft auf 5,0.</span><span class="sxs-lookup"><span data-stu-id="29d82-116">Invoking **fastForward** changes the *Settings*.**rate** property to 5.0.</span></span> <span data-ttu-id="29d82-117">Wenn die **Rate** anschließend geändert wird **oder wenn "** wiedergeben" oder " **Beenden** " aufgerufen wird, wird die schnelle Weiterleitung von Windows Media Player beendet.</span><span class="sxs-lookup"><span data-stu-id="29d82-117">If **rate** is subsequently changed, or if **play** or **stop** is called, Windows Media Player will cease fast forwarding.</span></span>

<span data-ttu-id="29d82-118">Die **FastForward** -Methode funktioniert nicht für Live-Übertragungen und bestimmte Medientypen.</span><span class="sxs-lookup"><span data-stu-id="29d82-118">The **fastForward** method does not work for live broadcasts and certain media types.</span></span> <span data-ttu-id="29d82-119">Um zu ermitteln, ob Sie sich in einem Clip schnell vorwärts befinden, nennen Sie **IsAvailable**("FastForward").</span><span class="sxs-lookup"><span data-stu-id="29d82-119">To determine whether you can fast forward in a clip, call **isAvailable**("FastForward").</span></span>

## <a name="examples"></a><span data-ttu-id="29d82-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="29d82-120">Examples</span></span>

<span data-ttu-id="29d82-121">Im folgenden Beispiel wird ein HTML-Schaltflächen Element erstellt, das **FastForward** verwendet, um die schnelle Wiedergabe des Medien Elements zu starten.</span><span class="sxs-lookup"><span data-stu-id="29d82-121">The following example creates an HTML BUTTON element that uses **fastForward** to start fast play of the media item.</span></span> <span data-ttu-id="29d82-122">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="29d82-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "FF"  NAME = "FF"  VALUE = ">>"  

    /* Execute JScript when the BUTTON is clicked. 
       Check first to make sure fast-forward mode is available
       for this particular media item */
    onClick = "if (Player.controls.isAvailable('FastForward'))
        Player.controls.fastForward();
">

```



## <a name="requirements"></a><span data-ttu-id="29d82-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29d82-123">Requirements</span></span>



| <span data-ttu-id="29d82-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29d82-124">Requirement</span></span> | <span data-ttu-id="29d82-125">Wert</span><span class="sxs-lookup"><span data-stu-id="29d82-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="29d82-126">Version</span><span class="sxs-lookup"><span data-stu-id="29d82-126">Version</span></span><br/> | <span data-ttu-id="29d82-127">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="29d82-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="29d82-128">DLL</span><span class="sxs-lookup"><span data-stu-id="29d82-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="29d82-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29d82-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29d82-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29d82-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29d82-131">**Controls-Objekt**</span><span class="sxs-lookup"><span data-stu-id="29d82-131">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="29d82-132">**Controls. IsAvailable**</span><span class="sxs-lookup"><span data-stu-id="29d82-132">**Controls.isAvailable**</span></span>](controls-isavailable.md)
</dt> <dt>

[<span data-ttu-id="29d82-133">**Controls. Play**</span><span class="sxs-lookup"><span data-stu-id="29d82-133">**Controls.play**</span></span>](controls-play.md)
</dt> <dt>

[<span data-ttu-id="29d82-134">**Controls. Pause**</span><span class="sxs-lookup"><span data-stu-id="29d82-134">**Controls.stop**</span></span>](controls-stop.md)
</dt> <dt>

[<span data-ttu-id="29d82-135">**"Settings. Rate"**</span><span class="sxs-lookup"><span data-stu-id="29d82-135">**Settings.rate**</span></span>](settings-rate.md)
</dt> </dl>

 

 





