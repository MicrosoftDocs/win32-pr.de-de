---
title: Iwmpcontrols CurrentPosition (Eigenschaft)
description: Die CurrentPosition-Eigenschaft ruft die aktuelle Position im Medien Element in Sekunden ab oder legt diese fest.
ms.assetid: 48f5241e-7528-485e-bf47-d655ba842af2
keywords:
- CurrentPosition-Eigenschaft, Fenster Media Player
- CurrentPosition-Eigenschaft, Windows Media Player, iwmpcontrols-Schnittstelle
- Iwmpcontrols Interface, Windows Media Player, CurrentPosition (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPControls.currentPosition
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fee8c2c8244d6034069f21033978ce2883ff852d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370808"
---
# <a name="iwmpcontrolscurrentposition-property"></a><span data-ttu-id="a2298-106">Iwmpcontrols:: CurrentPosition (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a2298-106">IWMPControls::currentPosition property</span></span>

<span data-ttu-id="a2298-107">Die **CurrentPosition** -Eigenschaft ruft die aktuelle Position im Medien Element in Sekunden ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="a2298-107">The **currentPosition** property gets or sets the current position in the media item in seconds from the beginning.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2298-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2298-108">Syntax</span></span>


```CSharp
public System.Double currentPosition {get; set;}
```


```VB

Public Property currentPosition As System.Double
```





## <a name="property-value"></a><span data-ttu-id="a2298-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a2298-109">Property value</span></span>

<span data-ttu-id="a2298-110">Ein **System. Double** -Wert, der die aktuelle Position ist.</span><span class="sxs-lookup"><span data-stu-id="a2298-110">A **System.Double** that is the current position.</span></span>

## <a name="examples"></a><span data-ttu-id="a2298-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a2298-111">Examples</span></span>

<span data-ttu-id="a2298-112">Im folgenden Beispiel wird **CurrentPosition** verwendet, um eine vom Benutzer bereitgestellte Position zu suchen.</span><span class="sxs-lookup"><span data-stu-id="a2298-112">The following example uses **currentPosition** to seek to a position provided by the user.</span></span> <span data-ttu-id="a2298-113">Als Reaktion auf einen Klick auf eine Schaltfläche wird **CurrentPosition** auf den Wert festgelegt, der in einem Textfeld mit dem Namen newPosition eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="a2298-113">In response to a button click, **currentPosition** is set to the value entered in a text box called newPosition.</span></span> <span data-ttu-id="a2298-114">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a2298-114">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setPosition_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Set the current position of the media item to the position entered by the user.
    player.Ctlcontrols.currentPosition = Convert.ToDouble(newPosition.Text);
}
```


```VB

Public Sub setPosition_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setPosition.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Set the current position of the media item to the position entered by the user.
    player.Ctlcontrols.currentPosition = Convert.ToDouble(newPosition.Text)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="a2298-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2298-115">Requirements</span></span>



| <span data-ttu-id="a2298-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2298-116">Requirement</span></span> | <span data-ttu-id="a2298-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a2298-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2298-118">Version</span><span class="sxs-lookup"><span data-stu-id="a2298-118">Version</span></span><br/>   | <span data-ttu-id="a2298-119">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="a2298-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a2298-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="a2298-120">Namespace</span></span><br/> | <span data-ttu-id="a2298-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a2298-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a2298-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="a2298-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a2298-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a2298-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2298-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2298-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2298-125">**Iwmpcontrols-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="a2298-125">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a2298-126">**Iwmpcontrols. currentpositionstring (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="a2298-126">**IWMPControls.currentPositionString (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentpositionstring--vb-and-c.md)
</dt> </dl>

 

 





