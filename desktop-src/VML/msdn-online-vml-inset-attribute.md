---
title: VML-INSET-Attribut
description: VML-INSET-Attribut
ms.assetid: b50f900a-b0dc-4042-af9e-050011307765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83f2ea38ef4ca90f6687196335d2edd2d39c09c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101795"
---
# <a name="vml-inset-attribute"></a>VML-INSET-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Gibt die inneren Rand Werte für Text Feld Text an. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[TextBox](msdn-online-vml-textbox-element.md)

**Tagsyntax**

<v: *Element* INSET = " *Expression* " >

**Skript Syntax**

*Element* . Inset = "*Ausdruck*"

*Ausdruck* = *Element*. Inset

**Anmerkungen**

Der Wert für den internen Textrand wird als Zeichenfolge angegeben, die vier Werte enthält, die jeweils durch Kommas oder Leerzeichen voneinander getrennt sind. Die Werte werden vom linken, oberen, rechten und unteren Rand des Felds festgelegt, das durch das [textboxrect](msdn-online-vml-textboxrect-attribute.md) -Attribut von **path** angegeben wird. Fehlende Werte werden auf den Standardwert festgelegt, der "0,1 in, 0,05 in, 0,1 in, 0,05 in" ist.

Für gedrehte Formen in Browsern, die keine Rotation unterstützen, wird das umgebende Feld am nächstgelegenen Vielfachen von 90 Grad ausgerichtet.

*VML-Standard Attribut*

**Beispiel**

Das Textfeld enthält einen einsetenrand von 10 Pixeln.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox id="mytextbox" inset="10px, 10px, 10px, 10px">
   VML
   </v:textbox/>
   </v:shape>
```



 

 