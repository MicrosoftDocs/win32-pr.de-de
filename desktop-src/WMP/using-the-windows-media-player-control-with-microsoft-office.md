---
title: Verwenden des Windows Media Player-Steuer Elements mit Microsoft Office
description: Verwenden des Windows Media Player-Steuer Elements mit Microsoft Office
ms.assetid: bc7b2623-8e6d-4af6-b4d0-8087c0159273
keywords:
- Windows Media Player, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Objektmodell, Einbetten des ActiveX-Steuer Elements
- Objektmodell, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Mobile, Einbetten des ActiveX-Steuer Elements
- Windows Media Player ActiveX-Steuerelement, einbetten
- Windows Media Player Mobile ActiveX-Steuerelement, einbetten
- ActiveX-Steuerelement, einbetten
- Windows Media Player, Office
- Windows Media Player-Objektmodell, Office
- Objektmodell, Office
- Windows Media Player Mobile, Office
- Windows Media Player ActiveX-Steuerelement, Office
- Windows Media Player Mobile ActiveX-Steuerelement, Office
- ActiveX-Steuerelement, Office
- Office-Dokument Einbettung
- einbetten, Office-Dokumente
- Windows Media Player ActiveX-Steuerelement, Excel
- Windows Media Player Mobile ActiveX-Steuerelement, Excel
- ActiveX-Steuerelement, Excel
- einbetten, Excel-Kalkulations Tabellen
- Einbettung von Excel-Tabellen
- Windows Media Player ActiveX-Steuerelement, PowerPoint
- Windows Media Player Mobile ActiveX-Steuerelement, PowerPoint
- ActiveX-Steuerelement, PowerPoint
- einbetten, PowerPoint-Folien anzeigen
- PowerPoint-Folien Anzeige Einbettung
- Windows Media Player ActiveX-Steuerelement, Word
- Windows Media Player Mobile ActiveX-Steuerelement, Word
- ActiveX-Steuerelement, Word
- Wort Papier Einbettung
- einbetten, Word-Dokumente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2504b46b4fb409dede108c41b43014c3aaeae5ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947776"
---
# <a name="using-the-windows-media-player-control-with-microsoft-office"></a><span data-ttu-id="7baf4-134">Verwenden des Windows Media Player-Steuer Elements mit Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="7baf4-134">Using the Windows Media Player Control with Microsoft Office</span></span>

<span data-ttu-id="7baf4-135">In diesem Abschnitt wird beschrieben, wie Sie das ActiveX-Steuerelement Windows Media Player 9 oder höher in verschiedene Dokumente einbetten, die mit Microsoft Office XP erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="7baf4-135">This section describes how to embed the Windows Media Player 9 Series or later ActiveX control in various documents created using Microsoft Office XP.</span></span>

<span data-ttu-id="7baf4-136">In den® von Microsoft Word, Excel und PowerPoint Betten Sie das Steuerelement ein, indem Sie im Menü **Einfügen** die Option **Objekt** auswählen und dann **Windows Media Player** aus der Liste der verfügbaren Objekttypen auswählen.</span><span class="sxs-lookup"><span data-stu-id="7baf4-136">In Microsoft Word, Excel, and PowerPoint®, you embed the control by selecting **Object** from the **Insert** menu, then choosing **Windows Media Player** from the list of available object types.</span></span> <span data-ttu-id="7baf4-137">Das Windows Media Player-Steuerelement wird im Dokument am aktuellen Speicherort angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7baf4-137">The Windows Media Player control appears in the document at the current location.</span></span> <span data-ttu-id="7baf4-138">Anschließend können Sie im Kontextmenü des-Steuer Elements **Format Control** ( **Format Objekt** in Excel) auswählen, um Layout, Text Wrapping Stil und andere Format Optionen anzupassen.</span><span class="sxs-lookup"><span data-stu-id="7baf4-138">You can then select **Format Control** ( **Format Object** in Excel) from the shortcut menu for the control to adjust the layout, text wrapping style, and other format options.</span></span> <span data-ttu-id="7baf4-139">In Word und Excel müssen Sie zu diesem Zweck den Entwurfs Modus verwenden.</span><span class="sxs-lookup"><span data-stu-id="7baf4-139">In Word and Excel, you must be in design mode to do this.</span></span>

<span data-ttu-id="7baf4-140">Nachdem Sie das Steuerelement positioniert und formatiert haben, können Sie es mithilfe des Dialog Felds **Eigenschaften** konfigurieren, das über die **Steuer** Element-Toolbox oder über das Kontextmenü im Entwurfs Modus für Word und Excel zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="7baf4-140">Once you have positioned and formatted the control, you can configure it using the **Properties** dialog box, which is accessible from the **Control Toolbox** or from the shortcut menu in design mode for Word and Excel.</span></span> <span data-ttu-id="7baf4-141">Hier können Sie grundlegende Player-Steuerelement Eigenschaften angeben, z. b. den Namen des Steuer Elements, die URL einer digitalen Mediendatei und den Benutzeroberflächen Modus.</span><span class="sxs-lookup"><span data-stu-id="7baf4-141">Here you can specify basic Player control properties such as the control name, the URL of a digital media file, and the user interface mode.</span></span> <span data-ttu-id="7baf4-142">Wenn die **uiMode** -Eigenschaft auf "None" festgelegt wird, werden alle Elemente im Steuerelement mit Ausnahme des Videos oder Visualisierungs Fensters ausgeblendet, sodass Sie eigene Schaltflächen hinzufügen und Skriptcode mithilfe Visual Basic for Applications (VBA) schreiben können, um die Schaltflächen Klicks und Player-Steuerelement Ereignisse zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="7baf4-142">Setting the **uiMode** property to "none" hides everything in the control except the video or visualization window, allowing you to add your own buttons and write script code using Visual Basic for Applications (VBA) to handle the button clicks and Player control events.</span></span>

<span data-ttu-id="7baf4-143">Im Dialogfeld "grundlegende **Eigenschaften** " können Sie auch auf das Dialogfeld "anspruchsvollere **Eigenschaften von Windows Media Player-Steuer** Element" zugreifen, indem Sie auf die Zeile "(Benutzer definiert)" doppelklicken oder nach dem Auswählen der Zeile auf die Schaltfläche mit den Auslassungs Punkten ("...") klicken</span><span class="sxs-lookup"><span data-stu-id="7baf4-143">From the basic **Properties** dialog box, you can also access the more sophisticated **Windows Media Player Control Properties** dialog box by double-clicking the "(Custom)" row or by clicking the ellipsis ("...") button after selecting that row.</span></span> <span data-ttu-id="7baf4-144">In diesem Dialogfeld können Sie alle verfügbaren Player-Steuerelement Eigenschaften ändern.</span><span class="sxs-lookup"><span data-stu-id="7baf4-144">From this dialog box, you can modify all available Player control properties.</span></span>

> [!Note]  
> <span data-ttu-id="7baf4-145">Sie müssen darauf achten, keine Aktionen in Ereignis Handlern für Player-Steuerelemente auszuführen, die dazu führen, dass das Steuerelement zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="7baf4-145">You must be careful not to take actions in Player control event handlers that will result in the control being destroyed.</span></span> <span data-ttu-id="7baf4-146">Wenn Sie z. b. das Windows Media Player-Steuerelement auf einer Folie in einer PowerPoint-Präsentation einbetten, sollten Sie die PowerPoint-Methode " **Next** " nicht aus dem **OpenStateChange** -Ereignis des Players oder einem anderen Ereignis abrufen</span><span class="sxs-lookup"><span data-stu-id="7baf4-146">For example, if you embed the Windows Media Player control on a slide in a PowerPoint presentation, do not call the PowerPoint **Next** method from the Player **openStateChange** event or any other event.</span></span>

 

> [!Note]  
> <span data-ttu-id="7baf4-147">Außerdem sollten Sie die Eigenschaft " **Player. URL** " nicht von einem Ereignishandler für Player-Steuerelemente festlegen.</span><span class="sxs-lookup"><span data-stu-id="7baf4-147">In addition, you should not set the **Player.URL** property from a Player control event handler.</span></span>

 

<span data-ttu-id="7baf4-148">Fügen Sie in FrontPage der Webseite das Windows Media Player-Steuerelement hinzu, indem Sie im Menü **Einfügen** die Option **Webkomponente** auswählen.</span><span class="sxs-lookup"><span data-stu-id="7baf4-148">In FrontPage, add the Windows Media Player control to a webpage by selecting **Web Component** from the **Insert** menu.</span></span> <span data-ttu-id="7baf4-149">Wählen Sie im Dialogfeld **Webkomponente einfügen** in der Liste **Komponententyp** die Option **Erweiterte Steuerelemente** aus, und wählen Sie dann in der Liste der Steuerelement Optionen **ActiveX-Steuer** Element aus.</span><span class="sxs-lookup"><span data-stu-id="7baf4-149">In the **Insert Web Component** dialog box, select **Advanced Controls** from the **Component type** list, then select **ActiveX Control** from the list of control choices.</span></span> <span data-ttu-id="7baf4-150">Wählen Sie im nächsten Fenster des Dialog Felds die Option **Windows Media Player** aus.</span><span class="sxs-lookup"><span data-stu-id="7baf4-150">In the next window of the dialog box, select **Windows Media Player**.</span></span> <span data-ttu-id="7baf4-151">Wenn Sie nicht aufgeführt ist, klicken Sie auf **Anpassen** , und aktivieren Sie das Kontrollkästchen **Windows Media Player** in der **Steuer** Elementliste.</span><span class="sxs-lookup"><span data-stu-id="7baf4-151">If it is not listed, click **Customize** and select the **Windows Media Player** check box in the **Control** list.</span></span>

<span data-ttu-id="7baf4-152">Nachdem das Windows Media Player-Steuerelement eingebettet ist, können Sie es positionieren und seine Größe ändern und seine Eigenschaften ändern, indem Sie im Kontextmenü für das Steuerelement **ActiveX-Steuerelement Eigenschaften** auswählen.</span><span class="sxs-lookup"><span data-stu-id="7baf4-152">After the Windows Media Player control is embedded, you can position and resize it, and modify its properties by selecting **ActiveX Control Properties** from the shortcut menu for the control.</span></span> <span data-ttu-id="7baf4-153">In der HTML-Ansicht werden die von Ihnen angegebenen Eigenschaftswerte im Object-Element angezeigt, das das Windows Media Player-Steuerelement darstellt.</span><span class="sxs-lookup"><span data-stu-id="7baf4-153">In the HTML view, the property values that you specify appear in the OBJECT element representing the Windows Media Player control.</span></span> <span data-ttu-id="7baf4-154">Der Objektname wird als ID-Attribut angezeigt, und die Steuerelement Eigenschaften werden als param-Tags angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7baf4-154">The object name appears as the ID attribute, and the control properties appear as PARAM tags.</span></span> <span data-ttu-id="7baf4-155">Der Objektname ermöglicht Ihnen den Zugriff auf das Windows-Media Player Steuerelement-Objektmodell, das Sie mit Microsoft JScript programmieren können.</span><span class="sxs-lookup"><span data-stu-id="7baf4-155">The object name gives you access to the Windows Media Player control object model, which you can program using Microsoft JScript.</span></span> <span data-ttu-id="7baf4-156">Weitere Informationen finden Sie unter [Verwenden des Windows Media Player-Steuer Elements in einer Webseite](using-the-windows-media-player-control-in-a-web-page.md).</span><span class="sxs-lookup"><span data-stu-id="7baf4-156">For more information, see [Using the Windows Media Player Control in a Web Page](using-the-windows-media-player-control-in-a-web-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7baf4-157">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7baf4-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7baf4-158">**Player-Steuerelement Handbuch**</span><span class="sxs-lookup"><span data-stu-id="7baf4-158">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




