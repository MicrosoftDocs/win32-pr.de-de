---
title: VML imagealignshape-Attribut
description: VML imagealignshape-Attribut
ms.assetid: 45d72560-ab64-4e85-b495-88f1557a62f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82aaab9c4c470b41bcf9fdb96ee2c048a7d0b81d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315620"
---
# <a name="vml-imagealignshape-attribute"></a>VML imagealignshape-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt die Ausrichtung des Strich Bilds. Lese-/Schreibzugriff. **Vgder State**.

**Gilt für**

[Stellung](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v:

Element *imagealignshape = "* Expression *" #b0*

**Skript Syntax**

Element *. imagealignshape = "* Ausdruck *"*

Expression- *=* Element *. imagealignshape*

**Anmerkungen**

Wenn **true**, wird das Bild mit der Form ausgerichtet, andernfalls wird das Bild an das Fenster ausgerichtet. Der Standardwert ist **True**.

*VML-Standard Attribut*

**Beispiel**

Das Bild wird am Fenster ausgerichtet.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red" strokeweight="20pt"
   style="top:20;left:20;width:300;height:300"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imagealignshape="false" width="5pt" filltype="tile" src="cylinder.gif"/>
   </v:shape>
```



 

 