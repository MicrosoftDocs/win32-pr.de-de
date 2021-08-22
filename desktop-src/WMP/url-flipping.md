---
title: URL-Flipping
description: URL-Flipping
ms.assetid: 2921dff1-f740-491c-9b5e-79b7638e2065
keywords:
- Windows Media Player,Webbasierte Präsentationen
- Windows Media Player Objektmodell, webbasierte Präsentationen
- Objektmodell, webbasierte Präsentationen
- Windows Media Player Mobile, webbasierte Präsentationen
- Windows Media Player ActiveX-Steuerelement, webbasierte Präsentationen
- Windows Media Player Mobile ActiveX-Steuerelement,Webbasierte Präsentationen
- ActiveX,Webbasierte Präsentationen
- Windows Media Player,URL-Flipping
- Windows Media Player-Objektmodell, URL-Flipping
- Objektmodell, URL-Flipping
- Windows Media Player Mobil, URL-Flipping
- Windows Media Player ActiveX,URL-Flipping
- Windows Media Player Mobile ActiveX-Steuerelement, URL-Flipping
- ActiveX,URL-Flipping
- Webbasierte Präsentationen, URL-Flipping
- Erstellen webbasierter Präsentationen, URL-Flipping
- URL-Flipping
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4471045506447b93621578f27e2f156bb214016b3fa8ec114a689b919314d10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134523"
---
# <a name="url-flipping"></a>URL-Flipping

Die Verwendung von Webseiten für Bildschirmpräsentationen wird als URL-Flipping bezeichnet und wird automatisch von Windows Media Player verarbeitet, wenn URL-Skriptbefehle in den abspielten digitalen Medienstream eingebettet sind. Sie können in jedem Skriptbefehl einen Zielframe für Ihre Seiten angeben, oder Sie können ihn angeben, indem Sie die eigenschaft **Einstellungen.defaultFrame** festlegen. Sie können diese Eigenschaft im Skriptcode oder mithilfe eines PARAM-Elements innerhalb des OBJECT-Elements festlegen, das das Windows Media Player einbettet.

Sie können die URL-Skriptbefehle in Ihrem JScript wie benutzerdefinierte Skriptbefehle verarbeiten. Wenn das Windows Media Player-Steuerelement URL-Skriptbefehle ignorieren soll, damit Sie sie vollständig selbst *verarbeiten* können, legen Sie die Einstellungen. **invokeURLs-Eigenschaft** auf FALSE entweder im Skriptcode oder mithilfe eines PARAM-Elements, wie zuvor beschrieben.

Im folgenden Beispiel wird ein typisches Frameset zum Kippen von URLs veranschaulicht. Erstellen Sie zunächst eine Seite, die das Frameset beschreibt:


```HTML
<HTML>
<FRAMESET cols="300,*">
  <FRAME name="player" src="player.html">
  <FRAME name="content">
</FRAMESET>
</HTML>

```



Erstellen Sie als Nächstes die player.html-Datei, auf die im Frameset verwiesen wird, mithilfe des folgenden Codes (die Datei video.wmv wird angenommen, dass sie im gleichen Verzeichnis wie die HTML-Dateien vorhanden ist):


```HTML
<HTML>
<BODY>
<OBJECT ID="Player" CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
  <PARAM name="URL" value="https://www.proseware.com/Media/video.wmv"/>
  <PARAM name="defaultFrame" value="content"/>
</OBJECT>
</BODY>
</HTML>

```



Wenn Ihre Webseiten klein genug sind, um schnell geladen zu werden, kann diese Einrichtung für Ihre Anforderungen ausreichen. Wenn Ihre Webseiten hingegen komplex sind, kann rich media streaming je nach Verbindungsgeschwindigkeit Ihrer Zielgruppe effektiver sein.

> [!Note]  
> Url-Flipping funktioniert nicht ordnungsgemäß mit Seiten, die in der Netscape Navigator. Anstatt in dem durch **defaultFrame** angegebenen Frame zu erscheinen, zeigt jeder im Navigator empfangene URL-Skriptbefehl die URL in einem neuen Browserfenster an.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen Web-Based Präsentationen**](creating-web-based-presentations.md)
</dt> <dt>

[**Verwenden des Skripts zum Steuern des URL-Flippings**](using-script-to-control-url-flipping.md)
</dt> </dl>

 

 




