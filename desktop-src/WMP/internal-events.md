---
title: Interne Ereignisse
description: Interne Ereignisse
ms.assetid: d99e84ec-41db-42e7-ab26-5ca6a3ba610b
keywords:
- Windows Media Player Skins, interne Ereignisse
- Skins, interne Ereignisse
- Ereignisse, intern
- Schreiben von Code für Skins, interne Ereignisse
- interne Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08ed2abca3f23a89ea6fe261a29639d671e0d58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947500"
---
# <a name="internal-events"></a>Interne Ereignisse

Sie können Änderungen erkennen, die in Windows-Media Player oder Änderungen in ihrer eigenen Skin auftreten. Dabei kann es sich um Änderungen in den Eigenschaften oder Methoden von Windows-Media Player Objekten, Änderungen in den Skin-Attributen usw. handeln.

## <a name="windows-media-player-property-changes"></a>Änderungen an der Windows Media Player-Eigenschaft

Sie können Änderungen in Windows Media Player mithilfe des wmpprop-Listener verarbeiten. Sie müssen den Listener als Wert eines Attributs einrichten. Fügen Sie den Wert in doppelte Anführungszeichen ein, und beginnen Sie mit dem Wort "wmpprop", gefolgt von einem Doppelpunkt. Dann fügen Sie die Eigenschaft ein, die Sie überwachen möchten. Wenn sich die-Eigenschaft ändert, ändert sich auch der Wert des-Attributs. Wenn Sie z. b. einen Wert für den Schieberegler Element ändern möchten, wenn sich der Wert des **CurrentPosition** -Attributs ändert, geben Sie Folgendes ein:


```C++
<SLIDER id="mySlider" value="wmpprop:player.Controls.currentPosition" />
```



-   **Wichtig** Verwenden Sie wmpprop nicht für Windows-Media Player Methoden. Unerwartete Ergebnisse können auftreten.

## <a name="windows-media-player-method-changes"></a>Windows Media Player-Methoden Änderungen

Sie können Ihre Skin auf die Verfügbarkeit von Methoden unter Windows Media Player mithilfe von wmpaktiviertem und wmpdeaktiviert festlegen. Diese werden ähnlich wie der wmpprop-Listener verwendet, mit dem Unterschied, dass Sie diese nur für Methoden des **Steuer** Element Objekts verwenden können, die von der **IsAvailable** -Methode unterstützt werden.

Beispielsweise können Sie eine Schaltfläche nur aktivieren, wenn die **Play** -Methode aktiviert ist, indem Sie Code wie den folgenden verwenden:


```C++
<BUTTON ... enabled="wmpenabled:player.Controls.Play();" />

```



-   **Wichtig** Verwenden Sie wmpaktivierte oder wmpdeaktivierte Windows-Media Player Eigenschaften nicht. Unerwartete Ergebnisse können auftreten.

## <a name="skin-attribute-changes"></a>Skin-Attribut Änderungen

Sie können auf Änderungen in den Skin-Attributen auf eine von zwei Arten reagieren, indem Sie wmpprop oder das **\_ OnChange** -Ereignis verwenden.

Sie können wmpprop verwenden, um auf Änderungen in ihrer eigenen Skin zu lauschen. Wenn Sie z. b. den Wert des Schiebereglers in einem Textfeld anzeigen möchten, können Sie Folgendes eingeben:


```C++
<TEXT ... value="wmpprop:mySlider.value">

```



Sie können das **\_ OnChange** -Ereignis verwenden, um Ereignisse in einem Element zu verarbeiten. Sie müssen den Namen des Attributs, das Sie nachverfolgen möchten, an **\_ OnChange** anfügen. Wenn Sie z. b. den Wert eines Textfelds überprüfen möchten, geben Sie Folgendes ein:


```C++
value_onchange

```



Anschließend würden Sie eine JScript-Zeichenfolge zuweisen, die Sie ausführen möchten, wenn sich der Wert ändert. Um z. b. auf eine Änderung des Werts eines Textfelds zu reagieren, das zum Anpassen des Umfangs von Windows Media Player verwendet werden kann, geben Sie Folgendes in Ihrem **Text** -Element als Attribut ein:


```C++
value_onchange = "JScript: player.Settings.Volume = myText.value"

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Behandeln von Ereignissen**](handling-events.md)
</dt> </dl>

 

 




