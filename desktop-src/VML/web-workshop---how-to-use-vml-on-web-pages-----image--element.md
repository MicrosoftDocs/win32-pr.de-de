---
title: Verwenden des Image-Elements
description: In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.
ms.assetid: 444c0b21-35f0-4e2d-ab6d-87a88229d9d2
keywords:
- Webworkshop, Image-Element
- Entwerfen von Webseiten, Image-Element
- Vector Markup Language (VML), Image-Element
- VML (Vector Markup Language), Image-Element
- Vektorgrafiken, Bildelement
- Bildelement
- VML-Elemente, Bild
- VML-Formen, Image-Element
- Vector Markup Language (VML), Attribute für Zuschneiden von Eigenschaften
- VML (Vector Markup Language), Attribute der zuschnittschaft
- Vektorgrafiken, Attribute für Zuschneiden von Eigenschaften
- VML-Formen, Attribute für Zuschneiden von Eigenschaften
- Attribute der zuschnitteigenschaften
- Vector Markup Language (VML), Eigenschafts Attribut erhalten
- VML (Vector Markup Language), Eigenschafts Attribut erhalten
- Vektorgrafiken, Eigenschafts Attribut gewinnen
- VML-Formen, Eigenschafts Attribut gewinnen
- Eigenschafts Attribut erhalten
- Vector Markup Language (VML), Kontrast
- VML (Vector Markup Language), Kontrast
- Vektorgrafiken, Kontrast
- VML-Formen, Kontrast
- Vector Markup Language (VML), Attribut der Blacklevel-Eigenschaft
- VML (Vector Markup Language), Attribut der Blacklevel-Eigenschaft
- Vektorgrafiken, Attribut der Blacklevel-Eigenschaft
- VML-Formen, Attribut der Blacklevel-Eigenschaft
- Attribut der Blacklevel-Eigenschaft
- Vector Markup Language (VML), Helligkeit
- VML (Vector Markup Language), Helligkeit
- Vektorgrafiken, Helligkeit
- VML-Formen, Helligkeit
- Vector Markup Language (VML), Graustufen Eigenschafts Attribut
- VML (Vector Markup Language), Graustufen Eigenschafts Attribut
- Vektorgrafiken, Graustufen Eigenschafts Attribut
- VML-Formen, Graustufen Eigenschafts Attribut
- Graustufen-Eigenschafts Attribut
- Vector Markup Language (VML), Gamma Property-Attribut
- VML (Vector Markup Language), Gamma Property-Attribut
- Vektorgrafiken, Gamma Property-Attribut
- VML-Formen, Gamma Property-Attribut
- Gamma Property-Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 820039ff76f3685eeea7a65e2bbc01578abbe581
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517048"
---
# <a name="using-the-image-element"></a>Verwenden des Image-Elements

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Verwenden von `<image>`

In diesem Thema wird veranschaulicht, wie das-Element verwendet wird, `<image>` um Bilder mit verschiedenen speziellen Effekten anzuzeigen.

Wenn Sie ein Bild anzeigen möchten, das aus einer externen Quelle geladen wurde, verwenden Sie in der Regel das `<img>` in HTML bereitgestellte-Element, und zeigen Sie dann das **src** -Eigenschafts Attribut auf den Speicherort der Bilddatei.

Alternativ können Sie das-Element verwenden, das `<image>` in VML bereitgestellt wird. Wenn Sie das- `<image>` Element verwenden, können Sie nur eine Bilddatei erstellen und das Bild dann unterschiedlich anzeigen, indem Sie die Eigenschafts Attribute des- `<image>` Elements ändern. Außerdem bietet das- `<image>` Element einige besondere Effekte, die Sie nicht verwenden können, indem Sie einfach das- `<img>` Element von HTML verwenden, wie z. b. das [Ausschneiden](#crop), den [Kontrast](#contrast), die [Helligkeit](#brightness), [Gamma](#gamma)und [grau](#grayscale)Stufen.

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="crop"></a>an

Sie können die Eigenschaften Attribute **CropBottom**, **CropTop**, **CropLeft** und **CropRight** des-Elements verwenden `<image>` , um unterschiedliche Bilder anzuzeigen, die aus derselben Bilddatei zugeschnitten werden.

Der Wert dieser zuschnittsattribute stellt den Prozentsatz aus dem Rand des Bilds dar. Der Wert kann eine beliebige Zahl zwischen 0 und 1 sein. Standardmäßig wird der Wert auf 0 festgelegt, was bedeutet, dass keine Zuschneiden von der Kante erfolgt. Der Wert 0,1 gibt an, dass 10 Prozent von der Kante abgeschnitten werden. der Wert 0,15 gibt an, dass der Rand 15 Prozent überspringt usw.

Wenn Sie z. b. fünf Bilder anzeigen möchten, die alle aus derselben Bilddatei entfernt wurden, können Sie das `<image>` -Element verwenden und andere zuschnittwerte angeben, wie in der folgenden VML-Darstellung dargestellt:

![image1.jpg (5770 Bytes)](images/image1.jpg)![image1 \-2.jpg (1969 Bytes)](images/image1-2.jpg)![image1 \-3.jpg (1148 Bytes)](images/image1-3.jpg)![image1 \-4.jpg (1686 Bytes)](images/image1-4.jpg)![image1 \-5.jpg (1364 Bytes)](images/image1-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:85pt;height:64pt' src="image1.jpg"
cropbottom="0.2" cropright="0.15"/>
<v:image style='width:50pt;height:44pt' src="image1.jpg"
cropbottom="0.45" cropleft="0.5"/>
<v:image style='width:80pt;height:56pt' src="image1.jpg"
croptop="0.3" cropright="0.2"/>
<v:image style='width:70pt;height:48pt' src="image1.jpg"
croptop="0.4" cropleft="0.3"/>
```





Das erste Bild, `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` , verfügt über keinen zuschöpfungs Wert. Aus diesem Grund wird 100 Prozent des ursprünglichen Abbilds mit einer Größe von 100 Punkten um 80 Punkte angezeigt.

Das zweite Bild, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>` , weist einige zuschnittwerte auf. `cropbottom="0.2"` Gibt an, dass 20 Prozent des Bilds vom unteren Rand abgeschnitten werden. `cropright="0.15"` gibt an, dass 15 Prozent des Bilds vom rechten Rand abgeschnitten werden. Das verbleibende Bild wird dann mit einer Größe von 85 Punkten um 64 Punkte angezeigt.

Ähnlich weisen die Dritten, vierten und fünften Bilder einige zuschnittwerte auf. Das ursprüngliche Bild wird entsprechend den zuschnittwerten zugeschnitten und dann entsprechend dem Wert von Width und Height angezeigt.

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="contrast"></a>Kontrast

Sie können das Attribut "Eigenschaft **erwerben** " des- `<image>` Elements verwenden, um verschiedene Bilder mit unterschiedlichen Kontrasteinstellungen anzuzeigen.

Der Wert des Attributs für die **Attribut Eigenschaft kann** beliebig sein. Standardmäßig ist der Wert 1, was die Verwendung des gleichen Kontrast wie das ursprüngliche Bild angibt. Der Wert 0 gibt keinen Kontrast an. Je größer die Zahl, desto höher der Kontrast.

Wenn Sie z. b. fünf Bilder mit unterschiedlichen Kontrasteinstellungen anzeigen möchten, können Sie das `<image>` -Element verwenden und einen anderen Wert für das Attribut "Eigenschaft **erhalten** " festlegen, wie in der folgenden VML-Darstellung dargestellt:

![image1.jpg (5770 Bytes)](images/image1.jpg)![Image2 \-2.jpg (270 bytes)](images/image2-2.jpg)![Image2 \-3.jpg (1919 Bytes)](images/image2-3.jpg)![Image2 \-4.jpg (3143 Bytes)](images/image2-4.jpg)![Image2 \-5.jpg (1724 Bytes)](images/image2-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0.5 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=3 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=-0.4 />
```





Wenn das Attribut für die Eigenschaft " **Gewinn** " auf 0 festgelegt ist, wird das gesamte Bild grau, da kein Kontrast vorliegt. Der Kontrast ist deutlicher, wenn das Attribut für die Eigenschaft " **Gewinn** " auf den Wert "0,5" festgelegt ist. Der Kontrast wird umgekehrt, wenn das Attribut für die Eigenschaft " **Gewinn** " auf einen negativen Wert wie "-0,4" festgelegt ist.

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="brightness"></a>Helligkeit

Sie können das Attribut der **Blacklevel** -Eigenschaft des- `<image>` Elements verwenden, um verschiedene Bilder mit unterschiedlichen Helligkeitseinstellungen anzuzeigen.

Der Wert des Attributs der **Blacklevel** -Eigenschaft kann ein beliebiger Wert zwischen 0 und 1 sein. Standardmäßig ist der Wert 0 (null) und gibt an, dass die Ebene der Helligkeit im ursprünglichen Bild beibehalten wird. Der Wert 1 gibt den höchsten Grad an Helligkeit an.

Wenn Sie z. b. fünf Bilder mit unterschiedlichen Helligkeitseinstellungen anzeigen möchten, können Sie das `<image>` -Element verwenden und einen anderen Wert für das Attribut der **Blacklevel** -Eigenschaft festlegen, wie in der folgenden VML-Darstellung dargestellt:

![image1.jpg (5770 Bytes)](images/image1.jpg)![image3 \-2.jpg (2579 Bytes)](images/image3-2.jpg)![image3 \-3.jpg (2330 Bytes)](images/image3-3.jpg)![image3 \-4.jpg (2727 Bytes)](images/image3-4.jpg)![image3 \-5.jpg (2435 Bytes)](images/image3-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.1 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.2 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.05 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.15 />
```





[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="grayscale"></a>Graustufe

Sie können das **Graustufen** Eigenschafts Attribut des- `<image>` Elements verwenden, um Bilder mit oder ohne Graustufen anzuzeigen.

Der Wert des **Graustufen** Eigenschafts Attributs kann entweder "true" oder "false" sein. Standardmäßig ist der Wert auf false festgelegt, damit das Bild in Farbe angezeigt wird. Wenn der Wert auf true festgelegt ist, wird das Bild in Graustufen angezeigt.

Beispielsweise verwendet das erste Bild, wie in der folgenden Abbildung gezeigt, die Standardeinstellung (false) des Graustufen-Attributs ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ). Daher wird das Bild in Farbe angezeigt.

Das zweite Bild legt das Graustufen Attribut auf "true ()" fest `<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` . Daher wird das Bild in Graustufen angezeigt, wie in der folgenden VML-Darstellung dargestellt:

![image1.jpg (5770 Bytes)](images/image1.jpg)!["image4 \-2.jpg (2138 Bytes)](images/image4-2.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg"
grayscale=true />
```





[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="gamma"></a>Gamma

Sie können das **Gamma** Property-Attribut des- `<image>` Elements verwenden, um Bilder mit unterschiedlichen Gamma Einstellungen anzuzeigen.

Der Wert des Gamma property-Attributs kann ein beliebiger Wert zwischen 0 und 1 sein. Standardmäßig ist der Wert auf 1 festgelegt.

Wenn Sie z. b. drei Bilder mit unterschiedlichen Gamma Einstellungen anzeigen möchten, können Sie das `<image>` -Element verwenden und einen anderen Wert des **Gamma** property-Attributs festlegen, wie in der folgenden VML-Darstellung gezeigt:

![image5 \-1.jpg (2714 Bytes)](images/image5-1.jpg)![image5 \-2.jpg (2729 Bytes)](images/image5-2.jpg)![image5 \-3.jpg (2726 Bytes)](images/image5-3.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0.5 />
```





Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://www.w3.org/TR/NOTE-VML#-toc416858408) .

 

 