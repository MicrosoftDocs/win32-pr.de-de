---
title: VML-Metal-Attribut
description: VML-Metal-Attribut
ms.assetid: 4d2efaed-d391-494f-9f0c-d57ad019f71d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d318724f0a8f3c5fbce1ee9045ed5d6e0d49686
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390356"
---
# <a name="vml-metal-attribute"></a>VML-Metal-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt, ob die Oberfläche der extrudierten Form Metal ähnelt. Lese-/Schreibzugriff. **Vgder State**.

**Gilt für**

[Schläuche](msdn-online-vml-extrusion-element.md)

**Tagsyntax**

<o: *Element* Metal = " *Expression* " >

**Skript Syntax**

*Element* . Metal = "*Ausdruck*"

*Ausdruck* = *Element*. Metal

**Anmerkungen**

Wenn diese Eigenschaft auf " **true**" festgelegt ist, bewirkt dieses Attribut, dass das für die Legende reflektierte Licht die Material Farbe anstelle der hellen Quellfarbe ist, sodass das Objekt mehr Metallic erscheint. Zur weiteren Näherung eines metallischen Materials ist es erforderlich, dass die Spekulation relativ hoch (etwa 1,2) und diffusity relativ niedrig (etwa 0,6) ist. Der Standardwert ist **False**.

*Microsoft Office Extensions-Attribut*

 

 