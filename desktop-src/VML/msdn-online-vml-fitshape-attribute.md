---
title: VML-fitshape-Attribut
description: VML-fitshape-Attribut
ms.assetid: a6e5a198-1478-4256-a4f2-b9ae6db6d7fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2b05d7bc31afc52c664217ff21d14b40fd0c27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340284"
---
# <a name="vml-fitshape-attribute"></a>VML-fitshape-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert, ob der Text dem umgebenden Feld einer Form entspricht. Lese-/Schreibzugriff. **Vgder State**.

**Gilt für**

[TextPath](msdn-online-vml-textpath-element.md)

**Tagsyntax**

<v: *Element* fitshape = " *Ausdruck* " >

**Skript Syntax**

*Element* . fitshape = "*Ausdruck*"

*Ausdruck* = *Element*. fitshape

**Anmerkungen**

Wenn **true**, wird der Text auf die Ränder des Felds gestreckt, das die gesamte Form definiert. Der Standardwert ist **False**.

*VML-Standard Attribut*

**Beispiel**

Der Text wird so gestreckt, dass er der Form entspricht.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text" fitshape="True"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 