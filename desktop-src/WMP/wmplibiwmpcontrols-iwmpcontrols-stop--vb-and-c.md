---
title: Methode zum Abbrechen von iwmpcontrols
description: Die Methode "beenden" beendet die Wiedergabe des Medien Elements. | Methode zum Abbrechen von iwmpcontrols
ms.assetid: 4be601af-6321-4115-a94d-cfc9228991cb
keywords:
- Windows-Media Player "Methode"
- Methode "Methode Media Player", "iwmpcontrols"-Schnittstelle
- Iwmpcontrols-Schnittstelle, Windows Media Player, Methode "Ende"
topic_type:
- apiref
api_name:
- IWMPControls.stop
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a73271098340ea0cf0a645472b5ef6333ae0f4b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371310"
---
# <a name="iwmpcontrolsstop-method"></a><span data-ttu-id="eca07-107">Iwmpcontrols:: End-Methode</span><span class="sxs-lookup"><span data-stu-id="eca07-107">IWMPControls::stop method</span></span>

<span data-ttu-id="eca07-108">Die Methode " **Beenden** " beendet die Wiedergabe des Medien Elements.</span><span class="sxs-lookup"><span data-stu-id="eca07-108">The **stop** method stops playback of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="eca07-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="eca07-109">Syntax</span></span>


```CSharp
public void stop();
```


```VB

Public Sub stop()
Implements IWMPControls.stop
```





## <a name="parameters"></a><span data-ttu-id="eca07-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="eca07-110">Parameters</span></span>

<span data-ttu-id="eca07-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="eca07-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eca07-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eca07-112">Return value</span></span>

<span data-ttu-id="eca07-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="eca07-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eca07-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eca07-114">Remarks</span></span>

<span data-ttu-id="eca07-115">Diese Methode bewirkt, dass Windows Media Player alle verwendeten Systemressourcen, z. b. das Audiogerät, freigibt.</span><span class="sxs-lookup"><span data-stu-id="eca07-115">This method causes Windows Media Player to release any system resources it is using, such as the audio device.</span></span> <span data-ttu-id="eca07-116">Das aktuelle Medien Element wird jedoch nicht freigegeben.</span><span class="sxs-lookup"><span data-stu-id="eca07-116">The current media item, however, is not released.</span></span>

<span data-ttu-id="eca07-117">Wenn Windows Media Player beendet wird, wird die aktuelle Wiedergabe Position im Medien Element auf den Anfang des Elements zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="eca07-117">When Windows Media Player is stopped, the current playback position in the media item is reset to the beginning of the item.</span></span> <span data-ttu-id="eca07-118">Wenn Sie anschließend **iwmpcontrols. Play** aufrufen, wird die Wiedergabe am Anfang des Medien Elements gestartet.</span><span class="sxs-lookup"><span data-stu-id="eca07-118">Subsequently calling **IWMPControls.play** will start playback from the beginning of the media item.</span></span> <span data-ttu-id="eca07-119">Verwenden Sie die **iwmpcontrols. Pause** -Methode, um einen Wiedergabe Vorgang anzuhalten, ohne die aktuelle Position zu ändern.</span><span class="sxs-lookup"><span data-stu-id="eca07-119">To halt a play operation without changing the current position, use the **IWMPControls.pause** method.</span></span>

## <a name="examples"></a><span data-ttu-id="eca07-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eca07-120">Examples</span></span>

<span data-ttu-id="eca07-121">Im folgenden Beispiel wird die Option zum Abbrechen des aktuellen Medien Elements als Reaktion auf das Click-Ereignis einer Schalt **Fläche verwendet.**</span><span class="sxs-lookup"><span data-stu-id="eca07-121">The following example uses **stop** to stop the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="eca07-122">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="eca07-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void stopButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("stop"))
    {
        controls.stop();
    }
}
```


```VB

Public Sub stopButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles stopButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;stop&quot;)) Then

        controls.stop()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="eca07-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eca07-123">Requirements</span></span>



| <span data-ttu-id="eca07-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eca07-124">Requirement</span></span> | <span data-ttu-id="eca07-125">Wert</span><span class="sxs-lookup"><span data-stu-id="eca07-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eca07-126">Version</span><span class="sxs-lookup"><span data-stu-id="eca07-126">Version</span></span><br/>   | <span data-ttu-id="eca07-127">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="eca07-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="eca07-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="eca07-128">Namespace</span></span><br/> | <span data-ttu-id="eca07-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="eca07-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="eca07-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="eca07-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="eca07-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="eca07-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eca07-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eca07-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eca07-133">**Iwmpcontrols-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="eca07-133">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="eca07-134">**Iwmpcontrols. Next (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="eca07-134">**IWMPControls.next (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="eca07-135">**Iwmpcontrols. Pause (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="eca07-135">**IWMPControls.pause (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="eca07-136">**Iwmpcontrols. Play (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="eca07-136">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="eca07-137">**Iwmpcontrols. Previous (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="eca07-137">**IWMPControls.previous (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)
</dt> </dl>

 

 





