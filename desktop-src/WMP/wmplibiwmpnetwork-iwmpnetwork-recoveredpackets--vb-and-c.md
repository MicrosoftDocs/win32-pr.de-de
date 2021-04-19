---
title: Eigenschaften von "iwmpnetwork"
description: Mit der Eigenschaft "Wiederherstellungs Pakete" wird die Anzahl der wiederhergestellten Pakete abgerufen.
ms.assetid: 90fcefcd-2bd7-4fb5-8337-36bec5d44e60
keywords:
- Eigenschaften Fenster für wiederherstellbare Pakete Media Player
- Eigenschaft "Wiederherstellungspakete" Windows Media Player, iwmpnetwork
- Iwmpnetwork Interface, Windows Media Player, Wiederherstellungspakete (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPNetwork.recoveredPackets
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe9fb8b44249be30289abb2f8922343285ca074
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370935"
---
# <a name="iwmpnetworkrecoveredpackets-property"></a><span data-ttu-id="0d8c3-106">Iwmpnetwork:: wiederherepakete (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0d8c3-106">IWMPNetwork::recoveredPackets property</span></span>

<span data-ttu-id="0d8c3-107">Mit der Eigenschaft " **Wiederherstellungs Pakete** " wird die Anzahl der wiederhergestellten Pakete abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0d8c3-107">The **recoveredPackets** property gets the number of recovered packets.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d8c3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d8c3-108">Syntax</span></span>


```CSharp
public System.Int32 recoveredPackets {get; set;}
```


```VB

Public ReadOnly Property recoveredPackets As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="0d8c3-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0d8c3-109">Property value</span></span>

<span data-ttu-id="0d8c3-110">Ein **System. Int32** -Wert, der die Anzahl der wiederhergestellten Pakete ist.</span><span class="sxs-lookup"><span data-stu-id="0d8c3-110">A **System.Int32** that is the number of recovered packets.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d8c3-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d8c3-111">Remarks</span></span>

<span data-ttu-id="0d8c3-112">Jedes Mal, wenn die Wiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf Null zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="0d8c3-112">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="0d8c3-113">Der Wert wird nicht zurückgesetzt, wenn die Wiedergabe angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="0d8c3-113">The value is not reset if playback is paused.</span></span>

<span data-ttu-id="0d8c3-114">Diese Eigenschaft ruft nur während der Laufzeit gültige Informationen ab, wenn die URL für die Wiedergabe mithilfe der **AxWindowsMediaPlayer. URL** -Eigenschaft festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="0d8c3-114">This property gets valid information only during run time when the URL for playback is set by using the **AxWindowsMediaPlayer.URL** property.</span></span> <span data-ttu-id="0d8c3-115">Der Wert ist 0 (null), wenn das HTTP-Protokoll verwendet wird, das verlustfrei ist.</span><span class="sxs-lookup"><span data-stu-id="0d8c3-115">The value will be zero when using the HTTP protocol, which is lossless.</span></span>

## <a name="examples"></a><span data-ttu-id="0d8c3-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d8c3-116">Examples</span></span>

<span data-ttu-id="0d8c3-117">Im folgenden Beispiel wird wieder **herstellbare Pakete** verwendet, um die Anzahl der wiederhergestellten Pakete in einer Bezeichnung als Reaktion auf das **PlayStateChange** -Ereignis anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0d8c3-117">The following example uses **recoveredPackets** to display the number of recovered packets in a label, in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="0d8c3-118">Im Beispiel wird ein Timer mit einem Intervall von 1 Sekunde verwendet, um die Anzeige zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="0d8c3-118">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="0d8c3-119">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0d8c3-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Test whether content is playing. 
    if (e.newState == 3)
    {
        // Start the timer. Update the display every 10 seconds.
        timer.Interval = 10000;
        timer.Start();
    }
    else
    {
        // Not playing; stop the timer.
        timer.Stop();
    }
}

private void UpdateRecoveredPackets(object sender, EventArgs e)
{
    recoveredPacketsLabel.Text = ("Packets recovered: " + player.network.recoveredPackets.ToString());
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

Public Sub UpdateRecoveredPackets(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    recoveredPacketsLabel.Text = (&quot;Packets recovered: &quot; + player.network.recoveredPackets.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="0d8c3-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d8c3-120">Requirements</span></span>



| <span data-ttu-id="0d8c3-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d8c3-121">Requirement</span></span> | <span data-ttu-id="0d8c3-122">Wert</span><span class="sxs-lookup"><span data-stu-id="0d8c3-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d8c3-123">Version</span><span class="sxs-lookup"><span data-stu-id="0d8c3-123">Version</span></span><br/>   | <span data-ttu-id="0d8c3-124">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="0d8c3-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="0d8c3-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="0d8c3-125">Namespace</span></span><br/> | <span data-ttu-id="0d8c3-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="0d8c3-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="0d8c3-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="0d8c3-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0d8c3-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0d8c3-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d8c3-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d8c3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d8c3-130">**AxWindowsMediaPlayer. URL (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0d8c3-130">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0d8c3-131">**Iwmpnetwork-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0d8c3-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





