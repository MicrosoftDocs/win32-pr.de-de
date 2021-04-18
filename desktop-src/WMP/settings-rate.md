---
title: "\"Settings. Rate\""
description: Die Rate-Eigenschaft gibt die aktuelle Wiedergabe Rate von Video Medien an oder ruft diese ab.
ms.assetid: 0f95f7ac-1bb6-4c80-89eb-eb300a03a0f1
keywords:
- Einstellungen. Raten Sie Windows Media Player
topic_type:
- apiref
api_name:
- Settings.rate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61287789487fddbe7e77fba5fc033d3103aecb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357652"
---
# <a name="settingsrate"></a><span data-ttu-id="6b8ef-104">"Settings. Rate"</span><span class="sxs-lookup"><span data-stu-id="6b8ef-104">Settings.rate</span></span>

<span data-ttu-id="6b8ef-105">Die **Rate** -Eigenschaft gibt die aktuelle Wiedergabe Rate von Video Medien an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="6b8ef-105">The **rate** property specifies or retrieves the current playback rate of video media.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b8ef-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b8ef-106">Syntax</span></span>

<span data-ttu-id="6b8ef-107">Player. Settings. Rate</span><span class="sxs-lookup"><span data-stu-id="6b8ef-107">player.settings.rate</span></span>

## <a name="possible-values"></a><span data-ttu-id="6b8ef-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="6b8ef-108">Possible Values</span></span>

<span data-ttu-id="6b8ef-109">Diese Eigenschaft ist eine Lese-/schreibzahl (**Double**) mit einem Standardwert von 1,0. </span><span class="sxs-lookup"><span data-stu-id="6b8ef-109">This property is a read/write **Number** (**double**) with a default value of 1.0.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b8ef-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b8ef-110">Remarks</span></span>

<span data-ttu-id="6b8ef-111">Diese Eigenschaft fungiert als Multiplikatorwert, mit dem Sie einen Clip schneller oder langsamer abspielen können.</span><span class="sxs-lookup"><span data-stu-id="6b8ef-111">This property acts as a multiplier value that allows you to play a clip at a faster or slower rate.</span></span> <span data-ttu-id="6b8ef-112">Der Standardwert 1,0 gibt die erstellte Geschwindigkeit an.</span><span class="sxs-lookup"><span data-stu-id="6b8ef-112">The default value of 1.0 indicates the authored speed.</span></span> <span data-ttu-id="6b8ef-113">Beachten Sie, dass eine Audiospur bei Raten, die niedriger als 0,5 oder höher als 1,5 sind, schwer zu verstehen ist.</span><span class="sxs-lookup"><span data-stu-id="6b8ef-113">Note that an audio track becomes difficult to understand at rates lower than 0.5 or higher than 1.5.</span></span> <span data-ttu-id="6b8ef-114">Eine Wiedergabe Rate von 2 entspricht der doppelten normalen Wiedergabegeschwindigkeit.</span><span class="sxs-lookup"><span data-stu-id="6b8ef-114">A playback rate of 2 equates to twice the normal playback speed.</span></span>

<span data-ttu-id="6b8ef-115">Windows Media Player versucht, die effektivsten von vier verschiedenen Wiedergabe Modi zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6b8ef-115">Windows Media Player will attempt to use the most effective of four different playback modes.</span></span> <span data-ttu-id="6b8ef-116">Bei diesen Modi handelt es sich um eine reibungslose Videowiedergabe, bei der Audiowiedergabe gewartet wird, eine nahtlose Videowiedergabe mit nicht gebeibehaltung Audiowiedergabe, eine Smooth Videowiedergabe ohne Audiodaten und eine Keyframe-Videowiedergabe ohne Audio</span><span class="sxs-lookup"><span data-stu-id="6b8ef-116">These modes are smooth video playback with audio pitch maintained, smooth video playback with audio pitch not maintained, smooth video playback with no audio, and keyframe video playback with no audio.</span></span> <span data-ttu-id="6b8ef-117">Der vom Player gewählte Modus hängt von zahlreichen Faktoren ab, einschließlich Dateityp und-Speicherort, Betriebssystem, Netzwerk und Server.</span><span class="sxs-lookup"><span data-stu-id="6b8ef-117">The mode chosen by the Player depends on numerous factors including file type and location, operating system, network, and server.</span></span>

<span data-ttu-id="6b8ef-118">Es gelten auch weitere Überlegungen, abhängig vom Medientyp:</span><span class="sxs-lookup"><span data-stu-id="6b8ef-118">Other considerations apply as well, depending on media type:</span></span>

-   <span data-ttu-id="6b8ef-119">Windows Media-Format (WMV) und ASF-Dateien: optimale Werte für diese Eigenschaft liegen zwischen 1 und 10 oder zwischen 1 und 10 für Reverse-Play.</span><span class="sxs-lookup"><span data-stu-id="6b8ef-119">Windows Media Format (WMV) and ASF files: Optimal values for this property are from 1 to 10, or from  1 to  10 for reverse play.</span></span> <span data-ttu-id="6b8ef-120">Werte zwischen 0,5 und 1,0 oder von-0,5 bis 1,0 funktionieren möglicherweise auch in Fällen, in denen audiotonhöhe beibehalten werden kann, z. b. bei der Wiedergabe von Dateien auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="6b8ef-120">Values from 0.5 to 1.0 or from -0.5 to -1.0 may also work well in cases where audio pitch can be maintained, for example, when playing files located on the local computer.</span></span> <span data-ttu-id="6b8ef-121">Werte mit einer absoluten Größe von mehr als 10 sind zulässig, sind jedoch nicht sehr sinnvoll.</span><span class="sxs-lookup"><span data-stu-id="6b8ef-121">Values with an absolute magnitude greater than 10 are allowed, but are not very meaningful.</span></span>
-   <span data-ttu-id="6b8ef-122">Andere Video Medientypen: Diese Eigenschaft kann zwischen 0 und 9 liegen.</span><span class="sxs-lookup"><span data-stu-id="6b8ef-122">Other Video Media Types: This property can range from 0 to 9.</span></span> <span data-ttu-id="6b8ef-123">Negative Werte sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="6b8ef-123">Negative values are not allowed.</span></span> <span data-ttu-id="6b8ef-124">Werte kleiner als 1 stellen eine langsame Bewegung dar.</span><span class="sxs-lookup"><span data-stu-id="6b8ef-124">Values less than 1 represent slow motion.</span></span> <span data-ttu-id="6b8ef-125">Werte oberhalb von 9 sind zulässig, sind jedoch nicht sehr sinnvoll.</span><span class="sxs-lookup"><span data-stu-id="6b8ef-125">Values above 9 are allowed, but are not very meaningful.</span></span>

<span data-ttu-id="6b8ef-126">Die-Steuer *Elemente*. die **FastForward** -Methode ändert den Wert von Rate in 5,0, während die **Steuer** *Elemente*. die **Rate** der **fastreverse** -Methode wurde in 5,0 geändert.</span><span class="sxs-lookup"><span data-stu-id="6b8ef-126">The *Controls*.**fastForward** method changes the value of **rate** to 5.0, while the *Controls*.**fastReverse** method changes **rate** to  5.0.</span></span>

<span data-ttu-id="6b8ef-127">Die Wiedergabe Rate einiger Medientypen kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="6b8ef-127">The playback rate of some media types cannot be altered.</span></span> <span data-ttu-id="6b8ef-128">Verwenden Sie die *Einstellungen*. **IsAvailable** -Methode, um zu bestimmen, ob diese Eigenschaft für ein bestimmtes Medien Element angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="6b8ef-128">Use the *Settings*.**isAvailable** method to determine whether this property can be specified for a particular media item.</span></span>

<span data-ttu-id="6b8ef-129">**Windows Media Player 10 Mobile**: Diese Eigenschaft akzeptiert nur die Werte von-5,0, 1,0 oder 5,0.</span><span class="sxs-lookup"><span data-stu-id="6b8ef-129">**Windows Media Player 10 Mobile**: This property only accepts or returns values of -5.0, 1.0, or 5.0.</span></span>

## <a name="examples"></a><span data-ttu-id="6b8ef-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6b8ef-130">Examples</span></span>

<span data-ttu-id="6b8ef-131">Im folgenden Beispiel wird ein HTML-SELECT-Element erstellt, das es dem Benutzer ermöglicht, die Wiedergabegeschwindigkeit des aktuellen Mediums zu ändern.</span><span class="sxs-lookup"><span data-stu-id="6b8ef-131">The following example creates an HTML SELECT element that allows the user to change the playback speed of the current media.</span></span> <span data-ttu-id="6b8ef-132">Die SELECT-Optionen bieten eine normale Geschwindigkeit, eine halbe Geschwindigkeit und eine doppelte Geschwindigkeit der Wiedergabe Raten.</span><span class="sxs-lookup"><span data-stu-id="6b8ef-132">The SELECT options offer normal speed, half -speed and double-speed playback rates.</span></span> <span data-ttu-id="6b8ef-133">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="6b8ef-133">The **Player** object was created with ID = "Player".</span></span>


```
<!-- Create the HTML SELECT element. -->
<SELECT  ID = pbRATE  NAME = "pbRATE"  LANGUAGE="JScript"
         onChange="
                   /* Test whether playback rate can be set. */
                   if(Player.settings.IsAvailable('Rate'))

                   /* Set the playback rate based on the current
                      value of the SELECT element. */
                   Player.settings.rate = this.value
">

/* Create the OPTION list. */
<OPTION VALUE = 1>NORMAL</OPTION>
<OPTION VALUE = .5>half speed</OPTION>
<OPTION VALUE = 2>2 speed</OPTION>
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="6b8ef-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b8ef-134">Requirements</span></span>



| <span data-ttu-id="6b8ef-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b8ef-135">Requirement</span></span> | <span data-ttu-id="6b8ef-136">Wert</span><span class="sxs-lookup"><span data-stu-id="6b8ef-136">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6b8ef-137">Version</span><span class="sxs-lookup"><span data-stu-id="6b8ef-137">Version</span></span><br/> | <span data-ttu-id="6b8ef-138">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="6b8ef-138">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="6b8ef-139">DLL</span><span class="sxs-lookup"><span data-stu-id="6b8ef-139">DLL</span></span><br/>     | <dl> <span data-ttu-id="6b8ef-140"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b8ef-140"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b8ef-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b8ef-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b8ef-142">**Controls. FastForward**</span><span class="sxs-lookup"><span data-stu-id="6b8ef-142">**Controls.fastForward**</span></span>](controls-fastforward.md)
</dt> <dt>

[<span data-ttu-id="6b8ef-143">**Controls. fastreverse**</span><span class="sxs-lookup"><span data-stu-id="6b8ef-143">**Controls.fastReverse**</span></span>](controls-fastreverse.md)
</dt> <dt>

[<span data-ttu-id="6b8ef-144">**Einstellungs Objekt**</span><span class="sxs-lookup"><span data-stu-id="6b8ef-144">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="6b8ef-145">**Settings. IsAvailable**</span><span class="sxs-lookup"><span data-stu-id="6b8ef-145">**Settings.isAvailable**</span></span>](settings-isavailable.md)
</dt> </dl>

 

 





