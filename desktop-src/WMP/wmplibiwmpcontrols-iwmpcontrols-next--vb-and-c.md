---
title: Iwmpcontrols Next-Methode
description: Die Next-Methode legt das nächste Element in der Wiedergabeliste als Aktuelles Element fest.
ms.assetid: 3f82ef25-a1e0-4845-b0ed-dd6463719577
keywords:
- nächste Methode, Windows Media Player
- nächste Methode, Windows Media Player, iwmpcontrols-Schnittstelle
- Iwmpcontrols Interface, Windows Media Player, nächste Methode
topic_type:
- apiref
api_name:
- IWMPControls.next
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8444ba7d9209759cb64c4b582e1af9d074332ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373971"
---
# <a name="iwmpcontrolsnext-method"></a><span data-ttu-id="182c3-106">Iwmpcontrols:: Next-Methode</span><span class="sxs-lookup"><span data-stu-id="182c3-106">IWMPControls::next method</span></span>

<span data-ttu-id="182c3-107">Die **Next** -Methode legt das nächste Element in der Wiedergabeliste als Aktuelles Element fest.</span><span class="sxs-lookup"><span data-stu-id="182c3-107">The **next** method sets the next item in the playlist as the current item.</span></span>

## <a name="syntax"></a><span data-ttu-id="182c3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="182c3-108">Syntax</span></span>


```CSharp
public void next();
```


```VB

Public Sub next()
Implements IWMPControls.next
```





## <a name="parameters"></a><span data-ttu-id="182c3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="182c3-109">Parameters</span></span>

<span data-ttu-id="182c3-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="182c3-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="182c3-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="182c3-111">Return value</span></span>

<span data-ttu-id="182c3-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="182c3-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="182c3-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="182c3-113">Remarks</span></span>

<span data-ttu-id="182c3-114">Wenn sich die Wiedergabeliste auf dem letzten Eintrag befindet, wenn **Next** aufgerufen wird, wird der erste Eintrag in der Wiedergabeliste zum aktuellen Eintrag.</span><span class="sxs-lookup"><span data-stu-id="182c3-114">If the playlist is on the last entry when **next** is invoked, the first entry in the playlist will become the current one.</span></span>

<span data-ttu-id="182c3-115">Bei serverseitigen Wiedergabelisten springt diese Methode zum nächsten Element in der serverseitigen Wiedergabeliste, nicht zur Client Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="182c3-115">For server-side playlists, this method skips to the next item in the server-side playlist, not the client playlist.</span></span>

<span data-ttu-id="182c3-116">Beim Abspielen einer DVD überspringt diese Methode das nächste logische Kapitel in der Wiedergabe Sequenz, das möglicherweise nicht das nächste Kapitel in der Wiedergabeliste ist.</span><span class="sxs-lookup"><span data-stu-id="182c3-116">When playing a DVD, this method skips to the next logical chapter in the playback sequence, which may not be the next chapter in the playlist.</span></span> <span data-ttu-id="182c3-117">Bei der Wiedergabe von DVD-Bildern wird diese Methode zum nächsten Bild überspringt.</span><span class="sxs-lookup"><span data-stu-id="182c3-117">When playing DVD still images, this method skips to the next image.</span></span>

## <a name="examples"></a><span data-ttu-id="182c3-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="182c3-118">Examples</span></span>

<span data-ttu-id="182c3-119">Im folgenden Beispiel wird als Reaktion auf das Click-Ereignis einer Schaltfläche **als nächstes** verwendet, um zum nächsten Element in der aktuellen Wiedergabeliste zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="182c3-119">The following example uses **next** to move to the next item in the current playlist in response to the Click event of a button.</span></span> <span data-ttu-id="182c3-120">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="182c3-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void nextButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("next"))
    {
        controls.next();
    }
}
```


```VB

Public Sub nextButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles nextButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;next&quot;)) Then

        controls.next()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="182c3-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="182c3-121">Requirements</span></span>



| <span data-ttu-id="182c3-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="182c3-122">Requirement</span></span> | <span data-ttu-id="182c3-123">Wert</span><span class="sxs-lookup"><span data-stu-id="182c3-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="182c3-124">Version</span><span class="sxs-lookup"><span data-stu-id="182c3-124">Version</span></span><br/>   | <span data-ttu-id="182c3-125">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="182c3-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="182c3-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="182c3-126">Namespace</span></span><br/> | <span data-ttu-id="182c3-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="182c3-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="182c3-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="182c3-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="182c3-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="182c3-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="182c3-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="182c3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="182c3-131">**Iwmpcontrols-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="182c3-131">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="182c3-132">**Iwmpcontrols. Previous (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="182c3-132">**IWMPControls.previous (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="182c3-133">**Iwmpcontrols. Stopps (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="182c3-133">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> </dl>

 

 





