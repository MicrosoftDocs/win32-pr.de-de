---
title: Iwmpcontrols FastForward-Methode
description: Die FastForward-Methode startet die schnelle Wiedergabe des Medien Elements in Vorwärtsrichtung. | Iwmpcontrols FastForward-Methode
ms.assetid: 44609d63-1d1a-489c-ac17-60b6d3ddc588
keywords:
- FastForward-Methoden Fenster Media Player
- FastForward-Methode, Windows Media Player, iwmpcontrols-Schnittstelle
- Iwmpcontrols-Schnittstelle, Windows Media Player, FastForward-Methode
topic_type:
- apiref
api_name:
- IWMPControls.fastForward
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1d99307a7b188b238157af62833273b8c724eab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370807"
---
# <a name="iwmpcontrolsfastforward-method"></a><span data-ttu-id="9dc06-107">Iwmpcontrols:: FastForward-Methode</span><span class="sxs-lookup"><span data-stu-id="9dc06-107">IWMPControls::fastForward method</span></span>

<span data-ttu-id="9dc06-108">Die **FastForward** -Methode startet die schnelle Wiedergabe des Medien Elements in Vorwärtsrichtung.</span><span class="sxs-lookup"><span data-stu-id="9dc06-108">The **fastForward** method starts fast play of the media item in the forward direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dc06-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9dc06-109">Syntax</span></span>


```CSharp
public void fastForward();
```


```VB

Public Sub fastForward()
Implements IWMPControls.fastForward
```





## <a name="parameters"></a><span data-ttu-id="9dc06-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9dc06-110">Parameters</span></span>

<span data-ttu-id="9dc06-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="9dc06-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9dc06-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9dc06-112">Return value</span></span>

<span data-ttu-id="9dc06-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9dc06-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dc06-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9dc06-114">Remarks</span></span>

<span data-ttu-id="9dc06-115">Die **FastForward** -Methode gibt den Clip um das Fünffache der normalen Geschwindigkeit wieder.</span><span class="sxs-lookup"><span data-stu-id="9dc06-115">The **fastForward** method plays the clip at five times the normal speed.</span></span> <span data-ttu-id="9dc06-116">Das Aufrufen von **FastForward** entspricht der Angabe von 5,0 für die Rate durch Festlegen der **iwmpsettings. Rate** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="9dc06-116">Calling **fastForward** is equivalent to specifying 5.0 for the rate by setting the **IWMPSettings.rate** property.</span></span> <span data-ttu-id="9dc06-117">Wenn die Rate anschließend geändert wird, oder wenn **iwmpcontrols. Play** oder **iwmpcontrols. Stop** aufgerufen wird, beendet Windows Media Player die schnelle Weiterleitung.</span><span class="sxs-lookup"><span data-stu-id="9dc06-117">If the rate is subsequently changed, or if **IWMPControls.play** or **IWMPControls.stop** is called, Windows Media Player will cease fast forwarding.</span></span>

<span data-ttu-id="9dc06-118">Die **FastForward** -Methode funktioniert nicht für Live-Übertragungen und bestimmte Medientypen.</span><span class="sxs-lookup"><span data-stu-id="9dc06-118">The **fastForward** method does not work for live broadcasts and certain media types.</span></span> <span data-ttu-id="9dc06-119">Um zu ermitteln, ob Sie sich in einem Clip schnell vorwärts bewegen können, übergeben Sie den **System. String** -Wert "FastForward" an die **iwmpcontrols. IsAvailable** -Eigenschaft (die **iwmpcontrols. get \_ IsAvailable** -Methode in c#).</span><span class="sxs-lookup"><span data-stu-id="9dc06-119">To determine whether you can fast forward in a clip, pass the **System.String** value "FastForward" to the **IWMPControls.isAvailable** property (the **IWMPControls.get\_isAvailable** method in C#).</span></span>

## <a name="examples"></a><span data-ttu-id="9dc06-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9dc06-120">Examples</span></span>

<span data-ttu-id="9dc06-121">Im folgenden Beispiel wird **FastForward** verwendet, um das aktuelle Medien Element in Reaktion auf das Click-Ereignis einer Schaltfläche schnell weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="9dc06-121">The following example uses **fastForward** to fast-forward the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="9dc06-122">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="9dc06-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void fastForwardButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("fastForward"))
    {
        controls.fastForward();
    }
}
```


```VB

Public Sub fastForwardButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fastForwardButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface. 
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;fastForward&quot;)) Then

        controls.fastForward()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="9dc06-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9dc06-123">Requirements</span></span>



| <span data-ttu-id="9dc06-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9dc06-124">Requirement</span></span> | <span data-ttu-id="9dc06-125">Wert</span><span class="sxs-lookup"><span data-stu-id="9dc06-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dc06-126">Version</span><span class="sxs-lookup"><span data-stu-id="9dc06-126">Version</span></span><br/>   | <span data-ttu-id="9dc06-127">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="9dc06-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="9dc06-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="9dc06-128">Namespace</span></span><br/> | <span data-ttu-id="9dc06-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="9dc06-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="9dc06-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="9dc06-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9dc06-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9dc06-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dc06-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9dc06-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dc06-133">**Iwmpcontrols-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="9dc06-133">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9dc06-134">**Iwmpcontrols. IsAvailable (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="9dc06-134">**IWMPControls.isAvailable (VB and C#)**</span></span>](iwmpcontrols-isavailable--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9dc06-135">**Iwmpcontrols. Play (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="9dc06-135">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9dc06-136">**Iwmpcontrols. Stopps (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="9dc06-136">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9dc06-137">**Iwmpsettings. Rate (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="9dc06-137">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





