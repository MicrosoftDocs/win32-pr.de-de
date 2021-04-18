---
title: Einfaches Beispiel für die Skripterstellung auf einer Webseite
description: Einfaches Beispiel für die Skripterstellung auf einer Webseite
ms.assetid: c6d6954e-f684-4dc1-8b9c-c5fc3cab7421
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
- Skript Beispiel für die Einbettung von Webseiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9616bd4032a1b2d7e70916b545db30289995eb4
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2019
ms.locfileid: "106337399"
---
# <a name="simple-example-of-scripting-in-a-web-page"></a><span data-ttu-id="3bae2-119">Einfaches Beispiel für die Skripterstellung auf einer Webseite</span><span class="sxs-lookup"><span data-stu-id="3bae2-119">Simple Example of Scripting in a Web Page</span></span>

<span data-ttu-id="3bae2-120">Sie können das Windows Media Player-Steuerelement problemlos in eine HTML-Datei einbetten, indem Sie jede Skriptsprache verwenden, die Ihr Browser erkennt</span><span class="sxs-lookup"><span data-stu-id="3bae2-120">You can easily embed the Windows Media Player control in an HTML file using any scripting language your browser recognizes.</span></span> <span data-ttu-id="3bae2-121">Im folgenden einfachen Beispiel wird mithilfe von Microsoft JScript eine Seite erstellt, die eine Datei wieder gibt, wenn Sie auf eine Schaltfläche klicken und die Wiedergabe der Datei beenden, wenn Sie auf eine andere Schaltfläche klicken.</span><span class="sxs-lookup"><span data-stu-id="3bae2-121">The following simple example uses Microsoft JScript to create a page that will play a file when you click on a button, and stop playing the file when you click on another button.</span></span>

<span data-ttu-id="3bae2-122">Sie können das Windows Media Player ActiveX-Steuerelement mithilfe der folgenden vier Schritte in eine Webseite einbetten:</span><span class="sxs-lookup"><span data-stu-id="3bae2-122">You can embed the Windows Media Player ActiveX control in a webpage using the following four steps:</span></span>

1.  <span data-ttu-id="3bae2-123">Erstellen Sie die Webseite.</span><span class="sxs-lookup"><span data-stu-id="3bae2-123">Create the webpage.</span></span>
2.  <span data-ttu-id="3bae2-124">Fügen Sie das Objekttag hinzu.</span><span class="sxs-lookup"><span data-stu-id="3bae2-124">Add the OBJECT tag.</span></span>
3.  <span data-ttu-id="3bae2-125">Fügen Sie eine Benutzeroberfläche hinzu.</span><span class="sxs-lookup"><span data-stu-id="3bae2-125">Add a user interface.</span></span> <span data-ttu-id="3bae2-126">In diesem Fall zwei Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="3bae2-126">In this case, two buttons.</span></span>
4.  <span data-ttu-id="3bae2-127">Fügen Sie einige Codezeilen hinzu, um zu antworten, wenn der Benutzer auf eine der Schaltflächen klickt, die Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="3bae2-127">Add a few lines of code to respond when the user clicks on one of the buttons you have created.</span></span>

## <a name="creating-the-web-page"></a><span data-ttu-id="3bae2-128">Erstellen der Webseite</span><span class="sxs-lookup"><span data-stu-id="3bae2-128">Creating the Web Page</span></span>

<span data-ttu-id="3bae2-129">Der erste Schritt besteht darin, eine gültige HTML-Webseite zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3bae2-129">The first step is to create a valid HTML webpage.</span></span> <span data-ttu-id="3bae2-130">Der folgende Code ist mindestens erforderlich, um eine leere, aber gültige HTML-Seite zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="3bae2-130">The following code is the minimum needed to create a blank but valid HTML page:</span></span>


```HTML
<HTML>
    <HEAD>
    </HEAD>
    <BODY>
    </BODY>
</HTML>

```



## <a name="adding-the-object-tag"></a><span data-ttu-id="3bae2-131">Hinzufügen des Objekttags</span><span class="sxs-lookup"><span data-stu-id="3bae2-131">Adding the OBJECT Tag</span></span>

<span data-ttu-id="3bae2-132">Nachdem Sie eine Webseite erstellt haben, müssen Sie ein Objekttag hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3bae2-132">Once you have created a webpage, you need to add an OBJECT tag.</span></span> <span data-ttu-id="3bae2-133">Dadurch wird das ActiveX-Steuerelement für den Browser identifiziert, und alle anfänglichen Definitionen werden eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="3bae2-133">This identifies the ActiveX control to the browser and sets up any initial definitions.</span></span> <span data-ttu-id="3bae2-134">Sie müssen das Objekttag im Text des Codes platzieren.</span><span class="sxs-lookup"><span data-stu-id="3bae2-134">You must place the OBJECT tag in the BODY of the code.</span></span> <span data-ttu-id="3bae2-135">Wenn Sie diese im Textkörper platzieren, wird die Standardbenutzer Oberfläche von Windows Media Player angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3bae2-135">If you place it in the BODY, the default user interface of Windows Media Player will be visible.</span></span> <span data-ttu-id="3bae2-136">Wenn Sie eine eigene Benutzeroberfläche erstellen möchten, legen Sie die Attribute height und Width auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="3bae2-136">If you want to create your own user interface, set the height and width attributes to 0 (zero).</span></span> <span data-ttu-id="3bae2-137">Sie können auch den *Player* festlegen. **uiMode** -Eigenschaft auf "unsichtbar", wenn Sie das Steuerelement ausblenden möchten, aber trotzdem Platz für das Steuerelement auf der Seite reservieren.</span><span class="sxs-lookup"><span data-stu-id="3bae2-137">You can also set the *Player*.**uiMode** property to "invisible" when you want to hide the control, but still reserve space for it on the page.</span></span> <span data-ttu-id="3bae2-138">Der folgende Code wird empfohlen, wenn Sie eine benutzerdefinierte Benutzeroberfläche bereitstellen:</span><span class="sxs-lookup"><span data-stu-id="3bae2-138">The following code is recommended when you provide a custom user interface:</span></span>


```HTML
<OBJECT ID="Player" height="0" width="0"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
</OBJECT>

```



<span data-ttu-id="3bae2-139">Die folgenden objekttagattribute sind erforderlich:</span><span class="sxs-lookup"><span data-stu-id="3bae2-139">The following OBJECT tag attributes are required:</span></span>

<span data-ttu-id="3bae2-140">id</span><span class="sxs-lookup"><span data-stu-id="3bae2-140">ID</span></span>

<span data-ttu-id="3bae2-141">Der Name, der von anderen Teilen des Codes verwendet wird, um das ActiveX-Steuerelement zu identifizieren und zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="3bae2-141">The name that will be used by other parts of the code to identify and use the ActiveX control.</span></span> <span data-ttu-id="3bae2-142">Sie können einen beliebigen Namen auswählen, solange es sich um einen Namen handelt, der nicht bereits von HTML, HTML-Erweiterungen oder der verwendeten Skriptsprache verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3bae2-142">You can choose any name you want, as long as it is a name that is not already used by HTML, HTML extensions, or the scripting language you are using.</span></span> <span data-ttu-id="3bae2-143">In diesem Beispiel wird der Name "Player" verwendet, Sie können ihn aber auch "myPlayer" oder etwas anderes nennen.</span><span class="sxs-lookup"><span data-stu-id="3bae2-143">In this example, the name "Player" is used, but you could also call it "MyPlayer" or something else.</span></span> <span data-ttu-id="3bae2-144">Wählen Sie einfach einen Namen aus, der für diese Webseite eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="3bae2-144">Just pick a name that is unique to that webpage.</span></span>

<span data-ttu-id="3bae2-145">ClassID</span><span class="sxs-lookup"><span data-stu-id="3bae2-145">CLASSID</span></span>

<span data-ttu-id="3bae2-146">Eine sehr große hexadezimal Zahl, die für das-Steuerelement eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="3bae2-146">A very large hexadecimal number that is unique to the control.</span></span> <span data-ttu-id="3bae2-147">Nur ein Steuerelement hat diese Zahl und ist das Windows Media Player ActiveX-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="3bae2-147">Only one control has this number and it is the Windows Media Player ActiveX control.</span></span> <span data-ttu-id="3bae2-148">Um typografische Fehler zu vermeiden, können Sie diese Nummer aus der Dokumentation kopieren und einfügen.</span><span class="sxs-lookup"><span data-stu-id="3bae2-148">To prevent typographical errors, you can copy and paste this number from the documentation.</span></span> <span data-ttu-id="3bae2-149">Versionen des Windows Media Player-Steuer Elements vor Version 7,0 verfügten über eine andere ClassID.</span><span class="sxs-lookup"><span data-stu-id="3bae2-149">Versions of the Windows Media Player control prior to version 7.0 had a different CLASSID.</span></span>

## <a name="adding-a-user-interface"></a><span data-ttu-id="3bae2-150">Hinzufügen einer Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="3bae2-150">Adding a User Interface</span></span>

<span data-ttu-id="3bae2-151">HTML ermöglicht eine große Zahl von Elementen der Benutzeroberfläche, sodass der Benutzer mit Ihrer Webseite interagieren kann, indem er auf Schlüssel und andere Benutzeraktionen klickt.</span><span class="sxs-lookup"><span data-stu-id="3bae2-151">HTML allows a vast wealth of user interface elements, allowing the user to interact with your webpage by clicking, pressing keys, and other user actions.</span></span> <span data-ttu-id="3bae2-152">Das Hinzufügen einiger Eingabe Schaltflächen ist die einfachste Möglichkeit, um eine schnelle Benutzeroberfläche bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3bae2-152">Adding a few INPUT buttons is the easiest way to provide a quick user interface.</span></span> <span data-ttu-id="3bae2-153">Mit dem folgenden Code werden zwei Schaltflächen erstellt, die auf den Benutzer reagieren können.</span><span class="sxs-lookup"><span data-stu-id="3bae2-153">The following code creates two buttons that can respond to the user.</span></span> <span data-ttu-id="3bae2-154">Wenn Sie auf eine Schaltfläche klicken, wird der Medienstrom abgespielt, und die andere Schaltfläche beendet ihn:</span><span class="sxs-lookup"><span data-stu-id="3bae2-154">Clicking one button starts the media stream playing and the other button stops it:</span></span>


```HTML
<INPUT TYPE="BUTTON" NAME="BtnPlay" VALUE="Play" OnClick="StartMeUp()">
<INPUT TYPE="BUTTON" NAME="BtnStop" VALUE="Stop" OnClick="ShutMeDown()">

```



<span data-ttu-id="3bae2-155">Der Name der Schaltfläche wird verwendet, um die Schaltfläche für den Code zu identifizieren. der Wert ist die Bezeichnung, die auf der Schaltfläche angezeigt wird, und das OnClick-Attribut gibt an, welcher Teil des Skriptcodes aufgerufen wird, wenn auf die Schaltfläche geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="3bae2-155">The name of the button is used to identify the button to your code; the value is the label that will appear on the button, and the OnClick attribute identifies which part of your scripting code will be called when the button is clicked.</span></span>

## <a name="adding-scripting-code"></a><span data-ttu-id="3bae2-156">Hinzufügen von Skript Code</span><span class="sxs-lookup"><span data-stu-id="3bae2-156">Adding Scripting Code</span></span>

<span data-ttu-id="3bae2-157">Der Skriptcode fügt der Seite Interaktivität hinzu.</span><span class="sxs-lookup"><span data-stu-id="3bae2-157">Scripting code adds interactivity to your page.</span></span> <span data-ttu-id="3bae2-158">Der Skriptcode kann auf Ereignisse, Aufruf Methoden und Änderungs Lauf Zeiteigenschaften reagieren.</span><span class="sxs-lookup"><span data-stu-id="3bae2-158">Scripting code can respond to events, call methods, and change run-time properties.</span></span> <span data-ttu-id="3bae2-159">Erweiterte Skripts sind in einem skripttagsatz enthalten.</span><span class="sxs-lookup"><span data-stu-id="3bae2-159">Extended scripts are enclosed in a SCRIPT tag set.</span></span> <span data-ttu-id="3bae2-160">Das Script-Tag teilt dem Browser mit, wo der Skriptcode ist, und identifiziert die Skriptsprache.</span><span class="sxs-lookup"><span data-stu-id="3bae2-160">The SCRIPT tag tells the browser where your scripting code is and identifies the scripting language.</span></span> <span data-ttu-id="3bae2-161">Wenn Sie keine Sprache identifizieren, wird als Standardsprache Microsoft JScript verwendet.</span><span class="sxs-lookup"><span data-stu-id="3bae2-161">If you do not identify a language, the default language will be Microsoft JScript.</span></span>

<span data-ttu-id="3bae2-162">Es ist empfehlenswert, das Skript in HTML-Kommentar Tags einzuschließen, sodass Browser, die keine Skripterstellung unterstützen, Ihren Code nicht als Text Rendering.</span><span class="sxs-lookup"><span data-stu-id="3bae2-162">It is good authoring practice to enclose your script in HTML comment tags so browsers that do not support scripting do not render your code as text.</span></span> <span data-ttu-id="3bae2-163">Fügen Sie das Skript-Tag an eine beliebige Stelle innerhalb des Texts der HTML-Datei ein, und Betten Sie den Code aus, der in den öffnenden und schließenden Skript Tags</span><span class="sxs-lookup"><span data-stu-id="3bae2-163">Put the SCRIPT tag anywhere within the BODY of your HTML file and embed the comment-surrounded code within the opening and closing SCRIPT tags.</span></span>

<span data-ttu-id="3bae2-164">Im folgenden Beispiel für ein Microsoft JScript-Code wird das Windows Media Player-Steuerelement aufgerufen und eine entsprechende Aktion als Reaktion auf den entsprechenden Klick auf die Schaltfläche ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3bae2-164">The following Microsoft JScript code example calls the Windows Media Player control and performs an appropriate action in response to the corresponding button click.</span></span>


```HTML
<SCRIPT>
<!--

function StartMeUp ()
{
    Player.URL = "laure.wma";
}

function ShutMeDown ()
{
    Player.controls.stop();
}

-->
</SCRIPT>

```



<span data-ttu-id="3bae2-165">Die Beispiel Funktion startmeup wird aufgerufen, wenn auf die Schaltfläche mit der markierten Wiedergabe Taste geklickt wird und die shutmedown-Funktion aufgerufen wird, wenn auf die Schaltfläche Beenden geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="3bae2-165">The example function, StartMeUp, is called when the button marked Play is clicked, and the ShutMeDown function is called when the Stop button is clicked.</span></span>

<span data-ttu-id="3bae2-166">Der Code in startmeup verwendet die URL-Eigenschaft, um einen Pfad zu den Medien zu definieren.</span><span class="sxs-lookup"><span data-stu-id="3bae2-166">The code inside StartMeUp uses the URL property to define a path to the media.</span></span> <span data-ttu-id="3bae2-167">Die Medien werden sofort wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="3bae2-167">The media will start playing immediately.</span></span>

<span data-ttu-id="3bae2-168">Der shutmedown-Code ruft  die Methode "Beenden **" des Steuerelement Objekts auf** .</span><span class="sxs-lookup"><span data-stu-id="3bae2-168">The ShutMeDown code calls the **stop** method of the **Controls** object.</span></span> <span data-ttu-id="3bae2-169">Beachten Sie, dass das Steuerelement-Objekt über die **Controls** -Eigenschaft des **Player** **-Objekts aufgerufen** wird, das den ID-Wert "Player" hat.</span><span class="sxs-lookup"><span data-stu-id="3bae2-169">Note that the **Controls** object is called through the **controls** property of the **Player** object, which has the ID value of "Player".</span></span>

<span data-ttu-id="3bae2-170">Der folgende Code veranschaulicht das vollständige Beispiel.</span><span class="sxs-lookup"><span data-stu-id="3bae2-170">The following code shows a complete example.</span></span>


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>
<OBJECT ID="Player" height="0" width="0"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
</OBJECT>
<INPUT TYPE="BUTTON" NAME="BtnPlay" VALUE="Play" OnClick="StartMeUp()">
<INPUT TYPE="BUTTON" NAME="BtnStop" VALUE="Stop" OnClick="ShutMeDown()">
<SCRIPT>
<!--

function StartMeUp ()
{
    Player.URL = "laure.wma";
}

function ShutMeDown ()
{
    Player.controls.stop();
}

-->
</SCRIPT>
</BODY>
</HTML>

```



<span data-ttu-id="3bae2-171">Beachten Sie, dass Sie in der URL-Eigenschaft eine gültige URL für einen gültigen Dateinamen angeben müssen.</span><span class="sxs-lookup"><span data-stu-id="3bae2-171">Note that you must provide a valid URL to a valid file name in the URL property.</span></span> <span data-ttu-id="3bae2-172">In diesem Fall wird davon ausgegangen, dass sich die Datei "Laure. wma" im selben Verzeichnis wie die HTML-Datei befindet.</span><span class="sxs-lookup"><span data-stu-id="3bae2-172">In this case the assumption is that the file laure.wma is in the same directory as the HTML file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3bae2-173">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3bae2-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bae2-174">**Verwenden des Windows Media Player-Steuer Elements in einer Webseite**</span><span class="sxs-lookup"><span data-stu-id="3bae2-174">**Using the Windows Media Player Control in a Web Page**</span></span>](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




