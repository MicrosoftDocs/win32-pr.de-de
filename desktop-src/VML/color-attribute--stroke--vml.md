---
title: Color-Attribut (Strich) (VML)
description: Color-Attribut (Strich) (VML)
ms.assetid: 8fa19789-0bd6-4e9f-8af4-566155eafc6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faa91522adcba5fa854d4749dc257f5489969270
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339902"
---
# <a name="color-attribute-strokevml"></a>Color-Attribut (Strich) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die Farbe eines Strichs. Lese-/Schreibzugriff. **Vgcolor**.

**Gilt für**

[Stellung](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v: *Element* Color = " *Expression* " >

**Skript Syntax**

*Element* . Color = "*Ausdruck*"

*Ausdruck* = *Element*. Color

**Anmerkungen**

Überschreibt das **strokeColor** -Attribut einer Form. Der Standardwert ist **schwarz**.

*VML-Standard Attribut*

**Beispiel**

Die Form hat eine Strichfarbe, die **grün** ist, nicht **rot**.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke color="green"/>
   </v:shape>
```



 

 