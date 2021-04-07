---
title: Origin-Attribut (vmlframe) (VML)
description: Origin-Attribut (vmlframe) (VML)
ms.assetid: 317c027e-5054-4543-ad98-2c21d1cf7154
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9341eecea9ec1eae8aaf1d7b1ad729986a8249
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729992"
---
# <a name="origin-attribute-vmlframevml"></a>Origin-Attribut (vmlframe) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den Ursprung des Clippingbereichs des Frames. Lese-/Schreibzugriff. **VgVector2D**.

**Gilt für**

[Vmlframe](msdn-online-vml-vmlframe-element.md)

**Tagsyntax**

<v: *Element* Origin = " *Expression* " >

**Skript Syntax**

*Element* . Origin = "*Ausdruck*"

*Ausdruck* = *Element*. Origin

**Anmerkungen**

Der Standardwert ist 0,0. Beachten Sie, dass **Origin** nur funktioniert, wenn [Clip](msdn-online-vml-clip-attribute.md) den Wert **true** hat. In diesem Attribut wird der Ursprung als die linke obere Ecke des Frames definiert.

*VML-Standard Attribut*

**Beispiel**

Der Ursprung des Clippingbereichs beträgt 100 PT, 100 PT.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'
   </v:vmlframe>
```



 

 