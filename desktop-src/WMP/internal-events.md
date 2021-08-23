---
title: Interne Ereignisse
description: Interne Ereignisse
ms.assetid: d99e84ec-41db-42e7-ab26-5ca6a3ba610b
keywords:
- Windows Media Player Skins,interne Ereignisse
- Skins, interne Ereignisse
- Events,internal
- Schreiben von Code für Skins, interne Ereignisse
- interne Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8859ed86cb4951509d452b24c108e73d4129e474abf1c0bc2f51487e2d42bd9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572520"
---
# <a name="internal-events"></a>Interne Ereignisse

Sie können Änderungen erkennen, die in Windows Media Player oder Änderungen in Ihrer eigenen Skin auftreten. Dies können Änderungen Windows Media Player Objekteigenschaften oder -methoden, Änderungen an Skinattributen und so weiter sein.

## <a name="windows-media-player-property-changes"></a>Windows Media Player Eigenschaftenänderungen

Sie können Änderungen in Windows Media Player mithilfe des wmpprop-Listeners verarbeiten. Sie müssen den Listener als Wert eines Attributs einrichten. Setzen Sie den Wert in doppelte Anführungszeichen, und beginnen Sie mit dem Wort "wmpprop", gefolgt von einem Doppelpunkt. Anschließend fügen Sie die Eigenschaft ein, auf die Sie lauschen möchten. Wenn sich die Eigenschaft ändert, ändert sich auch der Wert des Attributs. Wenn sich beispielsweise ein Schiebereglerelementwert ändert, wenn sich der Wert des **currentPosition-Attributs** ändert, geben Sie Folgendes ein:


```C++
<SLIDER id="mySlider" value="wmpprop:player.Controls.currentPosition" />
```



-   **Wichtig** Verwenden Sie wmpprop nicht für Windows Media Player Methoden. Unerwartete Ergebnisse können auftreten.

## <a name="windows-media-player-method-changes"></a>Windows Media Player Methodenänderungen

Sie können Ihre Skin mithilfe von wmpenabled und wmpdisabled auf die Verfügbarkeit von Methoden auf Windows Media Player reagieren lassen. Diese werden ähnlich wie der wmpprop-Listener verwendet, außer dass Sie diese nur für Methoden des **Control-Objekts** verwenden können, die von der **isAvailable-Methode unterstützt** werden.

Beispielsweise können Sie eine Schaltfläche nur aktivieren, wenn die **Play-Methode** aktiviert ist, indem Sie Code wie den folgenden verwenden:


```C++
<BUTTON ... enabled="wmpenabled:player.Controls.Play();" />

```



-   **Wichtig** Verwenden Sie wmpenabled oder wmpdisabled nicht für Windows Media Player Eigenschaften. Unerwartete Ergebnisse können auftreten.

## <a name="skin-attribute-changes"></a>Änderungen des Skinattributs

Sie können mithilfe von wmpprop oder des **\_ Onchange-Ereignisses** auf Änderungen in Ihren Skinattributen auf zwei Arten reagieren.

Sie können wmpprop verwenden, um auf Änderungen in Ihrer eigenen Skin zu lauschen. Wenn Sie beispielsweise den Schiebereglerwert in einem Textfeld anzeigen möchten, können Sie Folgendes eingeben:


```C++
<TEXT ... value="wmpprop:mySlider.value">

```



Sie können das **\_ Onchange-Ereignis** verwenden, um Ereignisse innerhalb eines Elements zu verarbeiten. Sie müssen den Namen des Attributs, das Sie nachverfolgen möchten, an **\_ onchange anfügen.** Wenn Sie beispielsweise den Wert eines Textfelds nachverfolgen möchten, geben Sie Folgendes ein:


```C++
value_onchange

```



Anschließend würden Sie eine Zeichenfolge JScript, die Sie ausführen möchten, wenn sich der Wert ändert. Um beispielsweise auf eine Änderung des Werts eines Textfelds zu reagieren, das zum Anpassen des Volumens von Windows Media Player verwendet werden kann, geben Sie Folgendes in Ihr **TEXT-Element** als Attribut ein:


```C++
value_onchange = "JScript: player.Settings.Volume = myText.value"

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Behandeln von Ereignissen**](handling-events.md)
</dt> </dl>

 

 




