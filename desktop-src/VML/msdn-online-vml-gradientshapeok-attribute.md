---
title: VML gradientshapeok-Attribut
description: VML gradientshapeok-Attribut
ms.assetid: c26ac4cb-f7f0-4666-b32f-d9fcaf9044a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d1b7c215fbe0b98c11f7e4d33301e81798bd37f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390921"
---
# <a name="vml-gradientshapeok-attribute"></a>VML gradientshapeok-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt, ob ein Farbverlaufs Pfad aus wiederholten konzentrischen Pfaden besteht. Lese-/Schreibzugriff. **Vgder State**.

**Gilt für**

[Pfad](msdn-online-vml-path-element.md)

**Tagsyntax**

<v: *Element* gradientshapeok = " *Ausdruck* " >

**Skript Syntax**

*Element* . gradientshapeok = "*Ausdruck*"

*Ausdruck* = *Element*. gradientshapeok

**Anmerkungen**

**True** gibt an, dass der Pfad mit einer konzentrischen Farbverlaufsfüllung gefüllt wird, wobei der Pfad als wiederholte Form des Farbverlaufs verwendet wird. Der Standardwert ist **false**.

*VML-Standard Attribut*

**Beispiel**

Der Pfad wird mit einer konzentrischen Verlaufs Füllung aufgefüllt, die aus wiederholten Rechtecke besteht.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:path gradientshapeok="True"/>
   </v:shape>
```



 

 