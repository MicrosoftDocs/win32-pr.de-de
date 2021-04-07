---
title: Src-Attribut (Strich) (VML)
description: Src-Attribut (Strich) (VML)
ms.assetid: dac6b5b7-2038-4534-97e9-a1340102777e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b5833b24abf0f16c6e17fa3319931565ee6c232
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727544"
---
# <a name="src-attribute-strokevml"></a>Src-Attribut (Strich) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert das Quell Bild, das für einen Strich Füllvorgang geladen werden soll. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Stellung](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v: *Element* src = " *Expression* " >

**Skript Syntax**

*Element* . src = "*Ausdruck*"

*Ausdruck* = *Element*. src

**Anmerkungen**

Die URL zu einem Bild, das für Bild-und Muster Füllungen geladen werden soll. Dieses Attribut muss immer vorhanden sein und auf gültige Bilddaten zeigen, damit ein Bild angezeigt wird. Wenn dieses Attribut allein angezeigt wird, d. h. kein **href** oder **Title**, wird das Bild verknüpft.

*VML-Standard Attribut*

**Beispiel**

Der Strich wird mit dem Bild erstellt, das von der cylinder.gif Datei angegeben wird.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke src="cylinder.gif" filltype="tile" width="10pt"/>
   </v:shape>
```





 

 