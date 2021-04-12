---
title: VML-arrowok-Attribut
description: VML-arrowok-Attribut
ms.assetid: 19b23544-4a72-4273-b48a-6aee39addcf6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8807b802370f81ddd084df8a171f95e8496c7ff0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390545"
---
# <a name="vml-arrowok-attribute"></a>VML-arrowok-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt, ob Pfeilspitzen angezeigt werden. Lese-/Schreibzugriff. **Vgder State**.

**Gilt für**

[Pfad](msdn-online-vml-path-element.md)

**Tagsyntax**

<v: *Element* arrowok = " *Expression* " >

**Skript Syntax**

*Element* . arrowok = "*Ausdruck*"

*Ausdruck* = *Element*. arrowok

**Anmerkungen**

Wenn der Wert **false** ist, weist der Pfad keine Pfeilspitzen auf. Der Standardwert ist **False**. Dieses Attribut überschreibt alle anderen Pfeilspitze-Attribute im Parent-oder **Stroke** -Element.

*VML-Standard Attribut*

**Beispiel**

Der Pfad weist keine Pfeilspitze auf.


```HTML
   <v:line id="whatsmyline"
   style="position:relative"
   from="114pt,66pt" to="402pt,66pt"
   strokecolor="black">
   <v:stroke startarrow="block" endarrow="block"/>
   <v:path arrowok="False"/>
   </v:line>
```



 

 