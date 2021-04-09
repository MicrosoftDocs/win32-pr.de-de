---
title: VML focussize-Attribut
description: VML focussize-Attribut
ms.assetid: 6ca5af2c-3064-423f-a7bb-202f23bf95da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8149973932e9601be2caa0306eefcec08951b238
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039583"
---
# <a name="vml-focussize-attribute"></a>VML focussize-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die Fokus Größe für radiale Füllungen. Lese-/Schreibzugriff. **VgVector2D**.

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *Element* focussize = " *Expression* " >

**Skript Syntax**

*Element* . focussize = "*Ausdruck*"

*Ausdruck* = *Element*. focussize

**Anmerkungen**

Die Werte sind Bruchteile der Breite und Höhe der Form. Der erste Wert ist ein Prozentsatz der Füllung am rechten Rand der Form, und der zweite Wert ist ein Prozentsatz der Füllung bis zum unteren Rand der Form. Der Standardwert ist 0,0. Ein **focussize** -Wert von 100%, 100% und eine **focusposition** von 0 (null) würde dazu führen, dass color2 die Mischung vollständig beherrschen würde. Für ausgeglichene Mischungen werden kleine Werte von ca. 10%, 10% empfohlen.

*VML-Standard Attribut*

**Beispiel**

Die radiale Füllung erstellt eine Mischung, die in der Mitte als blau beginnt und an allen vier Rändern rot wird. Der Mittelpunkt der Blend wird durch **focusposition** definiert, und die Größe der inneren anfangs Farbe wird durch **focussize** bestimmt.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l1,200, 200,200, 200,1 x e">
   <v:fill type="gradientradial" color="red" color2="blue"
   focusposition=".5,.5" focussize=".1,.1"/>
   </v:shape>
```



 

 