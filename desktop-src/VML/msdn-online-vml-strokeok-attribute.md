---
title: VML-Attribut "strokeok"
description: VML-Attribut "strokeok"
ms.assetid: f150f87b-1ed9-4c53-bf7f-ebe1e81642fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7a2875e3e6e8374238340ff2a596852e5ebce7c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948951"
---
# <a name="vml-strokeok-attribute"></a>VML-Attribut "strokeok"

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt, ob ein Strich angezeigt wird. Lese-/Schreibzugriff. **Vgder State**.

**Gilt für**

[Pfad](msdn-online-vml-path-element.md)

**Tagsyntax**

<v: *Element* strokeok = " *Expression* " >

**Skript Syntax**

*Element* . strokeok = "*Ausdruck*"

*Ausdruck* = *Element*. strokeok

**Anmerkungen**

Wenn der Wert **false** ist, kann der Pfad nicht gestreichelt werden. Der Standardwert ist **True**. Dieses Attribut überschreibt alle anderen Strich Attribute im Parent-oder **Stroke** -Element.

*VML-Standard Attribut*

**Beispiel**

Der Pfad wird nicht mit Strichen gezeichnet.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id="myPath" strokeok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 