---
title: VML-Master Attribut
description: VML-Master Attribut
ms.assetid: ec661dc6-8e1c-47a3-ad3a-e1ee7e64c840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d6c34fe49c107ed7ee1b4c1fb90d31bb07f17a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102315"
---
# <a name="vml-master-attribute"></a>VML-Master Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt, ob ein **ShapeType** -Element ein Master Element ist. Lese-/Schreibzugriff. **Vgder State**.

**Gilt für**

[ShapeType](msdn-online-vml-shapetype-element.md)

**Tagsyntax**

<v: *Element* o:Master = " *Ausdruck* " >

**Anmerkungen**

**True** gibt an, dass die Form **ShapeType** von der Rendering-Engine gerendert wird. Der Standardwert ist **False**.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Das **ShapeType** -Element ist eine masterform.


```HTML
   <v:shapetype id="laure"
   coordorigin= "0 0" coordsize="200 200"
   fillcolor= "red" o:master="True"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shapetype>
```



 

 