---
title: Verwenden von SAMI mit dem Windows Media Player-Steuerelement in einem Browser
description: Verwenden von SAMI mit dem Windows Media Player-Steuerelement in einem Browser
ms.assetid: 41906e57-adaa-4df7-86ba-19b8a757e216
keywords:
- Windows Media Player,Synchronized Accessible Media Interchange (SAMI)
- Windows Media Player Objektmodell, Synchronized Accessible Media Interchange (SAMI)
- Objektmodell, Synchronisierter barrierefreier Medienaustausch (Synchronized Accessible Media Interchange, SAMI)
- Windows Media Player Mobiler, synchronisierter zugänglicher Medienaustausch (Synchronized Accessible Media Interchange, SAMI)
- Windows Media Player ActiveX-Steuerelement, Synchronisierter barrierefreier Medienaustausch (Synchronized Accessible Media Interchange, SAMI)
- Windows Media Player Mobile ActiveX-Steuerelement, Synchronisierter barrierefreier Medienaustausch (Synchronized Accessible Media Interchange, SAMI)
- ActiveX-Steuerelement, Synchronisierter barrierefreier Medienaustausch (Synchronized Accessible Media Interchange, SAMI)
- Synchronisierter zugänglicher Medienaustausch (Synchronized Accessible Media Interchange, SAMI), Dateien
- SAMI (Synchronized Accessible Media Interchange), Dateien
- Synchronized Accessible Media Interchange (SAMI), Beispielcode
- SAMI (Synchronized Accessible Media Interchange), Beispielcode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d277f2849e6036d85bc8c03940a7dbd59df8b81083ca88240ebd68be768fde9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134343"
---
# <a name="using-sami-with-the-windows-media-player-control-in-a-browser"></a>Verwenden von SAMI mit dem Windows Media Player-Steuerelement in einem Browser

Anstatt eine SAMI-Datei für jeden Schriftschnitt oder jede Sprache zu erstellen, können Sie verschiedene Stilklassen in einer Datei deklarieren, indem Sie grundlegende Skripts und das Windows Media Player Steuerelementobjektmodell verwenden. Sie können benutzerdefinierte Steuerelemente erstellen, die es dem Benutzer ermöglichen, zwischen den verschiedenen Stil- und Sprachoptionen zu wählen. Darüber hinaus haben Sie die vollständige Kontrolle über den Entwurf der Player-Schnittstelle und die Anpassung der einzelnen Funktionen.

Ausführliche Informationen zum Einbetten des Windows Media Player-Steuerelements in eine Webseite finden Sie unter [Einfaches Beispiel für die Skripterstellung in einer Webseite.](simple-example-of-scripting-in-a-web-page.md)

Der folgende Beispielcode veranschaulicht die Verwendung von Untertiteln mit dem in eine Webseite eingebetteten Windows Media Player-Steuerelement. Sie enthält Steuerelemente, mit denen der Benutzer Schriftschnitt und Sprache auswählen kann.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




