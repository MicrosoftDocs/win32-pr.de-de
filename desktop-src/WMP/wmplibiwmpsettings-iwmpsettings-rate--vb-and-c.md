---
title: Iwmpsettings-Rate (Eigenschaft)
description: Mit der Eigenschaft Rate wird die aktuelle Wiedergabe Rate für Video abgerufen oder festgelegt.
ms.assetid: 7baa667b-52e5-4419-8e12-c3627a417b20
keywords:
- Rate der Eigenschaften Fenster Media Player
- Rate der Eigenschaften Fenster Media Player, iwmpsettings-Schnittstelle
- Iwmpsettings-Schnittstelle, Windows-Media Player, Rate-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPSettings.rate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f502bebdbd22523858637f8abccbe203db104cbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367596"
---
# <a name="iwmpsettingsrate-property"></a><span data-ttu-id="9cf46-106">Iwmpsettings:: Rate (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9cf46-106">IWMPSettings::rate property</span></span>

<span data-ttu-id="9cf46-107">Mit der Eigenschaft **Rate** wird die aktuelle Wiedergabe Rate für Video abgerufen oder festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9cf46-107">The **rate** property gets or sets the current playback rate for video.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cf46-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9cf46-108">Syntax</span></span>


```CSharp
public System.Double rate {get; set;}
```


```VB

Public Property rate As System.Double
```





## <a name="property-value"></a><span data-ttu-id="9cf46-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="9cf46-109">Property value</span></span>

<span data-ttu-id="9cf46-110">Ein **System. Double** -Wert, der die Wiedergabe Rate mit dem Standardwert 1,0 ist.</span><span class="sxs-lookup"><span data-stu-id="9cf46-110">A **System.Double** that is the playback rate, with a default value of 1.0.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cf46-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9cf46-111">Remarks</span></span>

<span data-ttu-id="9cf46-112">Der von dieser Eigenschaft abgerufene Wert fungiert als Multiplikatorwert, mit dem Sie ein Medien Element schneller oder langsamer wiedergeben können.</span><span class="sxs-lookup"><span data-stu-id="9cf46-112">The value retrieved by this property acts as a multiplier value that enables you to play a media item at a faster or slower rate.</span></span> <span data-ttu-id="9cf46-113">Der Standardwert 1,0 gibt die erstellte Geschwindigkeit an.</span><span class="sxs-lookup"><span data-stu-id="9cf46-113">The default value of 1.0 indicates the authored speed.</span></span>

<span data-ttu-id="9cf46-114">Beachten Sie, dass eine Audiospur bei Raten, die niedriger als 0,5 oder höher als 1,5 sind, schwer zu verstehen ist.</span><span class="sxs-lookup"><span data-stu-id="9cf46-114">Note that an audio track becomes difficult to understand at rates lower than 0.5 or higher than 1.5.</span></span> <span data-ttu-id="9cf46-115">Eine Wiedergabe Rate von 2 gibt die doppelte Geschwindigkeit der Wiedergabe an.</span><span class="sxs-lookup"><span data-stu-id="9cf46-115">A playback rate of 2 indicates twice the normal playback speed.</span></span>

<span data-ttu-id="9cf46-116">Windows Media Player versucht, die am effektivsten der folgenden vier verschiedenen Wiedergabe Modi zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9cf46-116">Windows Media Player will attempt to use the most effective of the following four different playback modes</span></span>

-   <span data-ttu-id="9cf46-117">Smooth Videowiedergabe mit gestelltem Audiobereich</span><span class="sxs-lookup"><span data-stu-id="9cf46-117">Smooth video playback with audio pitch maintained</span></span>
-   <span data-ttu-id="9cf46-118">Smooth-Videowiedergabe mit nicht gebeibehaltung audiotonhöhe</span><span class="sxs-lookup"><span data-stu-id="9cf46-118">Smooth video playback with audio pitch not maintained</span></span>
-   <span data-ttu-id="9cf46-119">Smooth Videowiedergabe ohne Audiodaten</span><span class="sxs-lookup"><span data-stu-id="9cf46-119">Smooth video playback with no audio</span></span>
-   <span data-ttu-id="9cf46-120">Keyframe-Videowiedergabe ohne Audiodaten</span><span class="sxs-lookup"><span data-stu-id="9cf46-120">Keyframe video playback with no audio</span></span>

<span data-ttu-id="9cf46-121">Der von Windows Media Player gewählte Modus hängt von zahlreichen Faktoren ab, einschließlich Dateityp und-Speicherort, Betriebssystem, Netzwerk und Server.</span><span class="sxs-lookup"><span data-stu-id="9cf46-121">The mode chosen by Windows Media Player depends on numerous factors including file type and location, operating system, network, and server.</span></span>

<span data-ttu-id="9cf46-122">Es gelten auch weitere Überlegungen, abhängig vom Format des digitalen Mediums, das zum Erstellen des Inhalts verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="9cf46-122">Other considerations apply as well, depending on the digital media format used to create the content:</span></span>

-   <span data-ttu-id="9cf46-123">**Windows Media Video (WMV) und ASF.**</span><span class="sxs-lookup"><span data-stu-id="9cf46-123">**Windows Media Video (WMV) and ASF.**</span></span> <span data-ttu-id="9cf46-124">Optimale Werte für die **Rate** -Eigenschaft liegen zwischen 1 und 10 oder zwischen 1 und 10 für Reverse-Play.</span><span class="sxs-lookup"><span data-stu-id="9cf46-124">Optimal values for the **rate** property are from 1 to 10, or from  1 to  10 for reverse play.</span></span> <span data-ttu-id="9cf46-125">Werte zwischen 0,5 und 1,0 oder zwischen-0,5 und 1,0 funktionieren möglicherweise auch in Fällen, in denen audiotonhöhe beibehalten werden kann, z. b. bei der Wiedergabe von Dateien auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="9cf46-125">Values from 0.5 to 1.0 or from -0.5 to -1.0 may also work well in cases where audio pitch can be maintained, such as when playing files located on the local computer.</span></span> <span data-ttu-id="9cf46-126">Werte mit einer absoluten Größe von mehr als 10 sind zulässig, sind jedoch nicht sehr sinnvoll.</span><span class="sxs-lookup"><span data-stu-id="9cf46-126">Values with an absolute magnitude greater than 10 are allowed, but are not very meaningful.</span></span>
-   <span data-ttu-id="9cf46-127">**Andere Videoformate.**</span><span class="sxs-lookup"><span data-stu-id="9cf46-127">**Other video formats.**</span></span> <span data-ttu-id="9cf46-128">Die **Rate** -Eigenschaft kann zwischen 0 und 9 liegen.</span><span class="sxs-lookup"><span data-stu-id="9cf46-128">The **rate** property can range from 0 to 9.</span></span> <span data-ttu-id="9cf46-129">Negative Werte sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="9cf46-129">Negative values are not allowed.</span></span> <span data-ttu-id="9cf46-130">Werte kleiner als 1 stellen eine langsame Bewegung dar.</span><span class="sxs-lookup"><span data-stu-id="9cf46-130">Values less than 1 represent slow motion.</span></span> <span data-ttu-id="9cf46-131">Werte oberhalb von 9 sind zulässig, sind jedoch nicht sehr sinnvoll.</span><span class="sxs-lookup"><span data-stu-id="9cf46-131">Values above 9 are allowed, but are not very meaningful.</span></span>

<span data-ttu-id="9cf46-132">Die **iwmpcontrols. FastForward** -Methode ändert den Wert von **Rate** in 5,0, während die **iwmpcontrols. fastreverse** -Methode den Wert von **Rate** in 5,0 ändert.</span><span class="sxs-lookup"><span data-stu-id="9cf46-132">The **IWMPControls.fastForward** method changes the value of **rate** to 5.0, while the **IWMPControls.fastReverse** method changes the value of **rate** to  5.0.</span></span>

<span data-ttu-id="9cf46-133">Die Wiedergabe Rate einiger digitaler Medienformate kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="9cf46-133">The playback rate of some digital media formats cannot be altered.</span></span> <span data-ttu-id="9cf46-134">Verwenden Sie die **iwmpsettings. IsAvailable** -Eigenschaft (in c# die **iwmpsettings. get \_ IsAvailable** -Methode), um zu ermitteln, ob diese Eigenschaft für ein bestimmtes Medien Element angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="9cf46-134">Use the **IWMPSettings.isAvailable** property (In C# the **IWMPSettings.get\_isAvailable** method) to discover whether this property can be specified for a particular media item.</span></span>

## <a name="examples"></a><span data-ttu-id="9cf46-135">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9cf46-135">Examples</span></span>

<span data-ttu-id="9cf46-136">Im folgenden Beispiel wird ein numerisches UpDown-Steuerelement verwendet, das es dem Benutzer ermöglicht, die Wiedergabegeschwindigkeit des aktuellen Mediums zu ändern.</span><span class="sxs-lookup"><span data-stu-id="9cf46-136">The following example uses a numeric updown control that allows the user to change the playback speed of the current media.</span></span> <span data-ttu-id="9cf46-137">Wenn der Benutzer auf die nach-oben-oder nach-unten-Pfeile des Steuer Elements klickt, wird die Eigenschaft **Rate** auf den neuen Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9cf46-137">When the user clicks the up or down arrows of the control, the **rate** property is set to the new value.</span></span> <span data-ttu-id="9cf46-138">Der mögliche Wertebereich im Steuerelement ist 0,5 (halbe Geschwindigkeit) bis 2,0 (doppelte Geschwindigkeit).</span><span class="sxs-lookup"><span data-stu-id="9cf46-138">The possible range of values in the control are 0.5 (half-speed) to 2.0 (double-speed).</span></span> <span data-ttu-id="9cf46-139">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="9cf46-139">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playbackRate_Click(object sender, System.EventArgs e)
{
    // Get the new value of the control, and cast it from decimal to double.
    double newRate = (double)((System.Windows.Forms.NumericUpDown)sender).Value;

    // Test whether playback rate can be set. 
    if( player.settings.get_isAvailable("Rate") )
    {
        // Set the playback rate to the new value.
        player.settings.rate = newRate;
    }
}
```


```VB

Public Sub playbackRate_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playbackRate.Click

    &#39;  Get the new value of the control as a double.
    Dim nUpDown As System.Windows.Forms.NumericUpDown = sender
    Dim newRate As Double = nUpDown.Value

    &#39;  Test whether playback rate can be set. 
    If (player.settings.isAvailable(&quot;Rate&quot;)) Then

        &#39;  Set the playback rate to the new value.
        player.settings.rate = newRate

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="9cf46-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9cf46-140">Requirements</span></span>



| <span data-ttu-id="9cf46-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9cf46-141">Requirement</span></span> | <span data-ttu-id="9cf46-142">Wert</span><span class="sxs-lookup"><span data-stu-id="9cf46-142">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cf46-143">Version</span><span class="sxs-lookup"><span data-stu-id="9cf46-143">Version</span></span><br/>   | <span data-ttu-id="9cf46-144">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="9cf46-144">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="9cf46-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="9cf46-145">Namespace</span></span><br/> | <span data-ttu-id="9cf46-146">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="9cf46-146">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="9cf46-147">Assembly</span><span class="sxs-lookup"><span data-stu-id="9cf46-147">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9cf46-148"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9cf46-148"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cf46-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9cf46-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cf46-150">**Iwmpcontrols. FastForward (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="9cf46-150">**IWMPControls.fastForward (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9cf46-151">**Iwmpcontrols. fastreverse (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="9cf46-151">**IWMPControls.fastReverse (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9cf46-152">**Iwmpsettings-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="9cf46-152">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9cf46-153">**Iwmpsettings. IsAvailable (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="9cf46-153">**IWMPSettings.isAvailable (VB and C#)**</span></span>](iwmpsettings-isavailable--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9cf46-154">**Iwmpsettings. stumm (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="9cf46-154">**IWMPSettings.mute (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> </dl>

 

 





