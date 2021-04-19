---
title: Iwmpcontrols. IsAvailable (VB und C)
description: Die IsAvailable-Eigenschaft (die get \_ IsAvailable-Methode in C \) Ruft einen Wert ab, der angibt, ob ein angegebener Informationstyp verfügbar ist oder eine bestimmte Aktion ausgeführt werden kann.
ms.assetid: 00812d5c-513e-49d5-93ba-750b81a852dd
keywords:
- Iwmpcontrols. IsAvailable (VB und C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPControls.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0d5d9ffcd6cad6eefb7cdff25fd2cf34b76ccc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370092"
---
# <a name="iwmpcontrolsisavailable-vb-and-c"></a><span data-ttu-id="2b6a9-104">Iwmpcontrols. IsAvailable (VB und c#)</span><span class="sxs-lookup"><span data-stu-id="2b6a9-104">IWMPControls.isAvailable (VB and C#)</span></span>

<span data-ttu-id="2b6a9-105">Mit der **IsAvailable** -Eigenschaft (der **get \_ IsAvailable** -Methode in c#) wird ein Wert abgerufen, der angibt, ob ein angegebener Informationstyp verfügbar ist oder eine angegebene Aktion ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="2b6a9-105">The **isAvailable** property (the **get\_isAvailable** method in C#) gets a value indicating whether a specified type of information is available or a specified action can be performed.</span></span>


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
bool get_isAvailable (
  System.String bstrItem
);
```



## <a name="parameters"></a><span data-ttu-id="2b6a9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b6a9-106">Parameters</span></span>

<span data-ttu-id="2b6a9-107">*bstritem*</span><span class="sxs-lookup"><span data-stu-id="2b6a9-107">*bstrItem*</span></span>

<span data-ttu-id="2b6a9-108">Ein System. String-Wert, der einem der folgenden Werte entspricht.</span><span class="sxs-lookup"><span data-stu-id="2b6a9-108">A System.String that is one of the following values.</span></span>



| <span data-ttu-id="2b6a9-109">Wert</span><span class="sxs-lookup"><span data-stu-id="2b6a9-109">Value</span></span>           | <span data-ttu-id="2b6a9-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b6a9-110">Description</span></span>                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b6a9-111">currentItem</span><span class="sxs-lookup"><span data-stu-id="2b6a9-111">currentItem</span></span>     | <span data-ttu-id="2b6a9-112">Ermittelt, ob der Benutzer die **iwmpcontrols. accesstitem** -Eigenschaft festlegen kann.</span><span class="sxs-lookup"><span data-stu-id="2b6a9-112">Discovers whether the user can set the **IWMPControls.currentItem** property.</span></span>                                                                                     |
| <span data-ttu-id="2b6a9-113">currentmarker</span><span class="sxs-lookup"><span data-stu-id="2b6a9-113">currentMarker</span></span>   | <span data-ttu-id="2b6a9-114">Ermittelt, ob der Benutzer einen bestimmten Marker suchen kann.</span><span class="sxs-lookup"><span data-stu-id="2b6a9-114">Discovers whether the user can seek to a specific marker.</span></span>                                                                                                         |
| <span data-ttu-id="2b6a9-115">CurrentPosition</span><span class="sxs-lookup"><span data-stu-id="2b6a9-115">currentPosition</span></span> | <span data-ttu-id="2b6a9-116">Ermittelt, ob der Benutzer eine bestimmte Position in der Datei suchen kann.</span><span class="sxs-lookup"><span data-stu-id="2b6a9-116">Discovers whether the user can seek to a specific position in the file.</span></span> <span data-ttu-id="2b6a9-117">Einige Dateien unterstützen keine Suchvorgänge.</span><span class="sxs-lookup"><span data-stu-id="2b6a9-117">Some files do not support seeking.</span></span>                                                        |
| <span data-ttu-id="2b6a9-118">FastForward</span><span class="sxs-lookup"><span data-stu-id="2b6a9-118">fastForward</span></span>     | <span data-ttu-id="2b6a9-119">Ermittelt, ob die Datei eine schnelle Weiterleitung unterstützt und ob diese Funktion aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="2b6a9-119">Discovers whether the file supports fast forwarding and whether that functionality can be invoked.</span></span> <span data-ttu-id="2b6a9-120">FastForward wird von vielen Dateitypen (und Livestreams) nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2b6a9-120">Many file types (and live streams) do not support fastForward.</span></span> |
| <span data-ttu-id="2b6a9-121">fastreverse</span><span class="sxs-lookup"><span data-stu-id="2b6a9-121">fastReverse</span></span>     | <span data-ttu-id="2b6a9-122">Ermittelt, ob die Datei fastreverse unterstützt und ob diese Funktion aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="2b6a9-122">Discovers whether the file supports fastReverse and whether that functionality can be invoked.</span></span> <span data-ttu-id="2b6a9-123">Fastreverse wird von vielen Dateitypen (und Livestreams) nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2b6a9-123">Many file types (and live streams) do not support fastReverse.</span></span>     |
| <span data-ttu-id="2b6a9-124">Weiter</span><span class="sxs-lookup"><span data-stu-id="2b6a9-124">next</span></span>            | <span data-ttu-id="2b6a9-125">Ermittelt, ob der Benutzer den nächsten Eintrag in einer Wiedergabeliste suchen kann.</span><span class="sxs-lookup"><span data-stu-id="2b6a9-125">Discovers whether the user can seek to the next entry in a playlist.</span></span>                                                                                              |
| <span data-ttu-id="2b6a9-126">pause</span><span class="sxs-lookup"><span data-stu-id="2b6a9-126">pause</span></span>           | <span data-ttu-id="2b6a9-127">Ermittelt, ob die **iwmpcontrols. Pause** -Methode verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="2b6a9-127">Discovers whether the **IWMPControls.pause** method is available.</span></span>                                                                                                 |
| <span data-ttu-id="2b6a9-128">Theater</span><span class="sxs-lookup"><span data-stu-id="2b6a9-128">play</span></span>            | <span data-ttu-id="2b6a9-129">Ermittelt, ob die **iwmpcontrols. Play** -Methode verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="2b6a9-129">Discovers whether the **IWMPControls.play** method is available.</span></span>                                                                                                  |
| <span data-ttu-id="2b6a9-130">Vorherige</span><span class="sxs-lookup"><span data-stu-id="2b6a9-130">previous</span></span>        | <span data-ttu-id="2b6a9-131">Ermittelt, ob der Benutzer den vorherigen Eintrag in einer Wiedergabeliste suchen kann.</span><span class="sxs-lookup"><span data-stu-id="2b6a9-131">Discovers whether the user can seek to the previous entry in a playlist.</span></span>                                                                                          |
| <span data-ttu-id="2b6a9-132">Schritt</span><span class="sxs-lookup"><span data-stu-id="2b6a9-132">step</span></span>            | <span data-ttu-id="2b6a9-133">Ermittelt, ob die **IWMPControls2. Step** -Methode während der Wiedergabe verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="2b6a9-133">Discovers whether the **IWMPControls2.step** method is available during playback.</span></span>                                                                                 |
| <span data-ttu-id="2b6a9-134">stop</span><span class="sxs-lookup"><span data-stu-id="2b6a9-134">stop</span></span>            | <span data-ttu-id="2b6a9-135">Ermittelt, ob die **iwmpcontrols.** End-Methode verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="2b6a9-135">Discovers whether the **IWMPControls.stop** method is available.</span></span>                                                                                                  |



 

## <a name="property-value"></a><span data-ttu-id="2b6a9-136">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2b6a9-136">Property Value</span></span>

<span data-ttu-id="2b6a9-137">**System.Boolean**</span><span class="sxs-lookup"><span data-stu-id="2b6a9-137">**System.Boolean**</span></span>

<span data-ttu-id="2b6a9-138">Ein **System. boolescher** Wert, der angibt, ob ein angegebener Informationstyp verfügbar ist oder eine bestimmte Aktion ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="2b6a9-138">A **System.Boolean** that indicates whether a specified type of information is available or a specified action can be performed.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b6a9-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b6a9-139">Remarks</span></span>

<span data-ttu-id="2b6a9-140">**Iwmpcontrols. IsAvailable** ist eine Eigenschaft in Visual Basic, die einen-Parameter annimmt.</span><span class="sxs-lookup"><span data-stu-id="2b6a9-140">**IWMPControls.isAvailable** is a property in Visual Basic that takes a parameter.</span></span> <span data-ttu-id="2b6a9-141">In c# wird dies als **iwmpcontrols. get \_ IsAvailable** -Methode bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2b6a9-141">In C# it is referred to as the **IWMPControls.get\_isAvailable** method.</span></span>

## <a name="examples"></a><span data-ttu-id="2b6a9-142">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2b6a9-142">Examples</span></span>

<span data-ttu-id="2b6a9-143">Im folgenden Beispiel wird die **IsAvailable** -Eigenschaft (die **get \_ IsAvailable** -Methode in c#) verwendet, um zu überprüfen, ob das aktuelle Medien Element die **CurrentPosition** -Eigenschaft unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2b6a9-143">The following example uses the **isAvailable** property (the **get\_isAvailable** method in C#) to verify that the current media item supports the **currentPosition** property.</span></span> <span data-ttu-id="2b6a9-144">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2b6a9-144">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// If the currentPosition property is supported, seek to position 0.
if (player.Ctlcontrols.get_isAvailable("currentPosition"))
{
    player.Ctlcontrols.currentPosition = 0;
}
```


```VB

' If the currentPosition property is supported, seek to position 0.
If (player.Ctlcontrols.isAvailable(&quot;currentPosition&quot;)) Then

    player.Ctlcontrols.currentPosition = 0

End If
```





## <a name="requirements"></a><span data-ttu-id="2b6a9-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b6a9-145">Requirements</span></span>



| <span data-ttu-id="2b6a9-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b6a9-146">Requirement</span></span> | <span data-ttu-id="2b6a9-147">Wert</span><span class="sxs-lookup"><span data-stu-id="2b6a9-147">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b6a9-148">Version</span><span class="sxs-lookup"><span data-stu-id="2b6a9-148">Version</span></span><br/>   | <span data-ttu-id="2b6a9-149">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="2b6a9-149">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2b6a9-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="2b6a9-150">Namespace</span></span><br/> | <span data-ttu-id="2b6a9-151">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="2b6a9-151">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2b6a9-152">Assembly</span><span class="sxs-lookup"><span data-stu-id="2b6a9-152">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2b6a9-153"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2b6a9-153"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b6a9-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b6a9-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b6a9-155">**Iwmpcontrols-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2b6a9-155">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2b6a9-156">**Iwmpcontrols. Currency Item (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2b6a9-156">**IWMPControls.currentItem (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2b6a9-157">**Iwmpcontrols. Pause (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2b6a9-157">**IWMPControls.pause (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2b6a9-158">**Iwmpcontrols. Play (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2b6a9-158">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2b6a9-159">**Iwmpcontrols. Stopps (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2b6a9-159">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2b6a9-160">**IWMPControls2. Step (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2b6a9-160">**IWMPControls2.step (VB and C#)**</span></span>](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md)
</dt> </dl>

 

 





