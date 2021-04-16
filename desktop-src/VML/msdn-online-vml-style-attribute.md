---
title: VML-Format Attribut
description: VML-Format Attribut
ms.assetid: 1695d2b2-cf60-48f1-b47e-f0f43696b5b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f291fad75bf14e06f40ad0a1446bd0418bba46b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473205"
---
# <a name="vml-style-attribute"></a>VML-Format Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den Stil des Frames. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Vmlframe](msdn-online-vml-vmlframe-element.md)

**Tagsyntax**

<v: *Element* Style = " *Expression* " >

**Skript Syntax**

*Element* . Style = "*Ausdruck*"

*Ausdruck* = *Element*. Style

**Anmerkungen**

Dieses Attribut verwendet die normalen CSS-Stil Attribute für die Positionierung.

*VML-Standard Attribut*

**Beispiel**

Der Stil definiert die tatsächliche Position des Frames.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 