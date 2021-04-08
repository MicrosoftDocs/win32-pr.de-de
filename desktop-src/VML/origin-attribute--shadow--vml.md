---
title: Origin-Attribut (Schatten) (VML)
description: Origin-Attribut (Schatten) (VML)
ms.assetid: acef5134-dad6-4ba6-9d70-a9f56cd8c5ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 481c3df832ec08bc193db021244049fae96d9e34
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729993"
---
# <a name="origin-attribute-shadowvml"></a>Origin-Attribut (Schatten) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den Mittelpunkt des Schattens. Lese-/Schreibzugriff. **VgVector2D**.

**Gilt für**

[Shadow](msdn-online-vml-shadow-element.md)

**Tagsyntax**

<v: *Element* Origin = " *Expression* " >

**Skript Syntax**

*Element* . Origin = "*Ausdruck*"

*Ausdruck* = *Element*. Origin

**Anmerkungen**

Ein paar von Dezimalstellen Werten der Form, von 50% bis-50%. Der Standardwert ist 0,0.

*VML-Standard Attribut*

**Beispiel**

Der Schatten weist einen Ursprung auf, der 20% nach unten und 20% rechts vom Ursprung der Form ist.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" origin="20%,20%"/>
   </v:shape>
```



 

 