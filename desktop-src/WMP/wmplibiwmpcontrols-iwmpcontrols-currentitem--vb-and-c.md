---
title: Eigenschaften von iwmpcontrols-Eigenschaften
description: Mit der Eigenschaft "ustitem" wird das aktuelle Medien Element in einer Wiedergabeliste abgerufen oder festgelegt.
ms.assetid: 0a331b1f-95bd-48ea-b951-1ca35cc96865
keywords:
- Eigenschaften Fenster für "Eigenschaften" Media Player
- Eigenschaft "Eigenschaften" Windows Media Player, iwmpcontrols-Schnittstelle
- Iwmpcontrols Interface, Windows Media Player, Eigenschaft "Impact Item"
topic_type:
- apiref
api_name:
- IWMPControls.currentItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aae04eb333e2fd347fa6f88b33ec2482a4dd8fd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358750"
---
# <a name="iwmpcontrolscurrentitem-property"></a><span data-ttu-id="7d0c6-106">Iwmpcontrols:: accesstitem (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7d0c6-106">IWMPControls::currentItem property</span></span>

<span data-ttu-id="7d0c6-107">Mit der Eigenschaft " **ustitem** " wird das aktuelle Medien Element in einer Wiedergabeliste abgerufen oder festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7d0c6-107">The **currentItem** property gets or sets the current media item in a playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d0c6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d0c6-108">Syntax</span></span>


```CSharp
public IWMPMedia currentItem {get; set;}
```


```VB

Public Property currentItem As IWMPMedia
```





## <a name="property-value"></a><span data-ttu-id="7d0c6-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7d0c6-109">Property value</span></span>

<span data-ttu-id="7d0c6-110">Eine **WMPLib. iwmpmedia** -Schnittstelle, die das Medien Element darstellt.</span><span class="sxs-lookup"><span data-stu-id="7d0c6-110">A **WMPLib.IWMPMedia** interface that represents the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d0c6-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d0c6-111">Remarks</span></span>

<span data-ttu-id="7d0c6-112">Diese Eigenschaft funktioniert nur mit Elementen in der aktuellen Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="7d0c6-112">This property works only with items in the current playlist.</span></span> <span data-ttu-id="7d0c6-113">Das Festlegen von " **ustitem** " auf die Schnittstelle eines gespeicherten Medien Elements wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7d0c6-113">Setting **currentItem** to the interface of a saved media item is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="7d0c6-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7d0c6-114">Examples</span></span>

<span data-ttu-id="7d0c6-115">Im folgenden Beispiel wird das aktuelle Medien Element des Players mithilfe von " **ustitem** " auf ein aus einem Listenfeld ausgewähltes Element festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7d0c6-115">The following example uses **currentItem** to set the player's current media item to an item selected from a list box.</span></span> <span data-ttu-id="7d0c6-116">Das Listenfeld wurde mit allen Elementen in der aktuellen Wiedergabeliste gefüllt.</span><span class="sxs-lookup"><span data-stu-id="7d0c6-116">The list box has been filled with all of the items in the current playlist.</span></span> <span data-ttu-id="7d0c6-117">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7d0c6-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playItem_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    int selectedItem = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    // Ensure that the previous media item is stopped.
    player.Ctlcontrols.stop();

    // Set the current item to the item selected from the list box.
    player.Ctlcontrols.currentItem = player.currentPlaylist.get_Item(selectedItem);
    
    // Play the current item.
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playItem_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles playItem.SelectedIndexChanged

    Dim lb As System.Windows.Forms.ListBox = sender
    Dim selectedItem As Integer = lb.SelectedIndex

    &#39; Ensure that the previous media item is stopped.
    player.Ctlcontrols.stop()

    &#39; Set the current item to the item selected from the list box.
    player.Ctlcontrols.currentItem = player.currentPlaylist.Item(selectedItem)

    &#39; Play the current item.
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="7d0c6-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d0c6-118">Requirements</span></span>



| <span data-ttu-id="7d0c6-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d0c6-119">Requirement</span></span> | <span data-ttu-id="7d0c6-120">Wert</span><span class="sxs-lookup"><span data-stu-id="7d0c6-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d0c6-121">Version</span><span class="sxs-lookup"><span data-stu-id="7d0c6-121">Version</span></span><br/>   | <span data-ttu-id="7d0c6-122">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="7d0c6-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="7d0c6-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="7d0c6-123">Namespace</span></span><br/> | <span data-ttu-id="7d0c6-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="7d0c6-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="7d0c6-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="7d0c6-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7d0c6-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7d0c6-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d0c6-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d0c6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d0c6-128">**Iwmpcontrolsinterface (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="7d0c6-128">**IWMPControlsInterface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7d0c6-129">**Iwmpmediainterface (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="7d0c6-129">**IWMPMediaInterface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7d0c6-130">**Iwmpplaylistcollection. getByName (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="7d0c6-130">**IWMPPlaylistCollection.getByName(VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





