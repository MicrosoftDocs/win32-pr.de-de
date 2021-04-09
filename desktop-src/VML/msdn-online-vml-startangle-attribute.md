---
title: VML-startAngle-Attribut
description: VML-startAngle-Attribut
ms.assetid: 334ae52a-cde4-427e-8080-ec789b4d9d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e779d343061ef65decb1dd21f615e054d561da28
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039235"
---
# <a name="vml-startangle-attribute"></a>VML-startAngle-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den Anfangspunkt des Bogens. Lese-/Schreibzugriff. [Vganglin Grad](msdn-online-vml-vgangleindegrees-data-type.md) .

**Gilt für**

[Arc](msdn-online-vml-arc-element.md)

**Tagsyntax**

<v: *Element* EndAngle = " *Expression* " >

**Skript Syntax**

*Element* . EndAngle = "*Ausdruck*"

*Ausdruck* = *Element*. EndAngle

**Anmerkungen**

Der Bogen wird als ein durch ein Oval gezeichneter Strich definiert, der durch die **Stil** Attribute einer Form begrenzt ist. Der Anfang des Strichs wird durch einen Winkel definiert, der von der geraden im Uhrzeigersinn (12 Uhr) gemessen wird. Der Standardwert ist 0 Grad.

VML-Standard Attribut

**Beispiel**

Der Bogen ist Lächeln. Der Startpunkt befindet sich am 90-Grad-Punkt eines Oval, das innerhalb des umgebenden Felds der Form verankert ist. Der Endpunkt befindet sich am 270-Grad-Punkt der Oval.


```HTML
   <v:arc id="myarc"
   style="position:relative;top:10;left:10;width:200;height:200"
   startangle="90" endangle="270">
   </v:arc>
```



 

 