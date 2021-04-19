---
title: AxWindowsMediaPlayer. uiMode (Eigenschaft)
description: Mit der uiMode-Eigenschaft wird ein Wert abgerufen oder festgelegt, der angibt, welche Steuerelemente in der Benutzeroberfläche angezeigt werden.
ms.assetid: 01034418-be70-44f3-8812-e529c747c9e4
keywords:
- uiMode-Eigenschaften Fenster Media Player
- uiMode-Eigenschaft, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, uiMode-Eigenschaft
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.uiMode
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33edcf6bdff9e1587269df9eb49c3729099d091e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361390"
---
# <a name="axwindowsmediaplayeruimode-property"></a><span data-ttu-id="0939b-106">AxWindowsMediaPlayer. uiMode (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0939b-106">AxWindowsMediaPlayer.uiMode property</span></span>

<span data-ttu-id="0939b-107">Mit der uiMode-Eigenschaft wird ein Wert abgerufen oder festgelegt, der angibt, welche Steuerelemente in der Benutzeroberfläche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="0939b-107">The uiMode property gets or sets a value indicating which controls are shown in the user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="0939b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0939b-108">Syntax</span></span>


```CSharp
public System.String uiMode {get; set;}
```


```VB

Public Property uiMode As System.String
```





## <a name="property-value"></a><span data-ttu-id="0939b-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0939b-109">Property value</span></span>

<span data-ttu-id="0939b-110">Ein System. String-Wert, der einem der folgenden Werte entspricht.</span><span class="sxs-lookup"><span data-stu-id="0939b-110">A System.String that is one of the following values.</span></span>



| <span data-ttu-id="0939b-111">Wert</span><span class="sxs-lookup"><span data-stu-id="0939b-111">Value</span></span>     | <span data-ttu-id="0939b-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0939b-112">Description</span></span>                                                                                                                                                                                                     | <span data-ttu-id="0939b-113">Audiobeispiel</span><span class="sxs-lookup"><span data-stu-id="0939b-113">Audio example</span></span>                                                   | <span data-ttu-id="0939b-114">Video Beispiel</span><span class="sxs-lookup"><span data-stu-id="0939b-114">Video example</span></span>                                                   |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="0939b-115">Unsichtbar</span><span class="sxs-lookup"><span data-stu-id="0939b-115">invisible</span></span> | <span data-ttu-id="0939b-116">Windows Media Player ist ohne sichtbare Benutzeroberfläche eingebettet (Steuerelemente, Video-oder Visualisierungs Fenster).</span><span class="sxs-lookup"><span data-stu-id="0939b-116">Windows Media Player is embedded without any visible user interface (controls, video or visualization window).</span></span>                                                                                                  | <span data-ttu-id="0939b-117">(Nichts wird angezeigt.)</span><span class="sxs-lookup"><span data-stu-id="0939b-117">(Nothing is displayed.)</span></span>                                         | <span data-ttu-id="0939b-118">(Nichts wird angezeigt.)</span><span class="sxs-lookup"><span data-stu-id="0939b-118">(Nothing is displayed.)</span></span>                                         |
| <span data-ttu-id="0939b-119">none</span><span class="sxs-lookup"><span data-stu-id="0939b-119">none</span></span>      | <span data-ttu-id="0939b-120">Windows Media Player ist ohne Steuerelemente eingebettet, und nur das Video-oder Visualisierungs Fenster wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0939b-120">Windows Media Player is embedded without controls, and with only the video or visualization window displayed.</span></span>                                                                                                   | ![uiMode = ' none ' with Audiodatei](images/uimode-none-audio-v11.png) | ![uiMode = ' none ' mit Video](images/uimode-none-video-v11.png) |
| <span data-ttu-id="0939b-123">Minibar</span><span class="sxs-lookup"><span data-stu-id="0939b-123">mini</span></span>      | <span data-ttu-id="0939b-124">Windows Media Player ist in das Fenster "Status", "Wiedergabe", "anhalten", "anhalten", "stumm" und "Lautstärke" neben dem Video-oder Visualisierungs Fenster eingebettet</span><span class="sxs-lookup"><span data-stu-id="0939b-124">Windows Media Player is embedded with the status window, play/pause, stop, mute, and volume controls shown in addition to the video or visualization window.</span></span>                                                    | ![uiMode = ' Mini ' mit Audiodatei](images/uimode-mini-audio-v11.png) | ![uiMode = ' Mini ' mit Video](images/uimode-mini-video-v11.png) |
| <span data-ttu-id="0939b-127">Voll</span><span class="sxs-lookup"><span data-stu-id="0939b-127">full</span></span>      | <span data-ttu-id="0939b-128">Standard.</span><span class="sxs-lookup"><span data-stu-id="0939b-128">Default.</span></span> <span data-ttu-id="0939b-129">Windows Media Player ist neben dem Video-oder Visualisierungs Fenster in die Steuerelemente "Status", "suchen", "Wiedergabe", "anhalten", "stumm Schaltung", "weiter", "zurück", "Zurückspulen" und "Volume" eingebettet</span><span class="sxs-lookup"><span data-stu-id="0939b-129">Windows Media Player is embedded with the status window, seek bar, play/pause, stop, mute, next, previous, fast forward, rewind, and volume controls in addition to the video or visualization window.</span></span> | ![uiMode = ' Full ' mit Audiodatei](images/uimode-full-audio-v11.png) | ![uiMode = ' Full ' mit Video](images/uimode-full-video-v11.png) |
| <span data-ttu-id="0939b-132">custom</span><span class="sxs-lookup"><span data-stu-id="0939b-132">custom</span></span>    | <span data-ttu-id="0939b-133">Windows Media Player ist mit einer benutzerdefinierten Benutzeroberfläche eingebettet.</span><span class="sxs-lookup"><span data-stu-id="0939b-133">Windows Media Player is embedded with a custom user interface.</span></span> <span data-ttu-id="0939b-134">Kann nur in C++-Programmen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0939b-134">Can only be used in C++ programs.</span></span>                                                                                                                | <span data-ttu-id="0939b-135">(Benutzerdefinierte Benutzeroberfläche wird angezeigt.)</span><span class="sxs-lookup"><span data-stu-id="0939b-135">(Custom user interface is displayed.)</span></span>                           | <span data-ttu-id="0939b-136">(Benutzerdefinierte Benutzeroberfläche wird angezeigt.)</span><span class="sxs-lookup"><span data-stu-id="0939b-136">(Custom user interface is displayed.)</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="0939b-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0939b-137">Remarks</span></span>

<span data-ttu-id="0939b-138">Diese Eigenschaft gibt die Darstellung der eingebetteten Windows-Media Player an.</span><span class="sxs-lookup"><span data-stu-id="0939b-138">This property specifies the appearance of the embedded Windows Media Player.</span></span> <span data-ttu-id="0939b-139">Wenn **uiMode** auf "None", "Mini" oder "Full" festgelegt ist, ist ein Fenster für die Anzeige von Videoclips und Audiovisualisierungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0939b-139">When **uiMode** is set to "none", "mini", or "full", a window is present for the display of video clips and audio visualizations.</span></span> <span data-ttu-id="0939b-140">Dieses Fenster kann im Mini-oder vollständigen Modus ausgeblendet werden, indem das **height** -Attribut des **Object** -Tags auf 40 festgelegt wird. dieses Fenster wird von unten gemessen und lässt den Steuerelement Teil der Benutzeroberfläche sichtbar.</span><span class="sxs-lookup"><span data-stu-id="0939b-140">This window can be hidden in mini or full mode by setting the **height** attribute of the **OBJECT** tag to 40, which is measured from the bottom, and leaves the controls portion of the user interface visible.</span></span> <span data-ttu-id="0939b-141">Wenn keine eingebettete Schnittstelle gewünscht ist, legen Sie die Attribute " **Width** " und " **height** " auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="0939b-141">If no embedded interface is desired, set both the **width** and **height** attributes to zero.</span></span>

<span data-ttu-id="0939b-142">Wenn **uiMode** auf "unsichtbar" festgelegt ist, wird keine Benutzeroberfläche angezeigt, aber der Leerraum ist nach wie vor durch **Breite** und **Höhe** angegeben.</span><span class="sxs-lookup"><span data-stu-id="0939b-142">If **uiMode** is set to "invisible", no user interface is displayed, but space is still reserved on the page as specified by **width** and **height**.</span></span> <span data-ttu-id="0939b-143">Dies ist nützlich, um das Seitenlayout beizubehalten, wenn **uiMode** geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="0939b-143">This is useful for retaining page layout when **uiMode** can change.</span></span> <span data-ttu-id="0939b-144">Außerdem ist der reservierte Speicherplatz transparent, sodass alle Elemente hinter dem Steuerelement sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="0939b-144">Additionally, the reserved space is transparent, so any elements layered behind the control will be visible.</span></span>

<span data-ttu-id="0939b-145">Wenn **uiMode** auf "Full" oder "Mini" festgelegt ist, zeigt Windows Media Player Transport Steuerelemente im Vollbildmodus an.</span><span class="sxs-lookup"><span data-stu-id="0939b-145">If **uiMode** is set to "full" or "mini", Windows Media Player displays transport controls in full-screen mode.</span></span> <span data-ttu-id="0939b-146">Wenn **uiMode** auf "None" festgelegt ist, werden keine Steuerelemente im Vollbildmodus angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0939b-146">If **uiMode** is set to "none", no controls are displayed in full-screen mode.</span></span>

<span data-ttu-id="0939b-147">Wenn das Fenster sichtbar ist und Audioinhalt wiedergegeben wird, wird die Visualisierung angezeigt, die zuletzt in Windows Media Player verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="0939b-147">If the window is visible and audio content is being played, the visualization displayed will be the one most recently used in Windows Media Player.</span></span>

<span data-ttu-id="0939b-148">Wenn **uiMode** in einem C++-Programm, das **iwmpremotemediaservices** implementiert, auf "Custom" festgelegt ist, wird die von **iwmpremotemediaservices. getcustomuimode** angezeigte Skin-Datei angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0939b-148">If **uiMode** is set to "custom" in a C++ program that implements **IWMPRemoteMediaServices**, the skin file indicated by **IWMPRemoteMediaServices.GetCustomUIMode** is displayed.</span></span>

<span data-ttu-id="0939b-149">Während der Vollbildwiedergabe blendet Windows Media Player den Mauszeiger aus, wenn **enablecontextmenu** den Wert false hat und **uiMode** den Wert "None" hat.</span><span class="sxs-lookup"><span data-stu-id="0939b-149">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

## <a name="examples"></a><span data-ttu-id="0939b-150">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0939b-150">Examples</span></span>

<span data-ttu-id="0939b-151">Im folgenden Beispiel wird ein Listenfeld erstellt, das es dem Benutzer ermöglicht, den Benutzeroberflächen Modus für ein eingebettetes Windows-Media Player Objekt zu ändern.</span><span class="sxs-lookup"><span data-stu-id="0939b-151">The following example creates a list box that allows the user to change the user interface mode for an embedded Windows Media Player object.</span></span> <span data-ttu-id="0939b-152">Das AxWMPLib. AxWindowsMediaPlayer-Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0939b-152">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Load the list box with the four UI mode options.
uiModeOptions.Items.Add("invisible");
uiModeOptions.Items.Add("none");
uiModeOptions.Items.Add("mini");
uiModeOptions.Items.Add("full");


private void uiModeOptions_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    // Get the selected UI mode in the list box as a string.
    string newMode = (string)(((System.Windows.Forms.ListBox)sender).SelectedItem);
     
    // Set the UI mode that the user selected.
    player.uiMode = newMode;            
}
```


```VB

' Load the list box with the four UI mode options.
uiModeOptions.Items.Add(&quot;invisible&quot;)
uiModeOptions.Items.Add(&quot;none&quot;)
uiModeOptions.Items.Add(&quot;mini&quot;)
uiModeOptions.Items.Add(&quot;full&quot;)


Public Sub uiModeOptions_OnSelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles uiModeOptions.SelectedIndexChanged

    &#39; Get the selected UI mode in the list box as a string.
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim newMode As String = lb.SelectedItem

    &#39; Set the UI mode that the user selected.
    player.uiMode = newMode

End Sub
```





## <a name="requirements"></a><span data-ttu-id="0939b-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0939b-153">Requirements</span></span>



| <span data-ttu-id="0939b-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0939b-154">Requirement</span></span> | <span data-ttu-id="0939b-155">Wert</span><span class="sxs-lookup"><span data-stu-id="0939b-155">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0939b-156">Version</span><span class="sxs-lookup"><span data-stu-id="0939b-156">Version</span></span><br/>   | <span data-ttu-id="0939b-157">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="0939b-157">Windows Media Player version 7.0 or later.</span></span> <span data-ttu-id="0939b-158">Windows Media Player 9 oder höher für "unsichtbar" oder "Benutzer definiert"</span><span class="sxs-lookup"><span data-stu-id="0939b-158">Windows Media Player 9 Series or later for "invisible" or "custom"</span></span><br/>   |
| <span data-ttu-id="0939b-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="0939b-159">Namespace</span></span><br/> | <span data-ttu-id="0939b-160">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="0939b-160">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="0939b-161">Assembly</span><span class="sxs-lookup"><span data-stu-id="0939b-161">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0939b-162"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0939b-162"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0939b-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0939b-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0939b-164">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0939b-164">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0939b-165">**AxWindowsMediaPlayer. enablecontextmenu (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0939b-165">**AxWindowsMediaPlayer.enableContextMenu (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md)
</dt> </dl>

 

 





