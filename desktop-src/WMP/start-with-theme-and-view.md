---
title: Beginnen Sie mit THEME und VIEW.
description: Beginnen Sie mit THEME und VIEW.
ms.assetid: 1ac92f3a-463a-4343-a269-5230c644b57f
keywords:
- Erstellen von Skins, THEME-Element
- Windows Media Player Skins, THEME-Element
- skins,THEME-Element
- Skindefinitionsdateien,THEME-Element
- THEME-Element
- Erstellen von Skins, VIEW-Element
- Windows Media Player Skins, VIEW-Element
- skins,VIEW-Element
- Skindefinitionsdateien,VIEW-Element
- VIEW-Element
- elements,VIEW
- elements,THEME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51bcb18a9d56a8780e56d81d6de60ca269036c72
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883718"
---
# <a name="start-with-theme-and-view"></a>Beginnen Sie mit THEME und VIEW.

Jede Skin muss genau ein **THEME-Element** und mindestens ein **VIEW-Element** aufweisen.

Erstellen Sie in Ihrem Text-Editor den folgenden Text:


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "False">


    </VIEW>
</THEME>

```



Lassen Sie einige leere Zeilen vor dem schließenden **VIEW-Tag,** da Sie später hier weiteren Code hinzufügen werden.

Speichern Sie Ihre Datei mit einem beliebigen Dateinamen, aber stellen Sie sicher, dass die Erweiterung WMS lautet. Ein typischer Dateiname kann beispielsweise skinone.wms sein.

Jede Skin muss mit THEME beginnen &lt; &gt; und mit </THEME> enden. Sie können nur ein **THEME-Element** in Ihrer Skin haben, aber Sie müssen über eines verfügen.

Außerdem benötigen Sie mindestens ein **VIEW-Element.** Sie können mehr als eine **VIEW-Ansicht** verwenden, aber in diesem Beispiel ist nur eine ansichtssynthalten. Sie müssen über eine öffnende &lt; &gt; VIEW- und eine schließende &lt; VIEW -Ansicht &gt; verfügen. Beachten Sie, dass das öffnende &lt; &gt; /VIEW-Tag das Tag nicht sofort schließt, sondern mehrere Attribute vor der schließenden spitzen Klammer (>) enthält. Die folgenden Attribute werden in diesem Beispiel im **THEME-Element** verwendet:

**clippingColor**

Sie benötigen nicht immer das **ClippingColor-Attribut,** wenn die Ränder der Skin rechteckig sind. Die Skin in diesem Beispiel ist oval, sodass Sie eine Ausschneidefarbe für die Teile der Skin benötigen, über die Sie den Desktop sehen möchten. im Wesentlichen alle Teile außerhalb des Ovals. In diesem Beispielskin verwenden wir ein dunkelgelbes, das im Webformat als \# "CSVC00" angegeben ist. Die Gründe für diese Auswahl sind unter [Erstellen der primären Art-Datei](creating-the-primary-art-file.md)angegeben. Im Wesentlichen ist dieser Wert immer eine Zahl, die Sie aus Ihrem Grafikprogramm erhalten.

**backgroundImage**

Dies ist der Name der primären Grafikdatei. Dabei sollte es sich um den genauen Dateinamen und Pfad Ihrer primären Grafikdatei befinden. Es werden nur BMP-, JPG-, GIF- und PNG-Dateien unterstützt, und BMP wird empfohlen.

**Titlebar**

Diese Skin hat keine **titleBar,** sodass der Wert "false" lautet. Sie möchten nur eine Titelleiste, wenn Ihre Skin eine Hintergrundfarbe aufweisen und rechteckig sein soll.

Stellen Sie sicher, dass Sie die schließende spitze Klammer (>) nach dem **titleBar-Wert** setzen, um anzugeben, dass Sie die Definition von **VIEW** abgeschlossen haben. Lassen Sie einige Leere Zeilen vor den schließenden **VIEW-** und **THEME-Tags.** Sie benötigen die Zeilen für Code, den Sie später hinzufügen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen der Skindefinitionsdatei**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




