---
title: ID-Attribut (Fill) (VML)
description: ID-Attribut (Fill) (VML)
ms.assetid: 56865772-51bd-4729-8e56-6b00e3c6bed0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4820c4f7a23cf940c199f27243d8ad5601390a84
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039264"
---
# <a name="id-attribute-fillvml"></a>ID-Attribut (Fill) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Ein Name, der einen eindeutigen Bezeichner für eine Füllung bereitstellt. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *Element* -ID = " *Ausdruck* " >

**Skript Syntax**

*Element* . ID = "*Ausdruck*"

*Ausdruck* = *Element*. ID

**Anmerkungen**

Verwenden Sie **ID** , um auf eine bestimmte Füllung zu verweisen. Nachdem Sie eine Füllung erstellt und eine ID angegeben haben, können Sie den ID-Namen verwenden, wenn Sie die Füllung bearbeiten möchten.

*VML-Standard Attribut*

**Beispiel**

Die Form hat eine Fill-ID mit dem Namen "myfill".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill id="myfill"/>
   </v:shape>
```



 

 