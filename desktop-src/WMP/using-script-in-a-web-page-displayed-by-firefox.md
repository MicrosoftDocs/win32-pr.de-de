---
title: Verwenden von Skripts in einer Webseite, die von Firefox angezeigt wird
description: Verwenden von Skripts in einer Webseite, die von Firefox angezeigt wird
ms.assetid: 0f1d21b1-1824-4ba9-9c0e-bd23ba847d9d
keywords:
- Windows Media Player, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Objektmodell, Einbetten des ActiveX-Steuer Elements
- Objektmodell, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Mobile, Einbetten des ActiveX-Steuer Elements
- Windows Media Player ActiveX-Steuerelement, einbetten
- Windows Media Player Mobile ActiveX-Steuerelement, einbetten
- ActiveX-Steuerelement, einbetten
- Windows Media Player ActiveX-Steuerelement, Webseiten
- Windows Media Player Mobile ActiveX-Steuerelement, Webseiten
- ActiveX-Steuerelement, Webseiten
- Windows Media Player ActiveX-Steuerelement, Skript Beispiel
- Windows Media Player Mobile ActiveX-Steuerelement, Skript Beispiel
- ActiveX-Steuerelement, Skript Beispiel
- Einbettungen, Webseiten
- Einbetten von Webseiten, Skript Beispiel
- Windows Media Player, Firefox
- Windows Media Player-Objektmodell, Firefox
- Objektmodell, Firefox
- Windows Media Player Mobile, Firefox
- Windows Media Player ActiveX-Steuerelement, Firefox
- Windows Media Player Mobile ActiveX-Steuerelement, Firefox
- ActiveX-Steuerelement, Firefox
- Firefox, Skript Beispiel
- Einbettung von Webseiten, Firefox
- Skript Beispiel für die Einbettung von Webseiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8629f87f954d12602999f76483fdd36ab279290
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2019
ms.locfileid: "106339848"
---
# <a name="using-script-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="98619-128">Verwenden von Skripts in einer Webseite, die von Firefox angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="98619-128">Using Script in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="98619-129">Skripts auf einer Webseite können das Player-Objektmodell verwenden, um den Player zu steuern, während der Benutzer mit der Seite interagiert.</span><span class="sxs-lookup"><span data-stu-id="98619-129">Script on a webpage can use the Player object model to control the Player as the user interacts with the page.</span></span> <span data-ttu-id="98619-130">Das folgende Eingabe Element verfügt beispielsweise über ein Skript, mit dem das Player Volume festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="98619-130">For example, the following INPUT element has script that sets the Player volume.</span></span>


```HTML
<INPUT type="button" value="Vol" OnClick="ChangeVolume()"/>
 
<SCRIPT>
  function ChangeVolume()
  {
    Player.settings.volume = 90;
  }
</SCRIPT>

```



<span data-ttu-id="98619-131">Viele der Objekte im Windows Media Player-Objektmodell werden von Internet Explorer und dem Firefox-Plug-in unterstützt.</span><span class="sxs-lookup"><span data-stu-id="98619-131">Many of the objects in the Windows Media Player object model are supported by Internet Explorer and by the Firefox plug-in.</span></span> <span data-ttu-id="98619-132">Es gibt jedoch einige Objekte, die vom Firefox-Plug-in nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="98619-132">However, there are some objects that are not supported by the Firefox plug-in.</span></span> <span data-ttu-id="98619-133">In der folgenden Tabelle werden alle Objekte im Player-Objektmodell aufgelistet, und es wird gezeigt, welche Objekte vom Firefox-Plug-in unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="98619-133">The following table lists all of the objects in the Player object model and shows which objects are supported by the Firefox plug-in.</span></span>



| <span data-ttu-id="98619-134">Object</span><span class="sxs-lookup"><span data-stu-id="98619-134">Object</span></span>                                              | <span data-ttu-id="98619-135">Firefox-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="98619-135">Firefox support</span></span> |
|-----------------------------------------------------|-----------------|
| [<span data-ttu-id="98619-136">Rom</span><span class="sxs-lookup"><span data-stu-id="98619-136">Cdrom</span></span>](cdrom-object.md)                           | <span data-ttu-id="98619-137">nein</span><span class="sxs-lookup"><span data-stu-id="98619-137">no</span></span>              |
| [<span data-ttu-id="98619-138">Cdromcollection</span><span class="sxs-lookup"><span data-stu-id="98619-138">CdromCollection</span></span>](cdromcollection-object.md)       | <span data-ttu-id="98619-139">nein</span><span class="sxs-lookup"><span data-stu-id="98619-139">no</span></span>              |
| [<span data-ttu-id="98619-140">Closedcaption</span><span class="sxs-lookup"><span data-stu-id="98619-140">ClosedCaption</span></span>](closedcaption-object.md)           | <span data-ttu-id="98619-141">ja</span><span class="sxs-lookup"><span data-stu-id="98619-141">yes</span></span>             |
| [<span data-ttu-id="98619-142">Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="98619-142">Controls</span></span>](controls-object.md)                     | <span data-ttu-id="98619-143">nein</span><span class="sxs-lookup"><span data-stu-id="98619-143">no</span></span>              |
| [<span data-ttu-id="98619-144">DVD</span><span class="sxs-lookup"><span data-stu-id="98619-144">DVD</span></span>](dvd-object.md)                               | <span data-ttu-id="98619-145">nein</span><span class="sxs-lookup"><span data-stu-id="98619-145">no</span></span>              |
| [<span data-ttu-id="98619-146">Fehler</span><span class="sxs-lookup"><span data-stu-id="98619-146">Error</span></span>](error-object.md)                           | <span data-ttu-id="98619-147">ja</span><span class="sxs-lookup"><span data-stu-id="98619-147">yes</span></span>             |
| [<span data-ttu-id="98619-148">ErrorItem</span><span class="sxs-lookup"><span data-stu-id="98619-148">ErrorItem</span></span>](erroritem-object.md)                   | <span data-ttu-id="98619-149">ja</span><span class="sxs-lookup"><span data-stu-id="98619-149">yes</span></span>             |
| [<span data-ttu-id="98619-150">Medien</span><span class="sxs-lookup"><span data-stu-id="98619-150">Media</span></span>](media-object.md)                           | <span data-ttu-id="98619-151">ja</span><span class="sxs-lookup"><span data-stu-id="98619-151">yes</span></span>             |
| [<span data-ttu-id="98619-152">Mediacollection</span><span class="sxs-lookup"><span data-stu-id="98619-152">MediaCollection</span></span>](mediacollection-object.md)       | <span data-ttu-id="98619-153">nein</span><span class="sxs-lookup"><span data-stu-id="98619-153">no</span></span>              |
| [<span data-ttu-id="98619-154">MetadataPicture</span><span class="sxs-lookup"><span data-stu-id="98619-154">MetadataPicture</span></span>](metadatapicture-object.md)       | <span data-ttu-id="98619-155">nein</span><span class="sxs-lookup"><span data-stu-id="98619-155">no</span></span>              |
| [<span data-ttu-id="98619-156">MetadataText</span><span class="sxs-lookup"><span data-stu-id="98619-156">MetadataText</span></span>](metadatatext-object.md)             | <span data-ttu-id="98619-157">nein</span><span class="sxs-lookup"><span data-stu-id="98619-157">no</span></span>              |
| [<span data-ttu-id="98619-158">Network</span><span class="sxs-lookup"><span data-stu-id="98619-158">Network</span></span>](network-object.md)                       | <span data-ttu-id="98619-159">ja</span><span class="sxs-lookup"><span data-stu-id="98619-159">yes</span></span>             |
| [<span data-ttu-id="98619-160">Player</span><span class="sxs-lookup"><span data-stu-id="98619-160">Player</span></span>](player-object.md)                         | <span data-ttu-id="98619-161">ja</span><span class="sxs-lookup"><span data-stu-id="98619-161">yes</span></span>             |
| [<span data-ttu-id="98619-162">PlayerApplication</span><span class="sxs-lookup"><span data-stu-id="98619-162">PlayerApplication</span></span>](playerapplication-object.md)   | <span data-ttu-id="98619-163">nein</span><span class="sxs-lookup"><span data-stu-id="98619-163">no</span></span>              |
| [<span data-ttu-id="98619-164">Abspielen</span><span class="sxs-lookup"><span data-stu-id="98619-164">Playlist</span></span>](playlist-object.md)                     | <span data-ttu-id="98619-165">ja</span><span class="sxs-lookup"><span data-stu-id="98619-165">yes</span></span>             |
| [<span data-ttu-id="98619-166">Playlistarray</span><span class="sxs-lookup"><span data-stu-id="98619-166">PlaylistArray</span></span>](playlistarray-object.md)           | <span data-ttu-id="98619-167">nein</span><span class="sxs-lookup"><span data-stu-id="98619-167">no</span></span>              |
| [<span data-ttu-id="98619-168">Playlistcollection</span><span class="sxs-lookup"><span data-stu-id="98619-168">PlaylistCollection</span></span>](playlistcollection-object.md) | <span data-ttu-id="98619-169">nein</span><span class="sxs-lookup"><span data-stu-id="98619-169">no</span></span>              |
| [<span data-ttu-id="98619-170">Abfrage</span><span class="sxs-lookup"><span data-stu-id="98619-170">Query</span></span>](query-object.md)                           | <span data-ttu-id="98619-171">nein</span><span class="sxs-lookup"><span data-stu-id="98619-171">no</span></span>              |
| [<span data-ttu-id="98619-172">Einstellungen</span><span class="sxs-lookup"><span data-stu-id="98619-172">Settings</span></span>](settings-object.md)                     | <span data-ttu-id="98619-173">ja</span><span class="sxs-lookup"><span data-stu-id="98619-173">yes</span></span>             |
| [<span data-ttu-id="98619-174">StringCollection</span><span class="sxs-lookup"><span data-stu-id="98619-174">StringCollection</span></span>](stringcollection-object.md)     | <span data-ttu-id="98619-175">nein</span><span class="sxs-lookup"><span data-stu-id="98619-175">no</span></span>              |



 

<span data-ttu-id="98619-176">Das Firefox-Plug-in unterstützt das **Player** -Objekt, aber bestimmte Eigenschaften des **Player** -Objekts geben **null** in einem Firefox-Browser zurück.</span><span class="sxs-lookup"><span data-stu-id="98619-176">The Firefox plug-in supports the **Player** object, but certain properties of the **Player** object return **NULL** in a Firefox browser.</span></span> <span data-ttu-id="98619-177">Beispielsweise gibt die [cdromcollection](player-cdromcollection.md) -Eigenschaft des **Player** -Objekts den Wert **null** zurück, da das Firefox-Plug-in das **CDROM** -Objekt nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="98619-177">For example, the [cdromCollection](player-cdromcollection.md) property of the **Player** object returns **NULL** because the Firefox plug-in does not support the **Cdrom** object.</span></span> <span data-ttu-id="98619-178">Ebenso geben die Eigenschaften " [DVD](player-dvd.md)", " [mediacollection](player-mediacollection.md)", " [playerapplication](player-playerapplication.md)" und " [playlistcollection](player-playlistcollection.md) " des **Player** -Objekts in einem Firefox-Browser den Wert **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="98619-178">Similarly, the [dvd](player-dvd.md), [mediaCollection](player-mediacollection.md), [playerApplication](player-playerapplication.md), and [playlistCollection](player-playlistcollection.md) properties of the **Player** object return **NULL** in a Firefox browser.</span></span>

<span data-ttu-id="98619-179">Die **Player. pluginversioninfo** -Eigenschaft wird vom Firefox-Plug-in, aber nicht von Internet Explorer unterstützt.</span><span class="sxs-lookup"><span data-stu-id="98619-179">The **Player.pluginVersionInfo** property is supported by the Firefox plug-in but not by Internet Explorer.</span></span> <span data-ttu-id="98619-180">Diese Eigenschaft gibt die Version des Firefox-Plug-ins zurück.</span><span class="sxs-lookup"><span data-stu-id="98619-180">This property returns the version of the Firefox plug-in.</span></span>

<span data-ttu-id="98619-181">Das Firefox-Plug-in unterstützt das **Medien** Objekt, einschließlich der [getItemInfoByType](media-getiteminfobytype.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="98619-181">The Firefox plug-in supports the **Media** object, including the [getItemInfoByType](media-getiteminfobytype.md) property.</span></span> <span data-ttu-id="98619-182">In einem Firefox-Browser unterstützt die **getItemInfoByType** -Eigenschaft jedoch nicht die Rückgabe Typen **MetadataText** und **MetadataPicture** .</span><span class="sxs-lookup"><span data-stu-id="98619-182">However, in a Firefox browser, the **getItemInfoByType** property does not support the **MetadataText** and **MetadataPicture** return types.</span></span>

<span data-ttu-id="98619-183">Das Firefox-Plug-in unterstützt das [Einstellungs](settings-object.md) Objekt außer der [setmode](settings-setmode.md) -Methode und der [requestmediaaccessrights](settings-requestmediaaccessrights.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="98619-183">The Firefox plug-in supports the [Settings](settings-object.md) object except for the [setMode](settings-setmode.md) method and the [requestMediaAccessRights](settings-requestmediaaccessrights.md) property.</span></span> <span data-ttu-id="98619-184">In einem Firefox-Browser gibt die **requestmediaaccessright** -Eigenschaft immer false zurück.</span><span class="sxs-lookup"><span data-stu-id="98619-184">In a Firefox browser, the **requestMediaAccessRight** property always returns false.</span></span>

## <a name="related-topics"></a><span data-ttu-id="98619-185">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="98619-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98619-186">**Verwenden des Windows Media Player-Steuer Elements mit Firefox**</span><span class="sxs-lookup"><span data-stu-id="98619-186">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




