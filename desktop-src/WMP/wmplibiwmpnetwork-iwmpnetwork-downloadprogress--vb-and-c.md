---
title: Iwmpnetwork DownloadProgress (Eigenschaft)
description: Die DownloadProgress-Eigenschaft ruft den Prozentsatz des abgeschlossenen Downloads ab.
ms.assetid: 40568c81-5bb5-45d9-b654-31072608663d
keywords:
- Download Progress-Eigenschaften Fenster Media Player
- Download Progress-Eigenschaft, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, Download Progress (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPNetwork.downloadProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b10b767845ac951e1364e15c7f6f1d729882e0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358222"
---
# <a name="iwmpnetworkdownloadprogress-property"></a><span data-ttu-id="c3c33-106">Iwmpnetwork::d ownloadprogress-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c3c33-106">IWMPNetwork::downloadProgress property</span></span>

<span data-ttu-id="c3c33-107">Die **DownloadProgress** -Eigenschaft ruft den Prozentsatz des abgeschlossenen Downloads ab.</span><span class="sxs-lookup"><span data-stu-id="c3c33-107">The **downloadProgress** property gets the percentage of downloading completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3c33-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3c33-108">Syntax</span></span>


```CSharp
public System.Int32 downloadProgress {get; set;}
```


```VB

Public ReadOnly Property downloadProgress As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="c3c33-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c3c33-109">Property value</span></span>

<span data-ttu-id="c3c33-110">Ein **System. Int32** -Wert, der den Download Fortschritt als Prozentsatz ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="c3c33-110">A **System.Int32** that is the download progress expressed as a percentage.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3c33-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3c33-111">Remarks</span></span>

<span data-ttu-id="c3c33-112">Wenn das Windows Media Player-Steuerelement mit einer digitalen Mediendatei verbunden ist, die gleichzeitig abgespielt und heruntergeladen werden kann, ruft die **DownloadProgress** -Eigenschaft den Prozentsatz der gesamten heruntergeladenen Datei ab.</span><span class="sxs-lookup"><span data-stu-id="c3c33-112">When the Windows Media Player control is connected to a digital media file that can be played and downloaded at the same time, the **downloadProgress** property gets the percentage of the total file that has been downloaded.</span></span> <span data-ttu-id="c3c33-113">Diese Funktion wird zurzeit nur für digitale Mediendateien unterstützt, die von Webservern heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="c3c33-113">This feature is currently supported only for digital media files downloaded from web servers.</span></span> <span data-ttu-id="c3c33-114">Eine Datei mit einem der folgenden Formate kann heruntergeladen und gleichzeitig abgespielt werden:</span><span class="sxs-lookup"><span data-stu-id="c3c33-114">A file of any of the following formats can be downloaded and played simultaneously:</span></span>

-   <span data-ttu-id="c3c33-115">Advanced Systems Format (ASF)</span><span class="sxs-lookup"><span data-stu-id="c3c33-115">Advanced Systems Format (ASF)</span></span>
-   <span data-ttu-id="c3c33-116">Windows Media Audio (WMA)</span><span class="sxs-lookup"><span data-stu-id="c3c33-116">Windows Media Audio (WMA)</span></span>
-   <span data-ttu-id="c3c33-117">Windows Media Video (WMV)</span><span class="sxs-lookup"><span data-stu-id="c3c33-117">Windows Media Video (WMV)</span></span>
-   <span data-ttu-id="c3c33-118">MP3</span><span class="sxs-lookup"><span data-stu-id="c3c33-118">MP3</span></span>
-   <span data-ttu-id="c3c33-119">MPEG</span><span class="sxs-lookup"><span data-stu-id="c3c33-119">MPEG</span></span>
-   <span data-ttu-id="c3c33-120">WAV</span><span class="sxs-lookup"><span data-stu-id="c3c33-120">WAV</span></span>

<span data-ttu-id="c3c33-121">Darüber hinaus können einige AVI-Dateien gleichzeitig heruntergeladen und abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="c3c33-121">In addition, some AVI files can be downloaded and played simultaneously.</span></span>

<span data-ttu-id="c3c33-122">Verwenden Sie den **AxWindowsMediaPlayer. \_ Wmpocxevents \_ bufferingevent** , um zu bestimmen, wann die Pufferung gestartet oder angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="c3c33-122">Use the **AxWindowsMediaPlayer.\_WMPOCXEvents\_BufferingEvent** to determine when buffering starts or stops.</span></span>

## <a name="examples"></a><span data-ttu-id="c3c33-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3c33-123">Examples</span></span>

<span data-ttu-id="c3c33-124">Im folgenden Codebeispiel wird **Download Progress** verwendet, um den Prozentsatz des abgeschlossenen Downloads anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c3c33-124">The following code example uses **downloadProgress** to display the percentage of downloading completed.</span></span> <span data-ttu-id="c3c33-125">Die Informationen werden in einer Bezeichnung als Reaktion auf das **Puffer** Ereignis angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c3c33-125">The information is displayed in a label, in response to the **Buffering** Event.</span></span> <span data-ttu-id="c3c33-126">Im Beispiel wird ein Timer mit einem Intervall von 1 Sekunde verwendet, um die Anzeige zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c3c33-126">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="c3c33-127">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c3c33-127">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


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

// Update the download progress in a timer event handler.
private void UpdateDownloadProgress(object sender, EventArgs e)
{
    downloadProgressLabel.Text = ("Download progress: " + player.network.downloadProgress + " percent complete");
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

&#39; Update the download progress in a timer event handler.
Public Sub UpdateDownloadProgress(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    downloadProgressLabel.Text = (&quot;Download progress: &quot; + player.network.downloadProgress + &quot; percent complete&quot;)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="c3c33-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3c33-128">Requirements</span></span>



| <span data-ttu-id="c3c33-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3c33-129">Requirement</span></span> | <span data-ttu-id="c3c33-130">Wert</span><span class="sxs-lookup"><span data-stu-id="c3c33-130">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3c33-131">Version</span><span class="sxs-lookup"><span data-stu-id="c3c33-131">Version</span></span><br/>   | <span data-ttu-id="c3c33-132">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="c3c33-132">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c3c33-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="c3c33-133">Namespace</span></span><br/> | <span data-ttu-id="c3c33-134">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c3c33-134">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c3c33-135">Assembly</span><span class="sxs-lookup"><span data-stu-id="c3c33-135">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c3c33-136"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c3c33-136"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3c33-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3c33-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3c33-138">**AxWindowsMediaPlayer. buffereing-Ereignis (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="c3c33-138">**AxWindowsMediaPlayer.Buffering Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-buffering.md)
</dt> <dt>

[<span data-ttu-id="c3c33-139">**Iwmpnetwork-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="c3c33-139">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





