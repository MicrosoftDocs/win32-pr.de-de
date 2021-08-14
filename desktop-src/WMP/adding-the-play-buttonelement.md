---
title: Hinzufügen von Play BUTTONELEMENT
description: Hinzufügen von Play BUTTONELEMENT
ms.assetid: 895850a7-7538-4581-8348-41cbb3bc9717
keywords:
- Erstellen von Skins, BUTTONELEMENT-Element
- Windows Media Player,BUTTONELEMENT-Element
- skins,BUTTONELEMENT-Element
- Skindefinitionsdateien, BUTTONELEMENT-Element
- BUTTONELEMENT-Element
- elements,BUTTONELEMENT
- Erstellen von Skins, Wiedergabeschaltflächen
- Windows Media Player,Wiedergabeschaltflächen
- Skins, Wiedergabeschaltflächen
- Skindefinitionsdateien,Wiedergabeschaltflächen
- Wiedergabeschaltflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cab52691b48876327f45fbaf30a98de78c8c0c46a2eafd0a2c342e51c5a8683
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583544"
---
# <a name="adding-the-play-buttonelement"></a>Hinzufügen von Play BUTTONELEMENT

Abschließend können Sie die **BUTTONELEMENT-Elemente** hinzufügen, die die visuellen Schaltflächen auf dem Bildschirm verbinden, um Windows Media Player anzuzeigen. Dies ist der Kern Ihrer Skin, und Sie können sich dies als Verkabelung der Oberfläche der Skin mit der inneren Maschine des Windows Media Player.

**BUTTONELEMENT-Objekte** sind in einer **BUTTONGROUP enthalten.** Sie müssen immer mindestens ein **BUTTONELEMENT in** jeder **BUTTONGROUP haben.**

Legen Sie den Play **BUTTONELEMENT-Code** nach der schließenden eckigen Klammer von **BUTTONGROUP ab.**


```C++
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Play"
            onClick = "JScript: player.URL='https://proseware.com/laure.wma';" />

```



Die folgenden Attribute werden verwendet, um **buttonelement für** die Wiedergabeschaltfläche zu definieren:

**mappingColor**

Dies ist der Farbwert eines Bereich in der Zuordnungsartdatei, die Sie zuvor erstellt haben. In diesem Fall ist dies die vollgrüne Farbe. Dieses Attribut ist für alle **BUTTONELEMENT-Objekte erforderlich.** Wenn Sie diese Farbe definieren, geben Sie Windows Media Player an, diesen Farbbereich dem XML-Code dieser Schaltfläche zu zuordnen.

**upToolTip**

Dadurch wird der Text definiert, der angezeigt wird, wenn der Benutzer mit der Maus auf die Schaltfläche zeigt. Verwechseln Sie dies nicht mit der Hoverart, die angezeigt wird. Eine QuickInfo ist eine kleine Sprechblasenbeschriftung, die einen Moment dauert. Das Bild mit der Hoverart wird jedoch sofort in der farbe und form angezeigt, die Sie auswählen.

**Onclick**

Dadurch wird das Ereignis definiert, das auftritt, wenn der Mauszeiger auf die Schaltfläche klickt. Der Wert dieses Ereignisattributs wird als Ereignishandler bezeichnet und ist entweder eine Zeile mit Microsoft JScript-Code oder eine JScript-Funktion in einer externen Textdatei, die vom **loadScript-Attribut** einer VIEW geladen **wird.** In diesem Fall ruft JScript Code die **URL-Methode** von Windows Media Player auf, die eine Datei namens "laure.wma" lädt und abspielt. Beachten Sie, dass die Zeile mit einem Semikolon innerhalb der Anführungszeichen endet, was für JScript ist. Beachten Sie auch die Verwendung von einfachen Anführungszeichen innerhalb der doppelten Anführungszeichen, um den Dateinamen zu deaktivieren. Weitere Informationen zu JScript finden Sie unter [Using JScript](using-jscript.md) im Abschnitt About Skins (Informationen zu Skins) dieses SDK.

Beachten Sie, dass es kein endendes **BUTTONELEMENT-Tag** gibt. Wenn ein Element kein anderes Element umschließt, können Sie es mit dem Schrägstrich direkt vor der schließenden eckigen Klammer schließen. Dadurch wird XML informiert, dass Sie mit diesem Element fertig sind. Beispiel:


```C++
<BUTTONELEMENT></BUTTONELEMENT>
```



und


```C++
<BUTTONELEMENT/>
```



übermitteln die gleichen Informationen in XML.

Die Leistung von Skins entsteht durch die Verwendung von Ereignishandlern. Wenn der Benutzer mit der Maus etwas tut, können Sie dieses Ereignis mit JScript. Bei Ihrem Code kann es sich um eine einzelne Zeile Windows Media Player, die eine einfache Wiedergabe ermöglicht, oder es kann sich um eine vollständige Anwendung in JScript.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen der Skindefinitionsdatei**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




