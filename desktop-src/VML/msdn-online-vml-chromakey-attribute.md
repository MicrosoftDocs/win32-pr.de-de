---
title: VML Chromakey-Attribut
description: VML Chromakey-Attribut
ms.assetid: 937ced3f-2e55-4a22-a9e0-83dc198104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b69b10fe617de23783cf5e2e69b8b1a97b82fa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315633"
---
# <a name="vml-chromakey-attribute"></a>VML Chromakey-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den Farbwert des Bilds, das als transparent behandelt wird. Lese-/Schreibzugriff. **Vgcolor**.

**Gilt für**

[ImageData](msdn-online-vml-imagedata-element.md)

**Tagsyntax**

<v: *Element* Chromakey = " *Expression* " >

**Skript Syntax**

*Element* . Chromakey = "*Ausdruck*"

*Ausdruck* = *Element*. Chromakey

**Anmerkungen**

Verwenden Sie dieses Attribut, um Teile eines Bilds transparent zu machen, indem Sie die Transparenz an eine bestimmte Farbe anschlüsseln. Wenn Sie z. b. den **Chromakey** -Wert **schwarz** machen, ist jeder Teil des Bilds, der schwarz ist, transparent, und die Füllfarbe wird in diesem Teil des Bilds angezeigt.

*VML-Standard Attribut*

**Beispiel**

Die Bereiche des Bilds, die solide schwarz sind, werden transparent, sodass die grüne Füllfarbe stattdessen durch diese Bereiche angezeigt werden kann.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="green"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata chromakey="black" src="kids.jpg"/>
   </v:shape>
```



 

 