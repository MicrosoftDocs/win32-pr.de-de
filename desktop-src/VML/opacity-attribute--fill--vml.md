---
title: Opacity-Attribut (Fill) (VML)
description: Opacity-Attribut (Fill) (VML)
ms.assetid: abd2fe4d-6391-4413-80f0-549bcc74f42e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b913498705e65fa7211db4b4cef039894d573a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730136"
---
# <a name="opacity-attribute-fillvml"></a>Opacity-Attribut (Fill) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die Transparenz einer Füllung. Lese-/Schreibzugriff. [Vgbruchteile](msdn-online-vml-vgfraction-data-type.md).

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *Element* Deckkraft = " *Ausdruck* " >

**Skript Syntax**

*Element* . Opacity = "*Ausdruck*"

*Ausdruck* = *Element*. Deckkraft

**Anmerkungen**

Der Standardwert ist 1,0.

*VML-Standard Attribut*

**Beispiel**

Die Füllung der Form ist 50% transparent.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill opacity="50%" color="red"/>
   </v:shape>
```



 

 