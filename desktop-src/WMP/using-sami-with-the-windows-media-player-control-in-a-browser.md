---
title: Verwenden von Sami mit dem Windows Media Player-Steuerelement in einem Browser
description: Verwenden von Sami mit dem Windows Media Player-Steuerelement in einem Browser
ms.assetid: 41906e57-adaa-4df7-86ba-19b8a757e216
keywords:
- Windows Media Player, synchronisierter zugänglicher Medienaustausch (Sami)
- Windows Media Player-Objektmodell, synchronisierter zugänglicher Medienaustausch (Sami)
- Objektmodell, synchronisierter, zugänglicher Medienaustausch (Sami)
- Windows Media Player Mobile, synchronisierter verfügbarer Medienaustausch (Sami)
- Windows Media Player ActiveX-Steuerelement, synchronisierter barrierefreier Medienaustausch (Sami)
- Windows Media Player Mobile ActiveX-Steuerelement, synchronisierter barrierefreier Medienaustausch (Sami)
- ActiveX-Steuerelement, synchronisierter, zugänglicher Medienaustausch (Sami)
- Synchronisierter, barrierefreier Medienaustausch (Sami), Dateien
- Samisch (synchronisierter, zugänglicher Medienaustausch), Dateien
- Synchronisierter, barrierefreier Medienaustausch (Sami), Beispielcode
- Samisch (synchronisierter, zugänglicher Medienaustausch), Beispielcode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b651c3af117942d56ffc5334323913d26cdf6f99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948053"
---
# <a name="using-sami-with-the-windows-media-player-control-in-a-browser"></a><span data-ttu-id="c626c-114">Verwenden von Sami mit dem Windows Media Player-Steuerelement in einem Browser</span><span class="sxs-lookup"><span data-stu-id="c626c-114">Using SAMI with the Windows Media Player Control in a Browser</span></span>

<span data-ttu-id="c626c-115">Anstatt für jeden Schriftart Stil oder jede Sprache eine Sami-Datei zu erstellen, können Sie unterschiedliche Formatklassen in einer Datei mit grundlegenden Skripts und dem Windows-Media Player Steuerelement-Objektmodell deklarieren.</span><span class="sxs-lookup"><span data-stu-id="c626c-115">Instead of creating a SAMI file for each font style or language, you can declare different style classes in one file by using basic scripting and the Windows Media Player control object model.</span></span> <span data-ttu-id="c626c-116">Sie können benutzerdefinierte Steuerelemente erstellen, die es dem Benutzer ermöglichen, zwischen den verschiedenen Stil-und Sprachoptionen zu wählen.</span><span class="sxs-lookup"><span data-stu-id="c626c-116">You can create custom controls that enable the user to choose between the different style and language options.</span></span> <span data-ttu-id="c626c-117">Außerdem haben Sie die komplette Kontrolle über das Design der Player-Schnittstelle und die Anpassung der einzelnen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="c626c-117">Furthermore, you have complete control over the design of the Player interface and the customization of each function.</span></span>

<span data-ttu-id="c626c-118">Ausführliche Informationen zum Einbetten des Windows Media Player-Steuer Elements auf einer Webseite finden Sie unter [einfaches Beispiel der Skripterstellung auf einer](simple-example-of-scripting-in-a-web-page.md)Webseite.</span><span class="sxs-lookup"><span data-stu-id="c626c-118">For detailed information about embedding the Windows Media Player control in a webpage, see [Simple Example of Scripting in a Web Page](simple-example-of-scripting-in-a-web-page.md).</span></span>

<span data-ttu-id="c626c-119">Der folgende Beispielcode veranschaulicht die Verwendung von Untertiteln mit dem Windows Media Player-Steuerelement, das in eine Webseite eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="c626c-119">The following example code demonstrates how to use closed captions with the Windows Media Player control embedded in a webpage.</span></span> <span data-ttu-id="c626c-120">Es enthält Steuerelemente, mit denen der Benutzer Schriftart Stil und Sprache auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="c626c-120">It includes controls to allow the user to select font style and language.</span></span>


```C++
<HTML>
<HEAD>

<SCRIPT>
  // The following variable is used to prevent multiple initialization.
  var initialized = false;
  // The following function populates the select boxes.
  // It is called the first time the media file is opened.
  // Before then, the SAMI settings cannot be retrieved.
  function initialize() {
    var newOption;
    for (var i = 0; i < Player.closedCaption.SAMILangCount; i++) {
      newOption = document.createElement("OPTION");
      newOption.text = Player.closedCaption.getSAMILangName(i);
      newOption.value = newOption.text;
      CCLang.options.add(newOption);
    }
    for (var i = 0; i < Player.closedCaption.SAMIStyleCount; i++) {
      newOption = document.createElement("OPTION");
      newOption.text = Player.closedCaption.getSAMIStyleName(i);
      newOption.value = newOption.text;
      CCStyle.options.add(newOption);
    }
    initialized = true;
  }
</SCRIPT>

<!-- The following script code runs when the page is fully loaded. -->
<SCRIPT for="window" event="onload()">
  Player.closedCaption.captioningID = "captions";
  Player.closedCaption.SAMIFileName = "https://www.proseware.com/Media/seattle.smi";
  // The digital media file will open automatically, after which
  // the OpenStateChange event (handled below) will fire.
  Player.URL = "https://www.proseware.com/Media/seattle.wmv";
</SCRIPT>

<!-- The following script code runs when a media file is opened. -->
<SCRIPT for="Player" event="OpenStateChange(NewState)">
  // The first time this event fires, the Player stops and the 
  // initialize function is called. This allows the user to 
  // select a language and style before viewing the file.
  if (13 == NewState && !initialized) {
    Player.controls.stop();
    initialize();
  }
</SCRIPT>

</HEAD>
<BODY>

<OBJECT 
  ID="Player" 
  classID="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"
  height="200" 
  width="250"
>
</OBJECT>

<TABLE height="100" width="250" border="3" bordercolor="blue">
  <TR align="center">
    <TD bgcolor="white">
      <SELECT ID="CCLang" onClick="Player.closedCaption.SAMILang = value"></SELECT>
      <SELECT ID="CCStyle" onClick="Player.closedCaption.SAMIStyle = value"></SELECT>
    </TD>
  </TR>
  <TR height="75">
    <TD bgcolor="blue">
      <DIV id="captions"></DIV>
    </TD>
  </TR>
</TABLE>

</BODY>
</HTML>

```



## <a name="related-topics"></a><span data-ttu-id="c626c-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c626c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c626c-122">**Hinzufügen von Untertiteln zu digitalen Medien**</span><span class="sxs-lookup"><span data-stu-id="c626c-122">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




