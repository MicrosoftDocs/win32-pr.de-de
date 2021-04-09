---
title: VML-textpathok-Attribut
description: VML-textpathok-Attribut
ms.assetid: 5d061258-1c4d-4391-81ce-13af90a4231c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06046a4f29c147ef109f0e4670d9965bab77a9fa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858278"
---
# <a name="vml-textpathok-attribute"></a>VML-textpathok-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt, ob ein Textpfad angezeigt wird. Lese-/Schreibzugriff. **Vgder State**.

**Gilt für**

[Pfad](msdn-online-vml-path-element.md)

**Tagsyntax**

<v: *Element* textpathok = " *Ausdruck* " >

**Skript Syntax**

- *Element* . textpathok = "*Ausdruck*"

*Ausdruck* = - *Element*. textpathok

**Anmerkungen**

Wenn der Wert **false** ist, kann der Pfad keinen Textpfad enthalten. Der Standardwert ist **False**. Dieses Attribut muss auf " **true** " festgelegt sein, um Text in einem Pfad anzuzeigen.

*VML-Standard Attribut*

**Beispiel**

Die Form weist einen Textpfad auf. Der Text "Hello VML" wird in einer Lächeln förmigen Kurve angezeigt.


```HTML
   <v:curve id="tc" style="position:relative"
   from="50px 100px" to="400px 100px"
   control1="200px 200px" control2="300px 200px">
   <v:stroke weight="1pt" color="blue"
   filltype="solid"/>
   <v:fill on="True" color="yellow" color2="green" type="gradient"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" id="mytp"
   style="font:normal normal normal 36pt Arial"
   fitpath="True" string="Hello VML"/>
   </v:curve>
```



 

 