---
title: Iwmpnetwork-Framerate (Eigenschaft)
description: Die Framerate-Eigenschaft ruft die aktuelle Video Frame Rate ab.
ms.assetid: 800ecf3d-3b2c-48f9-8fc4-c7c32757749a
keywords:
- Eigenschaften Fenster "Framerate" Media Player
- Framerate-Eigenschaft, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, Framerate (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPNetwork.frameRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c338a116588fa9f1c552feff15f220e08b0f66e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367565"
---
# <a name="iwmpnetworkframerate-property"></a><span data-ttu-id="34200-106">Iwmpnetwork:: Framerate (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="34200-106">IWMPNetwork::frameRate property</span></span>

<span data-ttu-id="34200-107">Die **Framerate** -Eigenschaft ruft die aktuelle Video Frame Rate ab.</span><span class="sxs-lookup"><span data-stu-id="34200-107">The **frameRate** property gets the current video frame rate.</span></span>

## <a name="syntax"></a><span data-ttu-id="34200-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="34200-108">Syntax</span></span>


```CSharp
public System.Int32 frameRate {get; set;}
```


```VB

Public ReadOnly Property frameRate As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="34200-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="34200-109">Property value</span></span>

<span data-ttu-id="34200-110">Ein **System. Int32** -Wert, bei dem es sich um die aktuelle Frame Rate in Frames pro hundert Sekunden handelt.</span><span class="sxs-lookup"><span data-stu-id="34200-110">A **System.Int32** that is the current frame rate in frames per hundred seconds.</span></span>

> [!Note]  
> <span data-ttu-id="34200-111">Obwohl die **encodecodframerate** -Eigenschaft die codierte Frame Rate in Frames pro Sekunde misst, misst die Framerate-Eigenschaft die aktuelle **Framerate** in Frames pro hundert Sekunden.</span><span class="sxs-lookup"><span data-stu-id="34200-111">Although the **encodedFrameRate** property measures the encoded frame rate in frames per second, the **frameRate** property measures the current frame rate in frames per hundred seconds.</span></span> <span data-ttu-id="34200-112">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="34200-112">See Remarks.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="34200-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34200-113">Remarks</span></span>

<span data-ttu-id="34200-114">Der aktuelle Frameraten Wert wird in Frames pro hundert Sekunden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="34200-114">The current frame rate value is returned in frames per hundred seconds.</span></span> <span data-ttu-id="34200-115">Der Wert 2998 gibt z. b. 29,98 Frames pro Sekunde (fps) an.</span><span class="sxs-lookup"><span data-stu-id="34200-115">For example, a value of 2998 indicates 29.98 frames per second (fps).</span></span>

## <a name="examples"></a><span data-ttu-id="34200-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="34200-116">Examples</span></span>

<span data-ttu-id="34200-117">Im folgenden Codebeispiel wird **Framerate** verwendet, um die beim Codieren der Datei angegebene Framerate anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="34200-117">The following code example uses **frameRate** to display the frame rate specified when the file was encoded.</span></span> <span data-ttu-id="34200-118">Die Informationen werden in einer Bezeichnung als Reaktion auf das **PlayStateChange** -Ereignis angezeigt.</span><span class="sxs-lookup"><span data-stu-id="34200-118">The information is displayed in a label in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="34200-119">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="34200-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the frameRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.frameRate != 0)
            {
                frameRateLabel.Text = "Current Frame Rate: " + player.network.frameRate + " K bits/second";
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

    &#39; Display the frameRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.frameRate <> 0) Then

                frameRateLabel.Text = &quot;Current Frame Rate: &quot; + player.network.frameRate + &quot; K bits/second&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="34200-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34200-120">Requirements</span></span>



| <span data-ttu-id="34200-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34200-121">Requirement</span></span> | <span data-ttu-id="34200-122">Wert</span><span class="sxs-lookup"><span data-stu-id="34200-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34200-123">Version</span><span class="sxs-lookup"><span data-stu-id="34200-123">Version</span></span><br/>   | <span data-ttu-id="34200-124">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="34200-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="34200-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="34200-125">Namespace</span></span><br/> | <span data-ttu-id="34200-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="34200-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="34200-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="34200-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="34200-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="34200-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34200-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34200-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34200-130">**Iwmpnetwork-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="34200-130">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="34200-131">**Iwmpnetwork. encodedframerate (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="34200-131">**IWMPNetwork.encodedFrameRate (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-encodedframerate--vb-and-c.md)
</dt> </dl>

 

 





