---
title: Wiedergabemethode von iwmpcontrols
description: Die Play-Methode beginnt mit der Wiedergabe des aktuellen Medien Elements oder nimmt die Wiedergabe eines angehaltenen Elements wieder auf.
ms.assetid: 02e00df6-4dc1-44bb-9826-e69e8298ccaa
keywords:
- Wiedergabemethode Windows Media Player
- Wiedergabemethode, Windows Media Player, iwmpcontrols-Schnittstelle
- Iwmpcontrols Interface, Windows Media Player, Play-Methode
topic_type:
- apiref
api_name:
- IWMPControls.play
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fd87a2e2ba3d53b119df328fa68668c91c78d6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369246"
---
# <a name="iwmpcontrolsplay-method"></a><span data-ttu-id="54c93-106">Iwmpcontrols::p Lay-Methode</span><span class="sxs-lookup"><span data-stu-id="54c93-106">IWMPControls::play method</span></span>

<span data-ttu-id="54c93-107">Die **Play** -Methode beginnt mit der Wiedergabe des aktuellen Medien Elements oder nimmt die Wiedergabe eines angehaltenen Elements wieder auf.</span><span class="sxs-lookup"><span data-stu-id="54c93-107">The **play** method begins playback of the current media item, or resumes playback of a paused item.</span></span>

## <a name="syntax"></a><span data-ttu-id="54c93-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="54c93-108">Syntax</span></span>


```CSharp
public void play();
```


```VB

Public Sub play()
Implements IWMPControls.play
```





## <a name="parameters"></a><span data-ttu-id="54c93-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="54c93-109">Parameters</span></span>

<span data-ttu-id="54c93-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="54c93-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="54c93-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54c93-111">Return value</span></span>

<span data-ttu-id="54c93-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="54c93-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="54c93-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54c93-113">Remarks</span></span>

<span data-ttu-id="54c93-114">Wenn diese Methode während der schnellen Weiterleitung oder rebuggen aufgerufen wird, wird die Wiederholungsrate (der Wert von **iwmpsettings. Rate**) auf 1,0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="54c93-114">If this method is called while fast-forwarding or rewinding, the rate of playback (the value of **IWMPSettings.rate**) is set to 1.0.</span></span>

## <a name="examples"></a><span data-ttu-id="54c93-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="54c93-115">Examples</span></span>

<span data-ttu-id="54c93-116">Im folgenden Beispiel wird **Play** verwendet, um das aktuelle Medien Element als Reaktion auf das Click-Ereignis einer Schaltfläche wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="54c93-116">The following example uses **play** to play the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="54c93-117">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="54c93-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("play"))
    {
        controls.play();
    }
}
```


```VB

Public Sub playButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;play&quot;)) Then

        controls.play()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="54c93-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54c93-118">Requirements</span></span>



| <span data-ttu-id="54c93-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54c93-119">Requirement</span></span> | <span data-ttu-id="54c93-120">Wert</span><span class="sxs-lookup"><span data-stu-id="54c93-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54c93-121">Version</span><span class="sxs-lookup"><span data-stu-id="54c93-121">Version</span></span><br/>   | <span data-ttu-id="54c93-122">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="54c93-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="54c93-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="54c93-123">Namespace</span></span><br/> | <span data-ttu-id="54c93-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="54c93-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="54c93-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="54c93-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="54c93-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="54c93-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54c93-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54c93-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54c93-128">**Iwmpcontrols-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="54c93-128">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="54c93-129">**Iwmpcontrols. PlayItem (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="54c93-129">**IWMPControls.playItem (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-playitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="54c93-130">**Iwmpsettings. Rate (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="54c93-130">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





