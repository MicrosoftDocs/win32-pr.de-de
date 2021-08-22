---
title: Skindefinitionsdatei
description: Skindefinitionsdatei
ms.assetid: ed5f7c61-c830-4075-a79f-d5539454bd3b
keywords:
- Windows Media Player Skins, Skindefinitionsdateien
- Skins, Skindefinitionsdateien
- Dateien für Skins,Skindefinition
- Skindefinitionsdateien,Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7bf162870596968872c4f146772c9e62277f5b2ccb660270794248786a71355
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995240"
---
# <a name="skin-definition-file"></a>Skindefinitionsdatei

Skindefinitionsdateien enthalten die grundlegenden Anweisungen dazu, was die Skin macht und wo andere dateien gefunden werden können, die vom Skin verwendet werden. Es kann nur eine Skindefinitionsdatei für eine Skin geben, und sie hat die Dateinamenerweiterung .wms.

Die Anweisungen in der Skindefinitionsdatei sind in Extensible Markup Language (XML) geschrieben, was HTML ähnelt. Wenn Sie HTML zum Erstellen von Webseiten verwendet haben, werden Sie feststellen, dass XML vertraut aussieht.

Der XML-Code in der Skindefinitionsdatei verwendet einen Satz spezieller Elementtags, um Teile der Skin-Benutzeroberfläche zu definieren. Das [BUTTON-Element](button-element.md) definiert beispielsweise, wie sich eine Schaltfläche verhält, wohin sie wechseln wird und wie sie aussieht.

Jedes Elementtag verfügt über bestimmte Attribute. Das [BUTTON-Element](button-element.md) verfügt beispielsweise über ein Bildattribut, das definiert, wo sich das Bild für die Schaltfläche befindet.  Dies ähnelt HTML, wobei das BODY-Element über ein **bgcolor-Attribut** verfügt, das die Hintergrundfarbe der HTML-Seite definiert. Ausführliche Informationen zu allen Skinelementen und ihren Attributen finden Sie im Abschnitt Skin Programming Reference (Referenz zur [Skinprogrammierung).](skin-programming-reference.md)

XML verfügt über einige einfache Regeln, die Sie kennen müssen, um Skins zu erstellen. Im Gegensatz zu HTML erfordert XML, dass Sie die Regeln genau befolgen.

## <a name="enclose-elements-with-angle-brackets"></a>Einschließen von Elementen mit spitzen Klammern

Alle Elemente werden in spitzen Klammern eingeschlossen. Beispielsweise wird das **BUTTON-Element** wie folgt eingegeben:


```C++
<BUTTON>

```



Sie müssen das Wort "BUTTON" nicht in Großbuchstaben eingeben, aber die Konvention der Eingabe von Elementnamen in Großbuchstaben wird im Beispielcode dieses SDK verwendet.

## <a name="put-attributes-before-the-closing-bracket"></a>Attribute vor der schließenden Klammer setzen

Alle Attribute für ein bestimmtes Element müssen vor der schließenden spitzen Klammer eingeschlossen werden. Ein Attribut besteht aus dem Attributnamen gefolgt von einem Gleichheitszeichen (=) und dem Wert des Attributs in Anführungszeichen.


```C++
<BUTTON image="mypic.jpg">

```



Sie müssen das Wort "image" nicht in Kleinbuchstaben eingeben, aber die Konvention der Eingabe von Attributnamen in Kleinbuchstaben wird im Beispielcode dieses SDK verwendet. Beachten Sie auch, dass der Wert des Attributs in Anführungszeichen eingeschlossen ist.

## <a name="opening-and-closing-elements"></a>Öffnen und Schließen von Elementen

Einige Elemente werden in einem anderen Element gruppiert. Beispielsweise ist das **BUTTONGROUP-Element** nur sinnvoll, wenn Sie mindestens ein **BUTTONELEMENT-Element** damit verwenden. Um die Gruppierung zu deaktivieren, benötigen Sie ein öffnendes und schließendes Tag für jedes Element. Das öffnende Tag ist nur der Elementname und alle zugehörigen Attribute, die von spitzen Klammern umgeben sind. Das schließende Tag ist der Elementname, dem ein Schrägstrich (/) vorangestellt und dann in spitzen Klammern eingeschlossen wird. Das Öffnen des **BUTTONGROUP-Elements** sieht z. B. wie folgt aus:


```C++
<BUTTONGROUP>

```



Das schließende **BUTTONGROUP-Tag** sieht wie folgt aus:


```C++
</BUTTONGROUP>

```



Sie würden die **BUTTONELEMENT-Tags** zwischen den öffnenden und schließenden **BUTTONGROUP-Elementtags** setzen. Beispiel:


```C++
<BUTTONGROUP>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



## <a name="closing-off-elements"></a>Schließen von Elementen

Wenn ein Element keine anderen Elemente enthält, müssen Sie einen Schrägstrich am Ende des Elementnamens direkt vor der schließenden spitzen Klammer setzen. Im obigen Code weist jedes **BUTTONELEMENT-Element** beispielsweise einen Schrägstrich auf, um anzugeben, dass keine anderen Elemente darin geschachtelt sind.

Anders ausgedrückt: Sie müssen entweder über ein schließende Elementtag verfügen oder Ihr Element mit einem Schrägstrich schließen.

Dies ist richtig:


```C++
<BUTTONGROUP>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



Dies ist nicht richtig:


```C++
<BUTTONGROUP/>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



Dies ist auch nicht richtig:


```C++
<BUTTONGROUP>
    <BUTTONELEMENT>
    <BUTTONELEMENT>
</BUTTONGROUP>

```



Der folgende Abschnitt enthält weitere Informationen zu Skindefinitionsdateien:

-   [Struktur der Skindefinitionsdatei](skin-definition-file-structure.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Skindateien**](skin-files.md)
</dt> </dl>

 

 




