---
title: VML-Fokus Attribut
description: VML-Fokus Attribut
ms.assetid: 9ed52203-4142-47cd-851f-74230aac934d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 062b2900c2f980c9a1433e5e790a34d463def9be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039585"
---
# <a name="vml-focus-attribute"></a>VML-Fokus Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den Mittelpunkt einer linearen Farbverlaufsfüllung. Lese-/Schreibzugriff. **Vgbruchteile**.

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *Element* Fokus = " *Ausdruck* " >

**Skript Syntax**

*Element* . Focus = "*Ausdruck*"

*Ausdruck* = *Element*. Fokus

**Anmerkungen**

Definiert die Startposition der Mitte der Mischung. Die Werte reichen von 100% bis-100%. Der Standardwert ist 0. Ein Wert von 100% (oder-100%) Verschiebt den Fokus so, dass die Richtung der Blend umkehren wird (sodass die **Farbe** und der **color2** umkehren). Mit einem Wert von 50% wird die Mischung geändert, sodass sich die **Farbe** an beiden Enden und der **color2** -Wert in der Mitte befindet. Mit dem Wert-50% wird die Mischung geändert, sodass sich **color2** an beiden Enden und die **Farbe** in der Mitte befindet.

*VML-Standard Attribut*

**Beispiel**

Der Farbverlaufs Fokus der Füllung wird so verschoben, dass Rot (**Farbe**) ein Band in der Mitte der Form ist und dass der obere und untere Rand blau (**color2**) sind.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   method="linear" focus="-50%"/>
   </v:shape>
```



 

 