---
title: Href-Attribut (imagedata) (VML)
description: Href-Attribut (imagedata) (VML)
ms.assetid: vs|vml|~\shape\image\image_href.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4ea1c5a5eb4c37773d012c1ff888aa372cb7717
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727432"
---
# <a name="href-attribute-imagedatavml"></a>Href-Attribut (imagedata) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert eine URL für ein Bild. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[ImageData](msdn-online-vml-imagedata-element.md)

**Tagsyntax**

<v: *Element* o:href = " *Expression* " >

**Skript Syntax**

*Element* . href = "*Ausdruck*"

*Ausdruck* = *Element*. href

**Anmerkungen**

Beim Klicken auf die Form wird die URL vom Browser geladen. Das **href** -Attribut ähnelt dem standardmäßigen HTML- **href** -Attribut von Ankern.

Die Verwendung dieses Attributs vereinfacht das Erstellen von buttonswith-Bildern auf einer Webseite.

Dieses Attribut wird nur von Microsoft Office verwendet, wenn ein Bild verknüpft und eingebettet wurde. Microsoft Word verfügt über eine Benutzeroberfläche zum Einfügen von Bildern auf diese Weise.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Wenn auf das Bild geklickt wird, lädt der Browser die Microsoft Corporation-Startseite.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata o:href="https://www.microsoft.com" src="kids.jpg"/>
   </v:shape>
```



 

 