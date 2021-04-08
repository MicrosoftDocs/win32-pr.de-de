---
title: Color2-Attribut (Schatten) (VML)
description: Color2-Attribut (Schatten) (VML)
ms.assetid: 265d189a-1a11-4f57-9299-1bc1efd13595
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e735d7672457153881d384c7b625199cf4a202e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729193"
---
# <a name="color2-attribute-shadowvml"></a>Color2-Attribut (Schatten) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die zweite Farbe eines Schattens. Lese-/Schreibzugriff. **Vgcolor**.

**Gilt für**

[Shadow](msdn-online-vml-shadow-element.md)

**Tagsyntax**

<v: *Element* color2 = " *Ausdruck* " >

**Skript Syntax**

*Element* . color2 = "*Ausdruck*"

*Ausdruck* = *Element*. color2

**Anmerkungen**

Verwenden Sie eine zweite Farbe, um besondere Schatteneffekte zu erstellen. Weitere Informationen zu zweiten Farben finden Sie unter dem [Type](type-attribute--shadow--vml.md) -Attribut.

*VML-Standard Attribut*

**Beispiel**

Der Schatten ist für eine zweite Farbe blau.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="green" color2="blue"/>
   </v:shape>
```



 

 