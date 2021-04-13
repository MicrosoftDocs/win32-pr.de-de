---
title: Src-Attribut (Fill) (VML)
description: Src-Attribut (Fill) (VML)
ms.assetid: 88ad9413-1863-41e2-855b-2bf155ce23cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fddfcc6bb0ba7b4b026287c1efbbd8a20e09c37a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473197"
---
# <a name="src-attribute-fillvml"></a>Src-Attribut (Fill) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert das Bild, das für eine Füllung geladen werden soll. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *Element* src = " *Expression* " >

**Skript Syntax**

*Element* . src = "*Ausdruck * * *"**

*Ausdruck* = *Element*. src

**Anmerkungen**

Die URL zu einem Bild, das für Bild-und Muster Füllungen geladen werden soll. Dieses Attribut muss immer vorhanden sein und auf gültige Bilddaten zeigen, damit ein Bild angezeigt wird. Wenn dieses Attribut allein angezeigt wird (d. h. kein **href** -oder **Title** -Attribut), wird das Bild verknüpft.

*VML-Standard Attribut*

**Beispiel**

Ein gekacheltes Bild, das die Datei myimage.gif als Quelle verwendet, wird angezeigt.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="tile" src="myimage.gif"/>
   </v:shape>
```



 

 