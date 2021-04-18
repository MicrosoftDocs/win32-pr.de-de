---
title: Iwmpnetwork receivedpakete (Eigenschaft)
description: Die receivedpaketen-Eigenschaft ruft die Anzahl der empfangenen Pakete ab.
ms.assetid: 2a79dc81-4c7a-45d6-bc2b-b19ff5704c3b
keywords:
- receivedpaketen-Eigenschaft, Windows Media Player
- receivedpaketen-Eigenschaft, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, receivedpakete (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPNetwork.receivedPackets
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90c62b4d90039f07177e8fcdc971cb66e0044aee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354822"
---
# <a name="iwmpnetworkreceivedpackets-property"></a><span data-ttu-id="b5f60-106">Iwmpnetwork:: receivedpakete (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b5f60-106">IWMPNetwork::receivedPackets property</span></span>

<span data-ttu-id="b5f60-107">Die **receivedpaketen** -Eigenschaft ruft die Anzahl der empfangenen Pakete ab.</span><span class="sxs-lookup"><span data-stu-id="b5f60-107">The **receivedPackets** property gets the number of packets received.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5f60-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5f60-108">Syntax</span></span>


```CSharp
public System.Int32 receivedPackets {get; set;}
```


```VB

Public ReadOnly Property receivedPackets As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="b5f60-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b5f60-109">Property value</span></span>

<span data-ttu-id="b5f60-110">Ein **System. Int32** -Wert, der die Anzahl der empfangenen Pakete ist.</span><span class="sxs-lookup"><span data-stu-id="b5f60-110">A **System.Int32** that is the number of packets received.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5f60-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5f60-111">Remarks</span></span>

<span data-ttu-id="b5f60-112">Jedes Mal, wenn die Wiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf Null zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="b5f60-112">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="b5f60-113">Der Wert wird nicht zurückgesetzt, wenn die Wiedergabe angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f60-113">The value is not reset if playback is paused.</span></span>

## <a name="examples"></a><span data-ttu-id="b5f60-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b5f60-114">Examples</span></span>

<span data-ttu-id="b5f60-115">Im folgenden Beispiel wird **receivedpakete** verwendet, um die Anzahl der empfangenen Pakete anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b5f60-115">The following example uses **receivedPackets** to display the number of packets received.</span></span> <span data-ttu-id="b5f60-116">Die Informationen werden in einer Bezeichnung als Reaktion auf das **PlayStateChange** -Ereignis angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b5f60-116">The information is displayed in a label in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="b5f60-117">Im Beispiel wird ein Timer mit einem Intervall von 1 Sekunde verwendet, um die Anzeige zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b5f60-117">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="b5f60-118">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b5f60-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Test whether packets may be arriving.
    switch (e.newState)
    {
        // If WMPPlayState is Stopped, Paused, ScanForward, ScanReverse, Waiting, MediaEnded
        // or Transitioning then stop the timer. 
        case 1: 
        case 2: 
        case 4: 
        case 5: 
        case 7: 
        case 8: 
        case 9: 
            timer.Stop();
            break;

        // If WMPPlayState is Playing or Buffering then set the timer interval and start the timer.
        default:
            timer.Interval = 1000;
            timer.Start();
            break;
    }
}

private void UpdateReceivedPackets(object sender, EventArgs e)
{
    receivedPacketsLabel.Text = ("Packets received: " + player.network.receivedPackets.ToString());
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    &#39; Test whether packets may be arriving.
    Select Case e.newState

    &#39; If WMPPlayState is Stopped, Paused, ScanForward, ScanReverse, Waiting, MediaEnded
    &#39; or Transitioning then stop the timer. 
        Case 1
        Case 2
        Case 4
        Case 5
        Case 7
        Case 8
        Case 9
            timer.Stop()

        &#39; If WMPPlayState is Playing or Buffering then set the timer interval and start the timer.
        Case Else
            timer.Interval = 1000
            timer.Start()

    End Select

End Sub

Public Sub UpdateReceivedPackets(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    receivedPacketsLabel.Text = (&quot;Packets received: &quot; + player.network.receivedPackets.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="b5f60-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5f60-119">Requirements</span></span>



| <span data-ttu-id="b5f60-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5f60-120">Requirement</span></span> | <span data-ttu-id="b5f60-121">Wert</span><span class="sxs-lookup"><span data-stu-id="b5f60-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5f60-122">Version</span><span class="sxs-lookup"><span data-stu-id="b5f60-122">Version</span></span><br/>   | <span data-ttu-id="b5f60-123">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="b5f60-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b5f60-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="b5f60-124">Namespace</span></span><br/> | <span data-ttu-id="b5f60-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b5f60-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b5f60-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="b5f60-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b5f60-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b5f60-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5f60-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5f60-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5f60-129">**Iwmpnetwork-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="b5f60-129">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





