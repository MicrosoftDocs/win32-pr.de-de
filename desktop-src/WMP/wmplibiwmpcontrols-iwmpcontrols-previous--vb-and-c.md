---
title: Iwmpcontrols Previous-Methode
description: Die vorherige Methode legt das vorherige Element in der Wiedergabeliste als Aktuelles Element fest.
ms.assetid: 380524f5-e8b6-45c4-9f6c-3dbb49b1ac9f
keywords:
- vorherige Methode, Windows Media Player
- vorherige Methode, Windows Media Player, iwmpcontrols-Schnittstelle
- Iwmpcontrols Interface, Windows Media Player, vorherige Methode
topic_type:
- apiref
api_name:
- IWMPControls.previous
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 823038205a026afb7141491f562698eb60515a5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370806"
---
# <a name="iwmpcontrolsprevious-method"></a><span data-ttu-id="a3de1-106">Iwmpcontrols::p revious-Methode</span><span class="sxs-lookup"><span data-stu-id="a3de1-106">IWMPControls::previous method</span></span>

<span data-ttu-id="a3de1-107">Die **vorherige** Methode legt das vorherige Element in der Wiedergabeliste als Aktuelles Element fest.</span><span class="sxs-lookup"><span data-stu-id="a3de1-107">The **previous** method sets the previous item in the playlist as the current item.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3de1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3de1-108">Syntax</span></span>


```CSharp
public void previous();
```


```VB

Public Sub previous()
Implements IWMPControls.previous
```





## <a name="parameters"></a><span data-ttu-id="a3de1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3de1-109">Parameters</span></span>

<span data-ttu-id="a3de1-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a3de1-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a3de1-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a3de1-111">Return value</span></span>

<span data-ttu-id="a3de1-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a3de1-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3de1-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3de1-113">Remarks</span></span>

<span data-ttu-id="a3de1-114">Wenn sich die Wiedergabeliste auf dem ersten Eintrag befindet, wenn **Previous** aufgerufen wird, wird der letzte Eintrag in der Wiedergabeliste zum aktuellen Eintrag.</span><span class="sxs-lookup"><span data-stu-id="a3de1-114">If the playlist is on the first entry when **previous** is invoked, the last entry in the playlist will become the current one.</span></span>

## <a name="examples"></a><span data-ttu-id="a3de1-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a3de1-115">Examples</span></span>

<span data-ttu-id="a3de1-116">Im folgenden Beispiel wird **verwendet,** um zum vorherigen Element in der aktuellen Wiedergabeliste als Reaktion auf das Click-Ereignis einer Schaltfläche zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="a3de1-116">The following example uses **previous** to move to the previous item in the current playlist in response to the Click event of a button.</span></span> <span data-ttu-id="a3de1-117">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a3de1-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void previousButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("previous"))
    {
        controls.previous();
    }
}
```


```VB

Public Sub previousButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles previousButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;previous&quot;)) Then

        controls.previous()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="a3de1-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3de1-118">Requirements</span></span>



| <span data-ttu-id="a3de1-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3de1-119">Requirement</span></span> | <span data-ttu-id="a3de1-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a3de1-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3de1-121">Version</span><span class="sxs-lookup"><span data-stu-id="a3de1-121">Version</span></span><br/>   | <span data-ttu-id="a3de1-122">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="a3de1-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a3de1-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="a3de1-123">Namespace</span></span><br/> | <span data-ttu-id="a3de1-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a3de1-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a3de1-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="a3de1-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a3de1-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a3de1-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3de1-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3de1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3de1-128">**Iwmpcontrols-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="a3de1-128">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a3de1-129">**Iwmpcontrols. Next (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="a3de1-129">**IWMPControls.next (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a3de1-130">**Iwmpcontrols. Stopps (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="a3de1-130">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> </dl>

 

 





