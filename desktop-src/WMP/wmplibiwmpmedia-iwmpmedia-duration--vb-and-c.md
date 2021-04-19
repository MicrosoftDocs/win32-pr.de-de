---
title: Iwmpmedia Duration (Eigenschaft)
description: Die Duration-Eigenschaft ruft die Dauer des aktuellen Medien Elements in Sekunden ab.
ms.assetid: f8a0bf3e-eeaf-46f5-90c8-d3b11ce4eb39
keywords:
- Duration-Eigenschaften Fenster Media Player
- Duration-Eigenschaft, Windows Media Player, iwmpmedia-Schnittstelle
- Iwmpmedia Interface, Windows Media Player, Duration-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPMedia.duration
- IWMPMedia.get_duration
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f796cab042713082ce2066659f62736855e62787
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373969"
---
# <a name="iwmpmediaduration-property"></a><span data-ttu-id="164e2-106">Iwmpmedia::d urationseigenschaft</span><span class="sxs-lookup"><span data-stu-id="164e2-106">IWMPMedia::duration property</span></span>

<span data-ttu-id="164e2-107">Die **Duration** -Eigenschaft ruft die Dauer des aktuellen Medien Elements in Sekunden ab.</span><span class="sxs-lookup"><span data-stu-id="164e2-107">The **duration** property gets the duration in seconds of the current media item.</span></span>

<span data-ttu-id="164e2-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="164e2-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="164e2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="164e2-109">Syntax</span></span>


```CSharp
public System.Double duration {get;}
```


```VB

Public ReadOnly Property duration As System.Double
```





## <a name="property-value"></a><span data-ttu-id="164e2-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="164e2-110">Property value</span></span>

<span data-ttu-id="164e2-111">Ein **System. Double** -Wert, der die Dauer in Sekunden angibt.</span><span class="sxs-lookup"><span data-stu-id="164e2-111">A **System.Double** that is the duration in seconds.</span></span>

## <a name="remarks"></a><span data-ttu-id="164e2-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="164e2-112">Remarks</span></span>

<span data-ttu-id="164e2-113">Wenn diese Eigenschaft mit einem anderen als dem in AxWindowsMediaPlayer. currentMedia angegebenen Medien Element verwendet wird, enthält Sie möglicherweise keinen gültigen Wert.</span><span class="sxs-lookup"><span data-stu-id="164e2-113">If this property is used with a media item other than the one specified in AxWindowsMediaPlayer.currentMedia, it may not contain a valid value.</span></span>

<span data-ttu-id="164e2-114">Zum Abrufen der Dauer für Dateien, die sich nicht in der Bibliothek des Benutzers befinden, müssen Sie auf das Öffnen der Datei durch Windows Media Player warten. Das heißt, dass der aktuelle **openstate** -Wert " **mediaopen**" entsprechen muss.</span><span class="sxs-lookup"><span data-stu-id="164e2-114">To retrieve the duration for files that are not in the user's library, you must wait for Windows Media Player to open the file; that is, the current **OpenState** must equal **MediaOpen**.</span></span> <span data-ttu-id="164e2-115">Sie können dies überprüfen, indem Sie **AxWindowsMediaPlayer verarbeiten. \_ Wmpocxevents \_ OpenStateChange** -Ereignis oder durch regelmäßiges Überprüfen des Werts von **AxWindowsMediaPlayer. openstate**.</span><span class="sxs-lookup"><span data-stu-id="164e2-115">You can verify this by handling the **AxWindowsMediaPlayer.\_WMPOCXEvents\_OpenStateChange** event or by periodically checking the value of **AxWindowsMediaPlayer.openState**.</span></span>

<span data-ttu-id="164e2-116">Bei Wiedergabelisten kann die Dauer der einzelnen Medienelemente abgerufen werden, wenn das einzelne Medien Element geöffnet wird, anstatt beim Öffnen der Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="164e2-116">For playlists, the duration of each media item can be retrieved when the individual media item is opened, rather than the when the playlist is opened.</span></span>

<span data-ttu-id="164e2-117">Vor der Verwendung dieser Eigenschaft müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="164e2-117">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="164e2-118">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="164e2-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="164e2-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="164e2-119">Examples</span></span>

<span data-ttu-id="164e2-120">Im folgenden Beispiel wird **Duration** verwendet, um die verbleibende Zeit im aktuellen Medien Element in einer Bezeichnung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="164e2-120">The following example uses **duration** to display the time remaining in the current media item in a label.</span></span> <span data-ttu-id="164e2-121">Ein Timer aktualisiert den Text in der Bezeichnung jede Sekunde.</span><span class="sxs-lookup"><span data-stu-id="164e2-121">A timer updates the text in the label every second.</span></span>


```CSharp
// Set the timer to fire an event every second and start the timer.
timer.Interval = 1000;
timer.Start();

// Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
// determine when to start and stop the timer. 

private void TimerEventProcessor(object sender, System.EventArgs e)
{
    // Subtract the current position from the duration of the current media to get
    // the time remaining. Use the Math.floor method to round the result down to the
    // nearest whole number.
    double t = Math.Floor(player.currentMedia.duration - player.Ctlcontrols.currentPosition);

    // Display the time remaining in the current media.
    timeRemaining.Text = ("Seconds remaining: " + t.ToString());        
}
```


```VB

' Set the timer to fire an event every second and start the timer.
Timer.Interval = 1000
Timer.Start()

&#39; Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a Select Case statement to
&#39; determine when to start and stop the timer. 

Public Sub TimerEventProcessor(ByVal sender As Object, ByVal e As System.EventArgs) Handles Timer.Tick

    &#39; Subtract the current position from the duration of the current media to get
    &#39; the time remaining. Use the Math.Floor method to round the result down to the
    &#39; nearest whole number.
    Dim t As Double = Math.Floor(player.currentMedia.duration - player.Ctlcontrols.currentPosition)

    &#39; Display the time remaining in the current media.
    timeRemaining.Text = (&quot;Seconds remaining: &quot; + t.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="164e2-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="164e2-122">Requirements</span></span>



| <span data-ttu-id="164e2-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="164e2-123">Requirement</span></span> | <span data-ttu-id="164e2-124">Wert</span><span class="sxs-lookup"><span data-stu-id="164e2-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="164e2-125">Version</span><span class="sxs-lookup"><span data-stu-id="164e2-125">Version</span></span><br/>   | <span data-ttu-id="164e2-126">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="164e2-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="164e2-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="164e2-127">Namespace</span></span><br/> | <span data-ttu-id="164e2-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="164e2-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="164e2-129">Assembly</span><span class="sxs-lookup"><span data-stu-id="164e2-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="164e2-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="164e2-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="164e2-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="164e2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="164e2-132">**AxWindowsMediaPlayer. currentMedia (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="164e2-132">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="164e2-133">**AxWindowsMediaPlayer. openstate (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="164e2-133">**AxWindowsMediaPlayer.openState (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="164e2-134">**AxWindowsMediaPlayer. OpenStateChange-Ereignis (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="164e2-134">**AxWindowsMediaPlayer.OpenStateChange Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-openstatechange.md)
</dt> <dt>

[<span data-ttu-id="164e2-135">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="164e2-135">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="164e2-136">**Iwmpmedia. durationString (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="164e2-136">**IWMPMedia.durationString (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-durationstring--vb-and-c.md)
</dt> </dl>

 

 





