---
title: Opacity-Attribut (Strich) (VML)
description: Opacity-Attribut (Strich) (VML)
ms.assetid: 8f1968ba-0d0b-4cd6-9332-74755e891783
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cc97f445ede54676d73e95a60ec039ab214f4a5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474157"
---
# <a name="opacity-attribute-strokevml"></a>Opacity-Attribut (Strich) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den Umfang der Transparenz eines Strichs. Lese-/Schreibzugriff. **Vgbruchteile**.

**Gilt für**

[Stellung](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v: *Element* Deckkraft = " *Ausdruck* " >

**Skript Syntax**

*Element* . Opacity = "*Ausdruck*"

*Ausdruck* = *Element*. Deckkraft

**Anmerkungen**

Der Standardwert ist 1,0.

*VML-Standard Attribut*

**Beispiel**

Der Strich ist 50% transparent.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke opacity="50%"/>
   </v:shape>
```



 

 