---
title: Methode zum Anhalten von iwmpcontrols
description: Die Pause-Methode hält die Wiedergabe des Medien Elements an. | Methode zum Anhalten von iwmpcontrols
ms.assetid: 1d9ebaf3-84b4-458d-a393-2b685cd0dbfb
keywords:
- Windows-Media Player für die Methoden Pause
- Pause-Methode, Windows Media Player, iwmpcontrols-Schnittstelle
- Iwmpcontrols Interface, Windows Media Player, anhaltemethode
topic_type:
- apiref
api_name:
- IWMPControls.pause
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cf89cfef66c84be76a529d9c0cef6ec3ae6ac40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365647"
---
# <a name="iwmpcontrolspause-method"></a><span data-ttu-id="0282e-107">Iwmpcontrols::p ause-Methode</span><span class="sxs-lookup"><span data-stu-id="0282e-107">IWMPControls::pause method</span></span>

<span data-ttu-id="0282e-108">Die **Pause** -Methode hält die Wiedergabe des Medien Elements an.</span><span class="sxs-lookup"><span data-stu-id="0282e-108">The **pause** method pauses playback of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="0282e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0282e-109">Syntax</span></span>


```CSharp
public void pause();
```


```VB

Public Sub pause()
Implements IWMPControls.pause
```





## <a name="parameters"></a><span data-ttu-id="0282e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0282e-110">Parameters</span></span>

<span data-ttu-id="0282e-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0282e-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0282e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0282e-112">Return value</span></span>

<span data-ttu-id="0282e-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0282e-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0282e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0282e-114">Remarks</span></span>

<span data-ttu-id="0282e-115">Wenn eine Datei angehalten wird, gibt Windows Media Player keine Systemressourcen, z. b. das Audiogerät, aus.</span><span class="sxs-lookup"><span data-stu-id="0282e-115">When a file is paused, Windows Media Player does not give up any system resources, such as the audio device.</span></span>

<span data-ttu-id="0282e-116">Um zu ermitteln, ob ein bestimmter Medientyp angehalten werden kann, übergeben Sie den **System. String** -Wert "Pause" an die **iwmpcontrols. IsAvailable** -Eigenschaft (die **iwmpcontrols. get \_ IsAvailable** -Methode in c#).</span><span class="sxs-lookup"><span data-stu-id="0282e-116">To determine whether a particular media type can be paused, pass the **System.String** value "pause" to the **IWMPControls.isAvailable** property (the **IWMPControls.get\_isAvailable** method in C#).</span></span>

## <a name="examples"></a><span data-ttu-id="0282e-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0282e-117">Examples</span></span>

<span data-ttu-id="0282e-118">Im folgenden Beispiel wird **Pause** verwendet, um die Wiedergabe des aktuellen Medien Elements als Reaktion auf das Click-Ereignis einer Schaltfläche anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="0282e-118">The following example uses **pause** to pause playback of the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="0282e-119">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0282e-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void pauseButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("pause"))
    {
        controls.pause();
    }
}
```


```VB

Public Sub pauseButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles pauseButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;pause&quot;)) Then

        controls.pause()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="0282e-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0282e-120">Requirements</span></span>



| <span data-ttu-id="0282e-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0282e-121">Requirement</span></span> | <span data-ttu-id="0282e-122">Wert</span><span class="sxs-lookup"><span data-stu-id="0282e-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0282e-123">Version</span><span class="sxs-lookup"><span data-stu-id="0282e-123">Version</span></span><br/>   | <span data-ttu-id="0282e-124">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="0282e-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="0282e-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="0282e-125">Namespace</span></span><br/> | <span data-ttu-id="0282e-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="0282e-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="0282e-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="0282e-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0282e-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0282e-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0282e-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0282e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0282e-130">**Iwmpcontrols-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0282e-130">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0282e-131">**Iwmpcontrols. IsAvailable (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0282e-131">**IWMPControls.isAvailable (VB and C#)**</span></span>](iwmpcontrols-isavailable--vb-and-c.md)
</dt> </dl>

 

 





