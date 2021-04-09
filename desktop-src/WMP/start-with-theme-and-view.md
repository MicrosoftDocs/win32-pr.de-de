---
title: Mit Design und Ansicht beginnen
description: Mit Design und Ansicht beginnen
ms.assetid: 1ac92f3a-463a-4343-a269-5230c644b57f
keywords:
- Erstellen von Skins, Theme-Element
- Windows Media Player Skins, Theme-Element
- Skins, Theme-Element
- Skin-Definitions Dateien, Designelement
- Design-Element
- Erstellen von Skins, Ansichts Element
- Windows Media Player Skins, Ansichts Element
- Skins, Ansichts Element
- Skin-Definitions Dateien, Element anzeigen
- View-Element
- Elemente, Ansicht
- Elemente, Design
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499444ee2093e743f58174797794a50fbf74555a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856827"
---
# <a name="start-with-theme-and-view"></a>Mit Design und Ansicht beginnen

Jede Skin muss genau ein Design **Element und mindestens ein** **Ansichts** Element aufweisen.

Erstellen Sie mit dem Text-Editor den folgenden Text:


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "False">


    </VIEW>
</THEME>

```



Belassen Sie vor dem schließenden **Ansichts** Kennzeichen einige leere Zeilen, da Sie später weiteren Code hinzufügen.

Speichern Sie die Datei mit einem beliebigen Dateinamen, die Sie wünschen, aber stellen Sie sicher, dass die Erweiterung. WMS lautet. Ein typischer Dateiname könnte z. b. "skinone. WMS" lauten.

Jede Skin muss mit beginnen <THEME> und mit Enden </THEME>. Es kann nur ein Design **Element in** der Skin vorhanden sein, aber Sie müssen über ein Element verfügen.

Sie müssen auch über mindestens ein **Ansichts** Element verfügen. Sie können mehr als eine Ansicht haben, aber in diesem Beispiel ist nur eine **Ansicht** vorhanden. Sie müssen über ein öffnendes <VIEW> und ein Schließ Endes verfügen <VIEW>. Beachten Sie, dass das öffnende </VIEW> Tag das Tag nicht sofort schließt, sondern mehrere Attribute vor der schließenden Spitze Klammer (>) enthält. In diesem Beispiel werden die folgenden Attribute im **Theme** -Element verwendet:

**clippingcolor**

Das **clippingcolor** -Attribut wird nicht immer benötigt, wenn die Ränder der Skin rechteckig sind. Die Skin in diesem Beispiel ist Oval-geformt, sodass Sie eine clippingfarbe für die Teile der Skin benötigen, über die der Desktop angezeigt werden soll. im Wesentlichen alle Teile außerhalb der Oval. In diesem Beispiel wird ein dunkles gelb verwendet, das als " \# CCCC00" im Webformat angegeben wird. Die Gründe für diese Auswahl werden bei [der Erstellung der primären Grafikdatei](creating-the-primary-art-file.md)angegeben. Im Grunde ist dieser Wert immer eine Zahl, die Sie aus Ihrem Kunstprogramm erhalten.

**backgroundImage**

Dies ist der Name der primären Grafikdatei. Dabei sollte es sich um den genauen Dateinamen und den Pfad der primären Grafikdatei handeln. Nur BMP-, JPG-, GIF-und PNG-Dateien werden unterstützt, und BMP wird empfohlen.

**TitleBar**

Diese Skin besitzt keine **TitleBar**, sodass der Wert "false" lautet. Sie benötigen nur eine Titelleiste, wenn Sie möchten, dass Ihre Skin eine Hintergrundfarbe hat und rechteckig ist.

Stellen Sie sicher, dass Sie die schließende spitze Klammer (>) hinter dem **TitleBar** -Wert ablegen, um anzugeben, dass Sie die **Sicht** definiert haben. Lassen Sie vor der schließenden **Ansicht** **und den** Design Tags einige Leerzeilen. Sie benötigen die Zeilen für Code, die Sie später hinzufügen werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen der Skin-Definitionsdatei**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




