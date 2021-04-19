---
title: Iwmpnetwork-Eigenschaft (Eigenschaft)
description: Die Eigenschaft "receptionquality" Ruft den Prozentsatz der in den letzten 30 Sekunden nicht verlorenen Pakete ab.
ms.assetid: 103e6b8f-e029-4f53-93ac-b516896a7594
keywords:
- Eigenschaften Fenster von "receptionquality" Media Player
- Eigenschaft "receptionquality", Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, Eigenschaft "receptionquality"
topic_type:
- apiref
api_name:
- IWMPNetwork.receptionQuality
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3703ffa29183937874c40053bd3c7ae3c85d75d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370840"
---
# <a name="iwmpnetworkreceptionquality-property"></a><span data-ttu-id="4422a-106">Iwmpnetwork:: receptionquality (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4422a-106">IWMPNetwork::receptionQuality property</span></span>

<span data-ttu-id="4422a-107">Die Eigenschaft " **receptionquality** " Ruft den Prozentsatz der in den letzten 30 Sekunden nicht verlorenen Pakete ab.</span><span class="sxs-lookup"><span data-stu-id="4422a-107">The **receptionQuality** property gets the percentage of packets not lost in the last 30 seconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="4422a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4422a-108">Syntax</span></span>


```CSharp
public System.Int32 receptionQuality {get; set;}
```


```VB

Public ReadOnly Property receptionQuality As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="4422a-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="4422a-109">Property value</span></span>

<span data-ttu-id="4422a-110">Eine **System. Int32** , die die Empfangsqualität ist.</span><span class="sxs-lookup"><span data-stu-id="4422a-110">A **System.Int32** that is the reception quality.</span></span>

## <a name="remarks"></a><span data-ttu-id="4422a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4422a-111">Remarks</span></span>

<span data-ttu-id="4422a-112">Die Anzahl der während des Streamings empfangenen, verlorenen und wiederhergestellten Pakete wird einmal pro Sekunde überwacht.</span><span class="sxs-lookup"><span data-stu-id="4422a-112">The number of packets received, lost, and recovered during streaming is monitored once every second.</span></span> <span data-ttu-id="4422a-113">Die Eigenschaft " **receptionquality** " Ruft den Prozentsatz der in den letzten 30 Sekunden nicht verlorenen Pakete ab.</span><span class="sxs-lookup"><span data-stu-id="4422a-113">The **receptionQuality** property gets the percentage of packets not lost during the last 30 seconds.</span></span>

<span data-ttu-id="4422a-114">Jedes Mal, wenn die Wiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf Null zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="4422a-114">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="4422a-115">Der Wert wird nicht zurückgesetzt, wenn die Wiedergabe angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="4422a-115">The value is not reset if playback is paused.</span></span>

<span data-ttu-id="4422a-116">Diese Eigenschaft ruft nur während der Laufzeit gültige Informationen ab, wenn die URL für die Wiedergabe mithilfe der **AxWindowsMediaPlayer. URL** -Eigenschaft festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="4422a-116">This property gets valid information only during run time when the URL for playback is set by using the **AxWindowsMediaPlayer.URL** property.</span></span>

## <a name="examples"></a><span data-ttu-id="4422a-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4422a-117">Examples</span></span>

<span data-ttu-id="4422a-118">Im folgenden Beispiel wird " **receptionquality** " verwendet, um den Prozentsatz der Pakete anzuzeigen, die in einer Bezeichnung als Reaktion auf das **PlayStateChange** -Ereignis empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="4422a-118">The following example uses **receptionQuality** to display the percentage of packets received in a label, in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="4422a-119">Im Beispiel wird ein Timer mit einem Intervall von 1 Sekunde verwendet, um die Anzeige zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="4422a-119">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="4422a-120">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="4422a-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


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

private void UpdateReceptionQuality(object sender, EventArgs e)
{
    receptionQualityLabel.Text = ("Packets recovered: " + player.network.receptionQuality.ToString() + "%");
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

Public Sub UpdateReceptionQuality(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    receptionQualityLabel.Text = (&quot;Packets recovered: &quot; + player.network.receptionQuality.ToString() + &quot;%&quot;)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="4422a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4422a-121">Requirements</span></span>



| <span data-ttu-id="4422a-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4422a-122">Requirement</span></span> | <span data-ttu-id="4422a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="4422a-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4422a-124">Version</span><span class="sxs-lookup"><span data-stu-id="4422a-124">Version</span></span><br/>   | <span data-ttu-id="4422a-125">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="4422a-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="4422a-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="4422a-126">Namespace</span></span><br/> | <span data-ttu-id="4422a-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="4422a-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4422a-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="4422a-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4422a-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4422a-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4422a-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4422a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4422a-131">**AxWindowsMediaPlayer. URL (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="4422a-131">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4422a-132">**Iwmpnetwork-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="4422a-132">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





