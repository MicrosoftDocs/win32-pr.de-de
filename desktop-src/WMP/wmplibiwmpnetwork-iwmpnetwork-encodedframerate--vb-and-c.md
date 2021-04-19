---
title: Iwmpnetwork-encodframerate (Eigenschaft)
description: Die encoabdframerate-Eigenschaft ruft die vom Inhalts Autor angegebene Videoframerate ab.
ms.assetid: 4faf5675-5bf3-485d-802f-a1f900ddae63
keywords:
- encodedframerate-Eigenschaft, Fenster Media Player
- encodedframerate-Eigenschaft, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, encodedframerate (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPNetwork.encodedFrameRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b4176a9c2492d0ce34ffd0936c48dbdef065d1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352827"
---
# <a name="iwmpnetworkencodedframerate-property"></a><span data-ttu-id="09026-106">Iwmpnetwork:: encodebug-Framerate (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="09026-106">IWMPNetwork::encodedFrameRate property</span></span>

<span data-ttu-id="09026-107">Die **encoabdframerate** -Eigenschaft ruft die vom Inhalts Autor angegebene Videoframerate ab.</span><span class="sxs-lookup"><span data-stu-id="09026-107">The **encodedFrameRate** property gets the video frame rate specified by the content author.</span></span>

## <a name="syntax"></a><span data-ttu-id="09026-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="09026-108">Syntax</span></span>


```CSharp
public System.Int32 encodedFrameRate {get; set;}
```


```VB

Public ReadOnly Property encodedFrameRate As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="09026-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="09026-109">Property value</span></span>

<span data-ttu-id="09026-110">Ein **System. Int32** -Wert, der die codierte Framerate in Frames pro Sekunde (fps) ist.</span><span class="sxs-lookup"><span data-stu-id="09026-110">A **System.Int32** that is the encoded frame rate in frames per second (fps).</span></span>

> [!Note]  
> <span data-ttu-id="09026-111">Obwohl die **encodecodframerate** -Eigenschaft die codierte Frame Rate in Frames pro Sekunde misst, misst die Framerate-Eigenschaft die aktuelle **Framerate** in Frames pro hundert Sekunden.</span><span class="sxs-lookup"><span data-stu-id="09026-111">Although the **encodedFrameRate** property measures the encoded frame rate in frames per second, the **frameRate** property measures the current frame rate in frames per hundred seconds.</span></span>

 

## <a name="examples"></a><span data-ttu-id="09026-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="09026-112">Examples</span></span>

<span data-ttu-id="09026-113">Im folgenden Codebeispiel wird **encodedframerate** verwendet, um die beim Codieren der Datei angegebene Framerate anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="09026-113">The following code example uses **encodedFrameRate** to display the frame rate specified when the file was encoded.</span></span> <span data-ttu-id="09026-114">Die Informationen werden in einer Bezeichnung als Reaktion auf das **PlayStateChange** -Ereignis angezeigt.</span><span class="sxs-lookup"><span data-stu-id="09026-114">The information is displayed in a label, in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="09026-115">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="09026-115">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the encodedFrameRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.encodedFrameRate != 0)
            {
                encodedFrameRateLabel.Text = "Current Encoded Frame Rate: " + player.network.encodedFrameRate + " K bits/second";
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

    &#39; Display the encodedFrameRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.encodedFrameRate <> 0) Then

                encodedFrameRateLabel.Text = &quot;Current Encoded Frame Rate: &quot; + player.network.encodedFrameRate + &quot; K bits/second&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="09026-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09026-116">Requirements</span></span>



| <span data-ttu-id="09026-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="09026-117">Requirement</span></span> | <span data-ttu-id="09026-118">Wert</span><span class="sxs-lookup"><span data-stu-id="09026-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09026-119">Version</span><span class="sxs-lookup"><span data-stu-id="09026-119">Version</span></span><br/>   | <span data-ttu-id="09026-120">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="09026-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="09026-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="09026-121">Namespace</span></span><br/> | <span data-ttu-id="09026-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="09026-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="09026-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="09026-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="09026-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="09026-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09026-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09026-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09026-126">**Iwmpnetwork-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="09026-126">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="09026-127">**Iwmpnetwork. Framerate (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="09026-127">**IWMPNetwork.frameRate (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-framerate--vb-and-c.md)
</dt> </dl>

 

 





