---
title: VML-alt-Attribut
description: VML-alt-Attribut
ms.assetid: 6b7e778c-d8e2-432e-b69a-5d80fa62d105
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b420d556e69ed2f987a3a3b10a5709f926dc5c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209337"
---
# <a name="vml-alt-attribute"></a>VML-alt-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert alternativen Text, der anstelle einer Grafik angezeigt werden soll. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* alt = " *Ausdruck* " >

**Skript Syntax**

*Element* . alt = "*Ausdruck*"

*Ausdruck* = *Element*. alt

**Anmerkungen**

Das **alt** -Attribut ähnelt dem standardmäßigen HTML- **alt** -Attribut. Dieses Attribut bietet eine Möglichkeit für Browser, die Text in Sprache konvertieren, um grafische Elemente auf einer Seite zu beschreiben.

*VML-Standard Attribut*

**Siehe auch**

[Form](shape-element--vml.md)

**Beispiel**

Das **alt** -Element unten zeigt den Ausdruck "rotes Rechteck" in Browsern an, in denen Webseiten in gesprochene Ausdrücke konvertiert werden.


```HTML
   <v:rect id=myrect fillcolor="red" alt="Red rectangle"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Beispiel](/previous-versions/bb229663(v=vs.85))für ein alt-Attribut. (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 