---
title: Iwmpnetwork-Bitrate (Eigenschaft)
description: Die Bitrate-Eigenschaft ruft die aktuelle Bitrate ab, die empfangen wird.
ms.assetid: f7dda557-3954-45ed-9eac-6d27109e2dfa
keywords:
- Bitrate-Eigenschaften Fenster Media Player
- Bitrate-Eigenschaft, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, Bitrate (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPNetwork.bitRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f64039eb960a928f5268643e18d1a01b9034d5d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365966"
---
# <a name="iwmpnetworkbitrate-property"></a><span data-ttu-id="980a4-106">Iwmpnetwork:: Bitrate (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="980a4-106">IWMPNetwork::bitRate property</span></span>

<span data-ttu-id="980a4-107">Die **Bitrate** -Eigenschaft ruft die aktuelle Bitrate ab, die empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="980a4-107">The **bitRate** property gets the current bit rate being received.</span></span>

## <a name="syntax"></a><span data-ttu-id="980a4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="980a4-108">Syntax</span></span>


```CSharp
public System.Int32 bitRate {get; set;}
```


```VB

Public ReadOnly Property bitRate As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="980a4-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="980a4-109">Property value</span></span>

<span data-ttu-id="980a4-110">Ein **System. Int32** -Wert, der die Bitrate ist.</span><span class="sxs-lookup"><span data-stu-id="980a4-110">A **System.Int32** that is the bit rate.</span></span>

## <a name="remarks"></a><span data-ttu-id="980a4-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="980a4-111">Remarks</span></span>

<span data-ttu-id="980a4-112">Der Wert dieser Eigenschaft ist eine Kombination aus den Bitraten von Video-und Audiodatenströmen.</span><span class="sxs-lookup"><span data-stu-id="980a4-112">The value of this property is a combination of the bit rates of both video and audio streams.</span></span>

## <a name="examples"></a><span data-ttu-id="980a4-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="980a4-113">Examples</span></span>

<span data-ttu-id="980a4-114">Im folgenden Beispiel wird die Bitrate verwendet, um die aktuelle Medien **Bitrate** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="980a4-114">The following example uses **bitRate** to display the current media bit rate.</span></span> <span data-ttu-id="980a4-115">Die Informationen werden in einer Bezeichnung als Reaktion auf das **PlayStateChange** -Ereignis angezeigt.</span><span class="sxs-lookup"><span data-stu-id="980a4-115">The information is displayed in a label in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="980a4-116">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="980a4-116">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the bitRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.bitRate != 0)
            {
                bitRateLabel.Text = "Current Bit Rate: " + player.network.bitRate + " K bits/second";
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

    &#39; Display the bitRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.bitRate <> 0) Then

                bitRateLabel.Text = &quot;Current Bit Rate: &quot; + player.network.bitRate + &quot; K bits/second&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="980a4-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="980a4-117">Requirements</span></span>



| <span data-ttu-id="980a4-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="980a4-118">Requirement</span></span> | <span data-ttu-id="980a4-119">Wert</span><span class="sxs-lookup"><span data-stu-id="980a4-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="980a4-120">Version</span><span class="sxs-lookup"><span data-stu-id="980a4-120">Version</span></span><br/>   | <span data-ttu-id="980a4-121">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="980a4-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="980a4-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="980a4-122">Namespace</span></span><br/> | <span data-ttu-id="980a4-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="980a4-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="980a4-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="980a4-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="980a4-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="980a4-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="980a4-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="980a4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="980a4-127">**Iwmpnetwork-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="980a4-127">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





