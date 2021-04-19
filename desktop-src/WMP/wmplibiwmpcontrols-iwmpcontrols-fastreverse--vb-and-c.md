---
title: Iwmpcontrols fastreverse-Methode
description: Die fastreverse-Methode startet die schnelle Wiedergabe des Medien Elements in umgekehrter Richtung.
ms.assetid: 5c872e8d-2ffc-425f-a4dd-938ddd1426e0
keywords:
- fastreverse-Methode, Windows-Media Player
- fastreverse-Methode, Windows Media Player, iwmpcontrols-Schnittstelle
- Iwmpcontrols Interface, Windows Media Player, fastreverse-Methode
topic_type:
- apiref
api_name:
- IWMPControls.fastReverse
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7061481aea13b0ed83c3a3d0eb47ca24b940358b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361472"
---
# <a name="iwmpcontrolsfastreverse-method"></a><span data-ttu-id="1665b-106">Iwmpcontrols:: fastreverse-Methode</span><span class="sxs-lookup"><span data-stu-id="1665b-106">IWMPControls::fastReverse method</span></span>

<span data-ttu-id="1665b-107">Die **fastreverse** -Methode startet die schnelle Wiedergabe des Medien Elements in umgekehrter Richtung.</span><span class="sxs-lookup"><span data-stu-id="1665b-107">The **fastReverse** method starts fast play of the media item in the reverse direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="1665b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1665b-108">Syntax</span></span>


```CSharp
public void fastReverse();
```


```VB

Public Sub fastReverse()
Implements IWMPControls.fastReverse
```





## <a name="parameters"></a><span data-ttu-id="1665b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1665b-109">Parameters</span></span>

<span data-ttu-id="1665b-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="1665b-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1665b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1665b-111">Return value</span></span>

<span data-ttu-id="1665b-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1665b-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1665b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1665b-113">Remarks</span></span>

<span data-ttu-id="1665b-114">Die **fastreverse** -Methode scannt den Clip in umgekehrter Reihenfolge mit dem fünfmal normalen Tempo und zeigt nur die Keyframes an, wenn es sich um eine Videodatei handelt.</span><span class="sxs-lookup"><span data-stu-id="1665b-114">The **fastReverse** method scans the clip in reverse at five times the normal speed, displaying only the key frames if it is a video file.</span></span> <span data-ttu-id="1665b-115">Das Aufrufen von **fastreverse** entspricht der Angabe von-5,0 für die Rate durch Festlegen der **iwmpsettings. Rate** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1665b-115">Calling **fastReverse** is equivalent to specifying -5.0 for the rate by setting the **IWMPSettings.rate** property.</span></span> <span data-ttu-id="1665b-116">Wenn die Rate anschließend geändert wird, oder wenn **iwmpcontrols. Play** oder **iwmpcontrols. Stop** aufgerufen wird, wird Windows Media Player schnell umkehren.</span><span class="sxs-lookup"><span data-stu-id="1665b-116">If the rate is subsequently changed, or if **IWMPControls.play** or **IWMPControls.stop** is called, Windows Media Player will cease fast reverse.</span></span>

<span data-ttu-id="1665b-117">Wenn das Element Teil einer Wiedergabeliste ist, wird **fastreverse** am Anfang der aktuellen Spur angehalten. Wenn sich beispielsweise Track 3 in **fastreverse** befindet und der Anfang von Track 3 erreicht wird, wechselt Windows Media Player nicht mehr zu Track 2.</span><span class="sxs-lookup"><span data-stu-id="1665b-117">If the item is part of a playlist, **fastReverse** stops at the beginning of the current track. For instance, if track 3 is in **fastReverse**, when the beginning of track 3 is reached, Windows Media Player will not go to track 2.</span></span> <span data-ttu-id="1665b-118">Die Wiedergabe Anzahl wird beim Aufrufen von **fastreverse** nicht inkrementiert.</span><span class="sxs-lookup"><span data-stu-id="1665b-118">The play count is not incremented when calling **fastReverse**.</span></span>

<span data-ttu-id="1665b-119">Wenn Sie beim Ausführen von **fastreverse** **iwmpcontrols. FastForward** aufzurufen, wird **fastreverse** angehalten, und **iwmpcontrols. FastForward** wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="1665b-119">If you call **IWMPControls.fastForward** while **fastReverse** is running, **fastReverse** will be stopped and **IWMPControls.fastForward** will begin.</span></span>

<span data-ttu-id="1665b-120">Diese Methode funktioniert nicht für Live Übertragungen und bestimmte digitale Medientypen.</span><span class="sxs-lookup"><span data-stu-id="1665b-120">This method does not work for live broadcasts and certain digital media types.</span></span> <span data-ttu-id="1665b-121">Um zu ermitteln, ob Sie in einem Clip fast Reverse verwenden können, übergeben Sie den **System. String** -Wert "fastreverse" an die **iwmpcontrols. IsAvailable** -Eigenschaft (die **iwmpcontrols. get \_ IsAvailable** -Methode in c#).</span><span class="sxs-lookup"><span data-stu-id="1665b-121">To determine whether you can use fast reverse in a clip, pass the **System.String** value "FastReverse" to the **IWMPControls.isAvailable** property (the **IWMPControls.get\_isAvailable** method in C#).</span></span>

## <a name="examples"></a><span data-ttu-id="1665b-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1665b-122">Examples</span></span>

<span data-ttu-id="1665b-123">Im folgenden Beispiel wird **fastreverse** verwendet, um das aktuelle Medien Element als Reaktion auf das Click-Ereignis einer Schaltfläche umzukehren.</span><span class="sxs-lookup"><span data-stu-id="1665b-123">The following example uses **fastReverse** to reverse the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="1665b-124">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1665b-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void fastReverseButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("fastReverse"))
    {
        controls.fastReverse();
    }
}
```


```VB

Public Sub fastReverseButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fastReverseButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;fastReverse&quot;)) Then

        controls.fastReverse()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="1665b-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1665b-125">Requirements</span></span>



| <span data-ttu-id="1665b-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1665b-126">Requirement</span></span> | <span data-ttu-id="1665b-127">Wert</span><span class="sxs-lookup"><span data-stu-id="1665b-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1665b-128">Version</span><span class="sxs-lookup"><span data-stu-id="1665b-128">Version</span></span><br/>   | <span data-ttu-id="1665b-129">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="1665b-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="1665b-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="1665b-130">Namespace</span></span><br/> | <span data-ttu-id="1665b-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="1665b-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="1665b-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="1665b-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1665b-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1665b-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1665b-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1665b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1665b-135">**Iwmpcontrols-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="1665b-135">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1665b-136">**Iwmpcontrols. FastForward (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="1665b-136">**IWMPControls.fastForward (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1665b-137">**Iwmpcontrols. IsAvailable (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="1665b-137">**IWMPControls.isAvailable (VB and C#)**</span></span>](iwmpcontrols-isavailable--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1665b-138">**Iwmpcontrols. Play (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="1665b-138">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1665b-139">**Iwmpcontrols. Stopps (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="1665b-139">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1665b-140">**Iwmpsettings. Rate (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="1665b-140">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





