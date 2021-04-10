---
title: VML-Attribut "fillok"
description: VML-Attribut "fillok"
ms.assetid: 6855544d-0f12-4e21-8101-1bbf45795777
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 667524be103b7c641643a52a85368a82a1289e5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316412"
---
# <a name="vml-fillok-attribute"></a>VML-Attribut "fillok"

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt, ob eine Füllung angezeigt wird. Lese-/Schreibzugriff. **Vgder State**.

**Gilt für**

[Pfad](msdn-online-vml-path-element.md)

**Tagsyntax**

<v: *Element* fillok = " *Expression* " >

**Skript Syntax**

*Element* . fillok = "*Ausdruck*"

*Ausdruck* = *Element*. fillok

**Anmerkungen**

**False** gibt an, dass der Pfad nicht ausgefüllt werden kann. Der Standardwert ist **True**. Dieses Attribut überschreibt alle anderen Füll Attribute im übergeordneten Element oder im **Fill** -Element.

*VML-Standard Attribut*

**Beispiel**

Der Pfad wird nicht ausgefüllt.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id="myPath" fillok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 