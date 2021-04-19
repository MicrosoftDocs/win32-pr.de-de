---
title: Iwmpnetwork BufferingProgress (Eigenschaft)
description: Die BufferingProgress-Eigenschaft ruft den Prozentsatz der abgeschlossenen Pufferung ab.
ms.assetid: 8dc9f31e-7c34-4714-a633-d92c3da3052b
keywords:
- BufferingProgress-Eigenschaften Fenster Media Player
- BufferingProgress-Eigenschaft, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, BufferingProgress (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1da8a27ba41e5c4e201a5bdf0197992c30bce80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370157"
---
# <a name="iwmpnetworkbufferingprogress-property"></a><span data-ttu-id="5a673-106">Iwmpnetwork:: BufferingProgress (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5a673-106">IWMPNetwork::bufferingProgress property</span></span>

<span data-ttu-id="5a673-107">Die **BufferingProgress** -Eigenschaft ruft den Prozentsatz der abgeschlossenen Pufferung ab.</span><span class="sxs-lookup"><span data-stu-id="5a673-107">The **bufferingProgress** property gets the percentage of buffering completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a673-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a673-108">Syntax</span></span>


```CSharp
public System.Int32 bufferingProgress {get; set;}
```


```VB

Public ReadOnly Property bufferingProgress As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="5a673-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="5a673-109">Property value</span></span>

<span data-ttu-id="5a673-110">Ein **System. Int32** -Wert, der der Puffer Status ist, ausgedrückt als Prozentsatz.</span><span class="sxs-lookup"><span data-stu-id="5a673-110">A **System.Int32** that is the buffering progress expressed as a percentage.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a673-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a673-111">Remarks</span></span>

<span data-ttu-id="5a673-112">Jedes Mal, wenn die Wiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf Null zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="5a673-112">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="5a673-113">Wenn die Wiedergabe angehalten wird, wird Sie nicht zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="5a673-113">It is not reset if playback is paused.</span></span>

<span data-ttu-id="5a673-114">Die Pufferung gilt nur für Streaminginhalte.</span><span class="sxs-lookup"><span data-stu-id="5a673-114">Buffering applies only to streaming content.</span></span> <span data-ttu-id="5a673-115">Diese Eigenschaft ruft nur während der Laufzeit gültige Informationen ab, wenn die URL für die Wiedergabe mithilfe der **AxWindowsMediaPlayer. URL** -Eigenschaft festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="5a673-115">This property gets valid information only during run time when the URL for playback is set using the **AxWindowsMediaPlayer.URL** property.</span></span>

<span data-ttu-id="5a673-116">Verwenden Sie den **AxWindowsMediaPlayer. \_ Wmpocxevents \_ bufferingevent** , um zu bestimmen, wann die Pufferung gestartet oder angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="5a673-116">Use the **AxWindowsMediaPlayer.\_WMPOCXEvents\_BufferingEvent** to determine when buffering starts or stops.</span></span>

## <a name="examples"></a><span data-ttu-id="5a673-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5a673-117">Examples</span></span>

<span data-ttu-id="5a673-118">Im folgenden Beispiel wird **BufferingProgress** verwendet, um den Prozentsatz der in einer Bezeichnung abgeschlossenen Pufferung als Reaktion auf das Puffer Ereignis anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5a673-118">The following example uses **bufferingProgress** to display the percentage of buffering completed in a label, in response to the Buffering Event.</span></span> <span data-ttu-id="5a673-119">Im Beispiel wird ein Timer mit einem Intervall von 1 Sekunde verwendet, um die Anzeige zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5a673-119">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="5a673-120">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="5a673-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the Buffering event.
player.Buffering += new AxWMPLib._WMPOCXEvents_BufferingEventHandler(player_Buffering);

// Create an event handler for the Buffering event.
private void player_Buffering(object sender, AxWMPLib._WMPOCXEvents_BufferingEvent e)
{
    // Determine whether buffering has started or stopped.
    if (e.start == true)
    {
        // Set the timer interval at one second (1000 miliseconds).
        timer.Interval = 1000;
        
        // Start the timer.
        timer.Start();
    }
    else
    {
        // Buffering is complete. Stop the timer.
        timer.Stop();
    }
}

// Update the buffering progress in a timer event handler.
private void UpdateBufferingProgress(object sender, EventArgs e)
{
    bufferingProgressLabel.Text = ("Buffering progress: " + player.network.bufferingProgress + " percent complete");
}
```


```VB

' Create an event handler for the Buffering event.
Public Sub player_Buffering(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_BufferingEvent) Handles player.Buffering

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

&#39; Update the buffering progress in a timer event handler.
Public Sub UpdateBufferingProgress(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    bufferingProgressLabel.Text = (&quot;Buffering progress: &quot; + player.network.bufferingProgress + &quot; percent complete&quot;)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="5a673-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a673-121">Requirements</span></span>



| <span data-ttu-id="5a673-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5a673-122">Requirement</span></span> | <span data-ttu-id="5a673-123">Wert</span><span class="sxs-lookup"><span data-stu-id="5a673-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a673-124">Version</span><span class="sxs-lookup"><span data-stu-id="5a673-124">Version</span></span><br/>   | <span data-ttu-id="5a673-125">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="5a673-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="5a673-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="5a673-126">Namespace</span></span><br/> | <span data-ttu-id="5a673-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="5a673-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="5a673-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="5a673-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5a673-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="5a673-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a673-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a673-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a673-131">**AxWindowsMediaPlayer. URL (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="5a673-131">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5a673-132">**AxWindowsMediaPlayer. buffereing-Ereignis (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="5a673-132">**AxWindowsMediaPlayer.Buffering Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-buffering.md)
</dt> <dt>

[<span data-ttu-id="5a673-133">**Iwmpnetwork-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="5a673-133">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





