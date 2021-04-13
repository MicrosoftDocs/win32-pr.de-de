---
title: ID-Attribut (Image) (VML)
description: ID-Attribut (Image) (VML)
ms.assetid: d85a6d56-5896-4ac0-85c7-0edc72928c62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40ac489331699ca6fe040cddc0bebb408d524de7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390974"
---
# <a name="id-attribute-imagevml"></a>ID-Attribut (Image) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert einen Namen, der einen eindeutigen Bezeichner für ein Bild bereitstellt. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[ImageData](msdn-online-vml-imagedata-element.md)

**Tagsyntax**

<v: *Element* -ID = " *Ausdruck* " >

**Skript Syntax**

*Element* . ID = "*Ausdruck*"

*Ausdruck* = *Element*. ID

**Anmerkungen**

Verwenden Sie **ID** , um auf ein bestimmtes Image zu verweisen. Nachdem Sie ein Image erstellt und eine ID angegeben haben, können Sie den ID-Namen verwenden, wenn Sie das Abbild bearbeiten möchten.

**VML-Standard Attribut**

**Beispiel**

Die Form hat eine **imagedata** -ID mit dem Namen "MyImage".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata id="myimage" src="kids.jpg"/>
   </v:shape>
```



 

 