---
title: Hinzufügen des "Play"-ButtonElement
description: Hinzufügen des "Play"-ButtonElement
ms.assetid: 895850a7-7538-4581-8348-41cbb3bc9717
keywords:
- Erstellen von Skins, ButtonElement-Element
- Windows Media Player Skins, ButtonElement-Element
- Skins, ButtonElement-Element
- Skin-Definitions Dateien, ButtonElement-Element
- ButtonElement-Element
- Elemente, ButtonElement
- Erstellen von Skins, Wiedergabe Schaltflächen
- Windows Media Player Skins, Wiedergabe Schaltflächen
- Skins, Wiedergabe Schaltflächen
- Skin-Definitions Dateien, Wiedergabe Schaltflächen
- Wiedergabe Schaltflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92b5416adf2e323043eb563ec08e1e4d2525733
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515788"
---
# <a name="adding-the-play-buttonelement"></a>Hinzufügen des "Play"-ButtonElement

Schließlich können Sie die **ButtonElement** -Elemente, die die visuellen Schaltflächen auf dem Bildschirm verbinden, mit Windows-Media Player Aktionen hinzufügen. Dabei handelt es sich um den Kern ihrer Skin, den Sie als Verkabelung der Oberfläche der Skin an die inneren Maschinen von Windows Media Player vorstellen können.

**ButtonElement** s sind in einer **Button Group** enthalten. In jeder **ButtonGroup** muss immer mindestens ein **ButtonElement** vorhanden sein.

Fügen Sie den Code für die Wiedergabe **ButtonElement** nach der schließenden Spitze Klammer der **ButtonGroup** ein.


```C++
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Play"
            onClick = "JScript: player.URL='https://proseware.com/laure.wma';" />

```



Die folgenden Attribute werden verwendet, um das **ButtonElement** für die Wiedergabe Schaltfläche zu definieren:

**mappingColor**

Dies ist der Farbwert eines Bereichs in der Mapping-Grafikdatei, den Sie zuvor erstellt haben. In diesem Fall handelt es sich um eine solide grüne Farbe. Dieses Attribut ist für ein beliebiges **ButtonElement** erforderlich. Wenn Sie diese Farbe definieren, sagen Sie Windows Media Player, diesen Farbbereich dem XML-Code dieser Schaltfläche zuzuordnen.

**uptooltip**

Definiert den Text, der angezeigt wird, wenn der Benutzer mit dem Mauszeiger auf die Schaltfläche zeigt. Verwechseln Sie dies nicht mit der Maus, die angezeigt wird. Eine QuickInfo ist eine kleine Sprechblase, die eine Weile dauert. Das Hover-Kunst Bild wird jedoch sofort in der von Ihnen gewählten Farbe und Form angezeigt.

**OnClick**

Definiert das Ereignis, das auftritt, wenn mit der Maus auf die Schaltfläche geklickt wird. Der Wert dieses Ereignis Attributs wird als Ereignishandler bezeichnet und ist entweder eine Zeile von Microsoft JScript-Code oder eine JScript-Funktion in einer externen Textdatei, die vom **loadscript** -Attribut einer **Ansicht** geladen wird. In diesem Fall ruft der JScript-Code die **URL** -Methode von Windows Media Player auf, die eine Datei mit dem Namen "Laure. wma" lädt und damit beginnt. Beachten Sie, dass die Zeile mit einem Semikolon innerhalb der Anführungszeichen endet, was eine gute JScript-Codierungs Praxis ist. Beachten Sie auch, dass einfache Anführungszeichen innerhalb der doppelten Anführungszeichen verwendet werden, um den Dateinamen festzulegen. Weitere Informationen zu JScript finden Sie im Abschnitt über die [Verwendung von JScript](using-jscript.md) im Abschnitt about Skins dieses SDK.

Beachten Sie, dass kein **endbuttonelement** -Tag vorhanden ist. Wenn ein Element kein anderes Element einschließt, können Sie es mit dem Schrägstrich direkt vor der schließenden Spitze Klammer schließen. Dies teilt XML mit, dass Sie mit diesem Element fertig sind. Beispiel:


```C++
<BUTTONELEMENT></BUTTONELEMENT>
```



und


```C++
<BUTTONELEMENT/>
```



vermitteln Sie dieselben Informationen in XML.

Die Leistungsfähigkeit von Skins ergibt sich aus der Verwendung von Ereignis Handlern. Wenn der Benutzer mit einer Maus etwas bewirkt, kann dieses Ereignis mit JScript behandelt werden. Ihr Code kann eine einzelne Zeile sein, die es Windows Media Player ermöglicht, etwas einfaches Spiel auszuführen, oder es kann sich um eine in JScript geschriebene komplette Anwendung handeln.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen der Skin-Definitionsdatei**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




