---
title: Verwenden des Image-Elements
description: In diesem Artikel wird die Verwendung des Image-Elements in VML beschrieben, einem Feature, das seit Windows Internet Explorer 9 veraltet ist.
ms.assetid: 444c0b21-35f0-4e2d-ab6d-87a88229d9d2
keywords:
- Web-Workshop,image-Element
- Entwerfen von Webseiten,image-Element
- Vector Markup Language (VML),image-Element
- VML (Vector Markup Language),image-Element
- Vektorgrafik,Bildelement
- Bildelement
- VML-Elemente,Image
- VML-Formen, Bildelement
- Vector Markup Language (VML), Zuschneiden von Eigenschaftenattributen
- VML (Vector Markup Language),Zuschneiden von Eigenschaftenattributen
- Vektorgrafiken,Eigenschaftenattribute zuschneiden
- VML-Formen,Eigenschaftenattribute zuschneiden
- Zuschneideeigenschaftenattribute
- Vector Markup Language (VML),gain-Eigenschaftenattribut
- VML (Vector Markup Language),gain-Eigenschaftenattribut
- Vektorgrafiken,Gain-Eigenschaftsattribut
- VML-Formen,Gain-Eigenschaftsattribut
- gain-Eigenschaftenattribut
- Vector Markup Language (VML), Kontrast
- VML (Vector Markup Language),Kontrast
- Vektorgrafiken,Kontrast
- VML-Formen,Kontrast
- Vector Markup Language (VML), blacklevel-Eigenschaftenattribut
- VML (Vector Markup Language),blacklevel-Eigenschaftenattribut
- Vektorgrafiken,Blacklevel-Eigenschaftsattribut
- VML-Formen, Blacklevel-Eigenschaftsattribut
- blacklevel-Eigenschaftenattribut
- Vector Markup Language (VML), Helligkeit
- VML (Vector Markup Language), Helligkeit
- Vektorgrafiken, Helligkeit
- VML-Formen, Helligkeit
- Vector Markup Language (VML), Grayscale-Eigenschaftsattribut
- VML (Vector Markup Language),grayscale-Eigenschaftenattribut
- Vektorgrafik,Grayscale-Eigenschaftsattribut
- VML-Formen,Grayscale-Eigenschaftsattribut
- grayscale-Eigenschaftenattribut
- Vector Markup Language (VML),gamma-Eigenschaftsattribut
- VML (Vector Markup Language),gamma-Eigenschaftenattribut
- Vektorgrafiken, Gammaeigenschaftsattribut
- VML-Formen, Gammaeigenschaftsattribut
- gamma-Eigenschaftsattribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 572acef76afc42e02f476ca1825ef2541f596380
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407803"
---
# <a name="using-the-image-element"></a>Verwenden des Image-Elements

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Verwenden von `<image>`

In diesem Thema wird veranschaulicht, wie das -Element verwendet wird, um `<image>` Bilder mit verschiedenen Sondereffekten anzuzeigen.

Wenn Sie ein Bild anzeigen möchten, das aus einer externen Quelle geladen wurde, verwenden Sie in der Regel das in HTML bereitgestellte Element und verweisen dann das src-Eigenschaftsattribut auf den Speicherort der `<img>` Bilddatei. 

Alternativ können Sie das in `<image>` VML bereitgestellte Element verwenden. Wenn Sie das -Element verwenden, können Sie nur eine Bilddatei erstellen und das Bild dann anders anzeigen, indem Sie die Eigenschaftenattribute `<image>` des Elements `<image>` ändern. Darüber hinaus bietet das -Element mehrere Sondereffekte, die Sie nicht einfach mithilfe des HTML-Elements verwenden können, z. B. zuschneiden, `<image>` kontrastieren, `<img>` [](#crop) [Helligkeit,](#brightness) [Gamma](#gamma)und [Graustufen.](#grayscale) [](#contrast)

[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="crop"></a>Ernte

Sie können die **Eigenschaftenattribute cropbottom**, **croptop**, **cropleft** und **cropright** des Elements verwenden, um verschiedene Bilder anzuzeigen, die aus derselben `<image>` Bilddatei zugeschnitten werden.

Der Wert dieser Zuschneideattribute stellt den Prozentualen Schnitt vom Rand des Bilds dar. Der Wert kann eine beliebige Zahl zwischen 0 und 1 sein. Standardmäßig ist der Wert auf 0 festgelegt, was angibt, dass keine Zuschneide vom Rand entfernt wird. Der Wert 0,1 gibt einen Zuschnitt von 10 Prozent vom Rand an, der Wert 0,15 steht für einen Zuschnitt von 15 Prozent vom Rand und so weiter.

Um beispielsweise fünf Bilder anzuzeigen, die alle aus derselben Bilddatei zugeschnitten wurden, können Sie das -Element verwenden und verschiedene Zuschneidewerte angeben, wie in der folgenden `<image>` VML-Darstellung gezeigt:

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





Das erste Bild , `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` , hat keinen Zuschneidewert. Daher werden 100 Prozent des originalen Bilds mit einer Größe von 100 Punkten um 80 Punkten angezeigt.

Das zweite Bild, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>` , verfügt über einige Zuschneidewerte. `cropbottom="0.2"` gibt an, dass 20 Prozent des Bilds von unten zugeschnitten werden. `cropright="0.15"` gibt an, dass 15 Prozent des Bilds vom rechten Rand aus zugeschnitten werden. Das verbleibende Bild wird dann mit einer Größe von 85 Punkten um 64 Punkten angezeigt.

Auf ähnliche Weise haben das dritte, vierte und fünfte Bild einige Zuschneidewerte. Das ursprüngliche Bild wird gemäß den Zuschneidewerten zugeschnitten und dann entsprechend dem Wert von Breite und Höhe angezeigt.

[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="contrast"></a>Kontrast

Sie können  das Gain-Eigenschaftsattribut des -Elements verwenden, um `<image>` verschiedene Bilder mit unterschiedlichen Kontrasteinstellungen anzuzeigen.

Der Wert  des gain-Eigenschaftsattributs kann eine beliebige Zahl sein. Standardmäßig ist der Wert 1, was die Verwendung des gleichen Kontrasts wie das ursprüngliche Bild angibt. Der Wert 0 gibt keinen Kontrast an. Je größer die Zahl, desto höher der Kontrast.

Wenn Sie beispielsweise fünf Bilder mit unterschiedlichen Kontrasteinstellungen anzeigen möchten, können Sie das -Element verwenden und einen anderen Wert für das gain-Eigenschaftsattribut festlegen, wie in der folgenden `<image>` VML-Darstellung gezeigt: 

![image1.jpg (5770 Bytes)](images/image1.jpg)![image2 \-2.jpg (270 Bytes)](images/image2-2.jpg)![image2 \-3.jpg (1919 Bytes)](images/image2-3.jpg)![image2 \-4.jpg (3143 Bytes)](images/image2-4.jpg)![image2 \-5.jpg (1724 Bytes)](images/image2-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0.5 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=3 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=-0.4 />
```





Wenn  das Gain-Eigenschaftsattribut auf 0 festgelegt ist, wird das gesamte Bild grau, da kein Kontrast besteht. Der Kontrast ist deutlicher,  wenn das Gain-Eigenschaftsattribut auf 3 festgelegt ist, als wenn es auf 0,5 festgelegt ist. Der Kontrast wird umgekehrt, wenn das Gain-Eigenschaftsattribut auf einen negativen Wert wie -0,4 festgelegt ist. 

[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="brightness"></a>Helligkeit

Sie können das **Blacklevel-Eigenschaftsattribut** des Elements verwenden, um verschiedene Bilder `<image>` mit unterschiedlichen Helligkeitseinstellungen anzuzeigen.

Der Wert des **blacklevel-Eigenschaftsattributs** kann ein beliebiger Wert zwischen 0 und 1 sein. Standardmäßig ist der Wert 0, was angibt, dass die Helligkeitsstufe im ursprünglichen Bild beibehalten wird. Der Wert 1 gibt die höchste Helligkeitsstufe an.

Um beispielsweise fünf Bilder mit unterschiedlichen Helligkeitseinstellungen anzuzeigen, können Sie das -Element verwenden und einen anderen Wert für das Blacklevel-Eigenschaftsattribut festlegen, wie in der folgenden `<image>` VML-Darstellung gezeigt: 

![image1.jpg (5770 Bytes)](images/image1.jpg)![image3 \-2.jpg (2579 Bytes)](images/image3-2.jpg)![image3 \-3.jpg (2330 Bytes)](images/image3-3.jpg)![image3 \-4.jpg (2727 Bytes)](images/image3-4.jpg)![image3 \-5.jpg (2435 Bytes)](images/image3-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.1 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.2 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.05 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.15 />
```





[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="grayscale"></a>Graustufe

Sie können das **Grayscale-Eigenschaftsattribut** des Elements verwenden, um Bilder mit oder `<image>` ohne Graustufen anzuzeigen.

Der Wert des **Grayscale-Eigenschaftsattributs** kann entweder true oder false sein. Standardmäßig ist der Wert auf FALSE festgelegt, sodass das Bild in Farbe angezeigt wird. Wenn der Wert auf TRUE festgelegt ist, wird das Bild in Graustufen angezeigt.

Wie in der folgenden Abbildung gezeigt, verwendet das erste Bild beispielsweise die Standardeinstellung (false) des Graustufenattributs ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ). Daher wird das Bild in Farbe angezeigt.

Das zweite Bild legt das Graustufenattribut auf true fest ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ). Daher wird das Bild in Graustufen angezeigt, wie in der folgenden VML-Darstellung gezeigt:

![image1.jpg (5770 Bytes)](images/image1.jpg)![image4 \-2.jpg (2138 Bytes)](images/image4-2.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg"
grayscale=true />
```





[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="gamma"></a>Gamma

Sie können das **Gammaeigenschaftsattribut** des Elements verwenden, um Bilder mit `<image>` unterschiedlichen Gammaeinstellungen anzuzeigen.

Der Wert des Gammaeigenschaftsattributs kann ein beliebiger Wert zwischen 0 und 1 sein. Standardmäßig ist der Wert auf 1 festgelegt.

Um beispielsweise drei Bilder mit unterschiedlichen Gammaeinstellungen anzuzeigen, können Sie das -Element verwenden und einen anderen Wert des Gammaeigenschaftsattributs festlegen, wie in der folgenden `<image>` VML-Darstellung gezeigt: 

![image5 \-1.jpg (2714 Bytes)](images/image5-1.jpg)![image5 \-2.jpg (2729 Bytes)](images/image5-2.jpg)![image5 \-3.jpg (2726 Bytes)](images/image5-3.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0.5 />
```





Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://www.w3.org/TR/NOTE-VML#-toc416858408) .

 

 