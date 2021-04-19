---
title: Iwmpnetwork-Bandbreiten Eigenschaft
description: Die Bandbreiten Eigenschaft ruft die aktuelle Bandbreite des Medien Elements ab.
ms.assetid: 4355aa14-bca7-4b46-aad5-3e3796a54735
keywords:
- Bandbreiten Eigenschaften Fenster Media Player
- Bandbreiten Eigenschaft Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, Bandbreiten Eigenschaft
topic_type:
- apiref
api_name:
- IWMPNetwork.bandWidth
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df9a55f9d5c6724c428b75a4171c2e8b7ca13d18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354125"
---
# <a name="iwmpnetworkbandwidth-property"></a><span data-ttu-id="e844a-106">Iwmpnetwork:: bandWidth (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e844a-106">IWMPNetwork::bandWidth property</span></span>

<span data-ttu-id="e844a-107">Die **Bandbreiten** Eigenschaft ruft die aktuelle Bandbreite des Medien Elements ab.</span><span class="sxs-lookup"><span data-stu-id="e844a-107">The **bandWidth** property gets the current bandwidth of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="e844a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e844a-108">Syntax</span></span>


```CSharp
public System.Int32 bandWidth {get; set;}
```


```VB

Public ReadOnly Property bandWidth As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="e844a-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e844a-109">Property value</span></span>

<span data-ttu-id="e844a-110">Eine **System. Int32** , die die Bandbreite ist.</span><span class="sxs-lookup"><span data-stu-id="e844a-110">A **System.Int32** that is the bandwidth.</span></span>

## <a name="remarks"></a><span data-ttu-id="e844a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e844a-111">Remarks</span></span>

<span data-ttu-id="e844a-112">Der durch **AxWindowsMediaPlayer. URL** abgerufene Wert ist 0 (null), wenn die URL nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e844a-112">The value retrieved through **AxWindowsMediaPlayer.URL** will be zero if the URL is not set.</span></span> <span data-ttu-id="e844a-113">Diese Eigenschaft ist nur für Streamingmedien gültig.</span><span class="sxs-lookup"><span data-stu-id="e844a-113">This property is valid only for streaming media.</span></span>

## <a name="examples"></a><span data-ttu-id="e844a-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e844a-114">Examples</span></span>

<span data-ttu-id="e844a-115">Im folgenden Beispiel wird **Bandbreite** verwendet, um die aktuelle Medien Bandbreite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e844a-115">The following example uses **bandWidth** to display the current media bandwidth.</span></span> <span data-ttu-id="e844a-116">Die Informationen werden in einer Bezeichnung als Reaktion auf das **PlayStateChange** -Ereignis angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e844a-116">The information is displayed in a label in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="e844a-117">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e844a-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the bandwidth when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.bandWidth != 0)
            {
                bandWidthLabel.Text = "Current Bandwidth: " + player.network.bandWidth + " K bits/second";
            }
            else
            {
                bandWidthLabel.Text = "Bandwidth is only available for streaming media.";
            }
            break;

        default:
            break;
    }
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    &#39; Display the bandWidth when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.bandWidth <> 0) Then

                bandWidthLabel.Text = &quot;Current Bandwidth: &quot; + player.network.bandWidth + &quot; K bits/second&quot;

            Else

                bandWidthLabel.Text = &quot;Bandwidth is only available for streaming media.&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="e844a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e844a-118">Requirements</span></span>



| <span data-ttu-id="e844a-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e844a-119">Requirement</span></span> | <span data-ttu-id="e844a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="e844a-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e844a-121">Version</span><span class="sxs-lookup"><span data-stu-id="e844a-121">Version</span></span><br/>   | <span data-ttu-id="e844a-122">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="e844a-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="e844a-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="e844a-123">Namespace</span></span><br/> | <span data-ttu-id="e844a-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e844a-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e844a-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="e844a-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e844a-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e844a-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e844a-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e844a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e844a-128">**AxWindowsMediaPlayer. URL (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e844a-128">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e844a-129">**Iwmpnetwork-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e844a-129">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





