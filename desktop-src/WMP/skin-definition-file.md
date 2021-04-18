---
title: Skin-Definitionsdatei
description: Skin-Definitionsdatei
ms.assetid: ed5f7c61-c830-4075-a79f-d5539454bd3b
keywords:
- Windows Media Player Skins, Skin-Definitions Dateien
- Skins, Skin-Definitions Dateien
- Dateien für Skins, Skin-Definition
- Skin-Definitions Dateien, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bd06708a99a15dc9a8266278850c0507007f058
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340635"
---
# <a name="skin-definition-file"></a>Skin-Definitionsdatei

Skin-Definitions Dateien enthalten die grundlegenden Anweisungen, wie die Skin funktioniert und welche anderen von der Skin verwendeten Dateien gefunden werden können. Es kann nur eine Skin-Definitionsdatei für einen Skin vorhanden sein, die die Dateinamenerweiterung. WMS enthält.

Die Anweisungen in der Skin-Definitionsdatei werden in Extensible Markup Language (XML) geschrieben, die HTML ähnelt. Wenn Sie zum Erstellen von Webseiten HTML verwendet haben, werden Sie feststellen, dass XML vertraut ist.

Der XML-Code in der Skin-Definitionsdatei verwendet einen Satz von speziellen Element Tags, um Teile der Skin-Benutzeroberfläche zu definieren. Beispielsweise definiert das [Button](button-element.md) -Element, wie sich eine Schaltfläche verhält, wo Sie angezeigt wird und wie Sie aussehen soll.

Jedes Elementtag weist bestimmte Attribute auf. Beispielsweise verfügt das [Button](button-element.md) -Element über ein **Image** -Attribut, das definiert, wo das Bild für die Schaltfläche gefunden werden kann. Dies ähnelt HTML, wobei das Body-Element über ein **BgColor** -Attribut verfügt, das die Hintergrundfarbe der HTML-Seite definiert. Ausführliche Informationen zu allen Skin-Elementen und deren Attributen finden Sie im Abschnitt zur Design- [Programmier Referenz](skin-programming-reference.md) .

XML hat einige einfache Regeln, die Sie zum Erstellen von Skins kennen müssen. Im Gegensatz zu HTML erfordert XML, dass Sie die Regeln genau befolgen.

## <a name="enclose-elements-with-angle-brackets"></a>Einschließen von Elementen mit spitzen Klammern

Alle Elemente werden in spitzen Klammern eingeschlossen. Beispielsweise ist das **Button** -Element wie folgt typisiert:


```C++
<BUTTON>

```



Sie müssen das Wort "Button" nicht in Großbuchstaben eingeben, aber die Konvention zum Eingeben von Elementnamen in Großbuchstaben wird im Beispielcode dieses SDK verwendet.

## <a name="put-attributes-before-the-closing-bracket"></a>Attribute vor der schließenden Klammer platzieren

Alle Attribute für ein bestimmtes Element müssen vor der schließenden Spitze Klammer eingeschlossen werden. Ein Attribut besteht aus dem Attributnamen, gefolgt von einem Gleichheitszeichen (=) und dem Wert des Attributs in Anführungszeichen.


```C++
<BUTTON image="mypic.jpg">

```



Sie müssen das Wort "Image" nicht in Kleinbuchstaben eingeben, aber die Konvention der Typisierung von Attributnamen in Kleinbuchstaben wird im Beispielcode dieses SDK verwendet. Beachten Sie außerdem, dass der Wert des-Attributs in Anführungszeichen eingeschlossen ist.

## <a name="opening-and-closing-elements"></a>Öffnende und schließende Elemente

Einige Elemente werden in einem anderen Element gruppiert. Beispielsweise ist das **ButtonGroup** -Element nicht sehr sinnvoll, es sei denn, Sie verwenden ein oder mehrere **ButtonElement** -Elemente. Um die Gruppierung klar zu machen, müssen Sie für jedes Element über ein öffnendes und ein Schließ Endes Tag verfügen. Das öffnende Tag ist nur der Elementname und alle zugehörigen Attribute in spitzen Klammern. Das schließende Tag ist der Elementname, dem ein Schrägstrich (/) vorangestellt und dann durch spitzen Klammern eingeschlossen wird. Beispielsweise sieht das öffnende Tag des **ButtonGroup** -Elements wie folgt aus:


```C++
<BUTTONGROUP>

```



Das schließende **ButtonGroup** -Tag sieht wie folgt aus:


```C++
</BUTTONGROUP>

```



Sie würden die **ButtonElement** -Tags zwischen den öffnenden und schließenden **ButtonGroup** -Element Tags platzieren. Beispiel:


```C++
<BUTTONGROUP>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



## <a name="closing-off-elements"></a>Schließen von Elementen

Wenn ein Element keine anderen Elemente enthält, müssen Sie einen Schrägstrich am Ende des Element namens direkt vor der schließenden Spitze Klammer platzieren. Im obigen Code hat jedes **ButtonElement** -Element z. b. einen Schrägstrich, um anzugeben, dass keine anderen Elemente geschachtelt sind.

Mit anderen Worten, Sie müssen entweder ein Schließ Endes Elementtag haben oder das Element mit einem Schrägstrich schließen.

Dies ist richtig:


```C++
<BUTTONGROUP>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



Dies ist nicht korrekt:


```C++
<BUTTONGROUP/>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



Dies ist auch nicht korrekt:


```C++
<BUTTONGROUP>
    <BUTTONELEMENT>
    <BUTTONELEMENT>
</BUTTONGROUP>

```



Der folgende Abschnitt enthält weitere Informationen zu Skin-Definitions Dateien:

-   [Struktur der Skin-Definitionsdatei](skin-definition-file-structure.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Skin-Dateien**](skin-files.md)
</dt> </dl>

 

 




