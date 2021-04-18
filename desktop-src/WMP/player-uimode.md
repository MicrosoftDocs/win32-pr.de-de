---
title: Player. uiMode
description: Mit der uiMode-Eigenschaft wird ein Wert angegeben oder abgerufen, der angibt, welche Steuerelemente in der Benutzeroberfläche angezeigt werden.
ms.assetid: 6297d22b-e8ed-4f28-83f6-b74d3265c520
keywords:
- Player. uiMode-Windows-Media Player
topic_type:
- apiref
api_name:
- Player.uiMode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b1fd2e8e3a2ac6314255cd6ebc350b2ace8cb63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357639"
---
# <a name="playeruimode"></a><span data-ttu-id="17ba6-104">Player. uiMode</span><span class="sxs-lookup"><span data-stu-id="17ba6-104">Player.uiMode</span></span>

<span data-ttu-id="17ba6-105">Mit der **uiMode** -Eigenschaft wird ein Wert angegeben oder abgerufen, der angibt, welche Steuerelemente in der Benutzeroberfläche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="17ba6-105">The **uiMode** property specifies or retrieves a value indicating which controls are shown in the user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="17ba6-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="17ba6-106">Syntax</span></span>

<span data-ttu-id="17ba6-107">*Player* . **uiMode**</span><span class="sxs-lookup"><span data-stu-id="17ba6-107">*player* .**uiMode**</span></span>

## <a name="possible-values"></a><span data-ttu-id="17ba6-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="17ba6-108">Possible Values</span></span>

<span data-ttu-id="17ba6-109">Diese Eigenschaft ist eine Lese- **/schreibzeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="17ba6-109">This property is a read/write **String**.</span></span>



| <span data-ttu-id="17ba6-110">Wert</span><span class="sxs-lookup"><span data-stu-id="17ba6-110">Value</span></span>     | <span data-ttu-id="17ba6-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17ba6-111">Description</span></span>                                                                                                                                                                                                           | <span data-ttu-id="17ba6-112">Audiobeispiel</span><span class="sxs-lookup"><span data-stu-id="17ba6-112">Audio Example</span></span>                                          | <span data-ttu-id="17ba6-113">Video Beispiel</span><span class="sxs-lookup"><span data-stu-id="17ba6-113">Video Example</span></span>                                          |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="17ba6-114">Unsichtbar</span><span class="sxs-lookup"><span data-stu-id="17ba6-114">invisible</span></span> | <span data-ttu-id="17ba6-115">Windows Media Player ist ohne sichtbare Benutzeroberfläche eingebettet (Steuerelemente, Video-oder Visualisierungs Fenster).</span><span class="sxs-lookup"><span data-stu-id="17ba6-115">Windows Media Player is embedded without any visible user interface (controls, video or visualization window).</span></span>                                                                                                        | <span data-ttu-id="17ba6-116">(Nichts wird angezeigt.)</span><span class="sxs-lookup"><span data-stu-id="17ba6-116">(Nothing is displayed.)</span></span>                                | <span data-ttu-id="17ba6-117">(Nichts wird angezeigt.)</span><span class="sxs-lookup"><span data-stu-id="17ba6-117">(Nothing is displayed.)</span></span>                                |
| <span data-ttu-id="17ba6-118">none</span><span class="sxs-lookup"><span data-stu-id="17ba6-118">none</span></span>      | <span data-ttu-id="17ba6-119">Windows Media Player ist ohne Steuerelemente eingebettet, und nur das Video-oder Visualisierungs Fenster wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="17ba6-119">Windows Media Player is embedded without controls, and with only the video or visualization window displayed.</span></span>                                                                                                         | !["None" mit Audiodaten](images/uimode-none-audio-v11.png) | !["None" mit Video](images/uimode-none-video-v11.png) |
| <span data-ttu-id="17ba6-122">Minibar</span><span class="sxs-lookup"><span data-stu-id="17ba6-122">mini</span></span>      | <span data-ttu-id="17ba6-123">Windows Media Player ist in das Fenster "Status", "Wiedergabe", "anhalten", "anhalten", "stumm" und "Lautstärke" neben dem Video-oder Visualisierungs Fenster eingebettet</span><span class="sxs-lookup"><span data-stu-id="17ba6-123">Windows Media Player is embedded with the status window, play/pause, stop, mute, and volume controls shown in addition to the video or visualization window.</span></span>                                                          | !["Mini" mit Audiodaten](images/uimode-mini-audio-v11.png) | !["Mini" mit Video](images/uimode-mini-video-v11.png) |
| <span data-ttu-id="17ba6-126">Voll</span><span class="sxs-lookup"><span data-stu-id="17ba6-126">full</span></span>      | <span data-ttu-id="17ba6-127">Standard.</span><span class="sxs-lookup"><span data-stu-id="17ba6-127">Default.</span></span> <span data-ttu-id="17ba6-128">Windows Media Player ist neben dem Video-oder Visualisierungs Fenster in die Steuerelemente "Status", "suchen", "Wiedergabe", "anhalten", "stumm Schaltung", "weiter", "schnell vorwärts", "schnelles umkehren" und "Handels@@</span><span class="sxs-lookup"><span data-stu-id="17ba6-128">Windows Media Player is embedded with the status window, seek bar, play/pause, stop, mute, next, previous, fast forward, fast reverse, and volume controls in addition to the video or visualization window.</span></span> | !["Full" mit Audiodaten](images/uimode-full-audio-v11.png) | !["Full" mit Video](images/uimode-full-video-v11.png) |
| <span data-ttu-id="17ba6-131">custom</span><span class="sxs-lookup"><span data-stu-id="17ba6-131">custom</span></span>    | <span data-ttu-id="17ba6-132">Windows Media Player ist mit einer benutzerdefinierten Benutzeroberfläche eingebettet.</span><span class="sxs-lookup"><span data-stu-id="17ba6-132">Windows Media Player is embedded with a custom user interface.</span></span> <span data-ttu-id="17ba6-133">Kann nur in C++-Programmen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17ba6-133">Can only be used in C++ programs.</span></span>                                                                                                                      | <span data-ttu-id="17ba6-134">(Benutzerdefinierte Benutzeroberfläche wird angezeigt.)</span><span class="sxs-lookup"><span data-stu-id="17ba6-134">(Custom user interface is displayed.)</span></span>                  | <span data-ttu-id="17ba6-135">(Benutzerdefinierte Benutzeroberfläche wird angezeigt.)</span><span class="sxs-lookup"><span data-stu-id="17ba6-135">(Custom user interface is displayed.)</span></span>                  |



 

## <a name="remarks"></a><span data-ttu-id="17ba6-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17ba6-136">Remarks</span></span>

<span data-ttu-id="17ba6-137">Diese Eigenschaft gibt die Darstellung der eingebetteten Windows-Media Player an.</span><span class="sxs-lookup"><span data-stu-id="17ba6-137">This property specifies the appearance of the embedded Windows Media Player.</span></span> <span data-ttu-id="17ba6-138">Wenn **uiMode** auf "None", "Mini" oder "Full" festgelegt ist, ist ein Fenster für die Anzeige von Videoclips und Audiovisualisierungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="17ba6-138">When **uiMode** is set to "none", "mini", or "full", a window is present for the display of video clips and audio visualizations.</span></span> <span data-ttu-id="17ba6-139">Dieses Fenster kann im Mini-oder vollständigen Modus ausgeblendet werden, indem das **height** -Attribut des **Object** -Tags auf 40 festgelegt wird. dieses Fenster wird von unten gemessen und lässt den Steuerelement Teil der Benutzeroberfläche sichtbar.</span><span class="sxs-lookup"><span data-stu-id="17ba6-139">This window can be hidden in mini or full mode by setting the **height** attribute of the **OBJECT** tag to 40, which is measured from the bottom, and leaves the controls portion of the user interface visible.</span></span> <span data-ttu-id="17ba6-140">Wenn keine eingebettete Schnittstelle gewünscht ist, legen Sie die Attribute " **Width** " und " **height** " auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="17ba6-140">If no embedded interface is desired, set both the **width** and **height** attributes to zero.</span></span>

<span data-ttu-id="17ba6-141">Wenn **uiMode** auf "unsichtbar" festgelegt ist, wird keine Benutzeroberfläche angezeigt, aber der Leerraum ist nach wie vor durch **Breite** und **Höhe** angegeben.</span><span class="sxs-lookup"><span data-stu-id="17ba6-141">If **uiMode** is set to "invisible", no user interface is displayed, but space is still reserved on the page as specified by **width** and **height**.</span></span> <span data-ttu-id="17ba6-142">Dies ist nützlich, um das Seitenlayout beizubehalten, wenn **uiMode** geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="17ba6-142">This is useful for retaining page layout when **uiMode** can change.</span></span> <span data-ttu-id="17ba6-143">Außerdem ist der reservierte Speicherplatz transparent, sodass alle Elemente hinter dem Steuerelement sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="17ba6-143">Additionally, the reserved space is transparent, so any elements layered behind the control will be visible.</span></span>

<span data-ttu-id="17ba6-144">Wenn **uiMode** auf "Full" oder "Mini" festgelegt ist, zeigt Windows Media Player Transport Steuerelemente im Vollbildmodus an.</span><span class="sxs-lookup"><span data-stu-id="17ba6-144">If **uiMode** is set to "full" or "mini", Windows Media Player displays transport controls in full-screen mode.</span></span> <span data-ttu-id="17ba6-145">Wenn **uiMode** auf "None" festgelegt ist, werden keine Steuerelemente im Vollbildmodus angezeigt.</span><span class="sxs-lookup"><span data-stu-id="17ba6-145">If **uiMode** is set to "none", no controls are displayed in full-screen mode.</span></span>

<span data-ttu-id="17ba6-146">Wenn das Fenster sichtbar ist und Audioinhalt wiedergegeben wird, wird die Visualisierung angezeigt, die zuletzt in Windows Media Player verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="17ba6-146">If the window is visible and audio content is being played, the visualization displayed will be the one most recently used in Windows Media Player.</span></span>

<span data-ttu-id="17ba6-147">Wenn **uiMode** in einem C++-Programm, das **iwmpremotemediaservices** implementiert, auf "Custom" festgelegt ist, wird die von **iwmpremotemediaservices:: getcustomuimode** angezeigte Skin-Datei angezeigt.</span><span class="sxs-lookup"><span data-stu-id="17ba6-147">If **uiMode** is set to "custom" in a C++ program that implements **IWMPRemoteMediaServices**, the skin file indicated by **IWMPRemoteMediaServices::GetCustomUIMode** is displayed.</span></span>

<span data-ttu-id="17ba6-148">Während der Vollbildwiedergabe blendet Windows Media Player den Mauszeiger aus, wenn **enablecontextmenu** den Wert false hat und **uiMode** den Wert "None" hat.</span><span class="sxs-lookup"><span data-stu-id="17ba6-148">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

## <a name="examples"></a><span data-ttu-id="17ba6-149">Beispiele</span><span class="sxs-lookup"><span data-stu-id="17ba6-149">Examples</span></span>

<span data-ttu-id="17ba6-150">Im folgenden Beispiel wird ein HTML-SELECT-Element erstellt, das es dem Benutzer ermöglicht, die Benutzeroberfläche für ein eingebettetes **Player** -Objekt zu ändern.</span><span class="sxs-lookup"><span data-stu-id="17ba6-150">The following example creates an HTML SELECT element that allows the user to change the user interface for an embedded **Player** object.</span></span> <span data-ttu-id="17ba6-151">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="17ba6-151">The **Player** object was created with ID = "Player".</span></span>


```
<!-- Create an HTML SELECT element. -->
<SELECT  ID = UI  LANGUAGE="JScript"

         /* Specify the UI mode the user selects. */
         onChange = "Player.uiMode = UI.value">

/* These are the four UI mode options. */
<OPTION VALUE="invisible">Invisible
<OPTION VALUE="none">No Controls
<OPTION VALUE="mini">Mini Player
<OPTION VALUE="full">Full Player
</SELECT>

```



<span data-ttu-id="17ba6-152">Windows Media Player 10 Mobile: Diese Eigenschaft akzeptiert nur die Werte "None" oder "Full" oder gibt Sie zurück.</span><span class="sxs-lookup"><span data-stu-id="17ba6-152">Windows Media Player 10 Mobile: This property only accepts or returns values of "none" or "full".</span></span> <span data-ttu-id="17ba6-153">Auf Smartphone-Geräten werden nur Wiedergabe Status und ein Counter angezeigt, wenn *uiMode* auf "Full" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="17ba6-153">On Smartphone devices, only playback status and a counter are displayed when *uiMode* is set to "full".</span></span>

## <a name="requirements"></a><span data-ttu-id="17ba6-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17ba6-154">Requirements</span></span>



| <span data-ttu-id="17ba6-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17ba6-155">Requirement</span></span> | <span data-ttu-id="17ba6-156">Wert</span><span class="sxs-lookup"><span data-stu-id="17ba6-156">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17ba6-157">Version</span><span class="sxs-lookup"><span data-stu-id="17ba6-157">Version</span></span><br/> | <span data-ttu-id="17ba6-158">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="17ba6-158">Windows Media Player version 7.0 or later.</span></span> <span data-ttu-id="17ba6-159">Windows Media Player 9 oder höher für "unsichtbar" oder "Benutzer definiert".</span><span class="sxs-lookup"><span data-stu-id="17ba6-159">Windows Media Player 9 Series or later for "invisible" or "custom".</span></span><br/> |
| <span data-ttu-id="17ba6-160">DLL</span><span class="sxs-lookup"><span data-stu-id="17ba6-160">DLL</span></span><br/>     | <dl> <span data-ttu-id="17ba6-161"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17ba6-161"><dt>Wmp.dll</dt></span></span> </dl>                                        |



## <a name="see-also"></a><span data-ttu-id="17ba6-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17ba6-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17ba6-163">**Iwmpremotemediaservices-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="17ba6-163">**IWMPRemoteMediaServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
</dt> <dt>

[<span data-ttu-id="17ba6-164">**Iwmpremotemediaservices:: getcustomuimode**</span><span class="sxs-lookup"><span data-stu-id="17ba6-164">**IWMPRemoteMediaServices::GetCustomUIMode**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getcustomuimode)
</dt> <dt>

[<span data-ttu-id="17ba6-165">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="17ba6-165">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





