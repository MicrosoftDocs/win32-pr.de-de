---
title: Color-Attribut (Fill) (VML)
description: Color-Attribut (Fill) (VML)
ms.assetid: 38e75bf5-4da9-4c58-af86-3554d03a6b7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8480b3a013add36533a82b31338fba301e8353db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473221"
---
# <a name="color-attribute-fillvml"></a>Color-Attribut (Fill) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die Farbe einer Füllung. Lese-/Schreibzugriff. **Vgcolor**.

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *Element* Color = " *Expression* " >

**Skript Syntax**

*Element* . Color = "*Ausdruck*"

*Ausdruck* = *Element*. Color

**Anmerkungen**

Überschreibt das **FillColor** -Attribut einer Form. Der Standardwert ist **weiß**.

*VML-Standard Attribut*

**Beispiel**

Die Füllfarbe der Form ist grün.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="green"/>
   </v:shape>
```



 

 