---
title: VML V-Attribut
description: VML V-Attribut
ms.assetid: be55704f-71f3-4c0b-8a1b-d7de5efa85dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 690518e998163f7e47fb326b3037e6a4ec397e8f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101831"
---
# <a name="vml-v-attribute"></a>VML V-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die Befehle, die einen Pfad bilden. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Pfad](msdn-online-vml-path-element.md)

**Tagsyntax**

<v: *Element* v = " *Ausdruck* " >

**Skript Syntax**

*Element* . v = "*Ausdruck*"

*Ausdruck* = *Element*. v

**Anmerkungen**

Überschreibt das **path** -Attribut einer Form. Koordinaten können fest Ziffern, relative Zahlen oder Verweise auf Formeln sein (mit dem Format " @n ", wobei "n" eine Formel Nummer ist, z. b. " @2 " bezieht sich auf die zweite Formel im Formel Array).

*VML-Standard Attribut*

**Beispiel**

Ein Rechteck wird mit dem **V** -Attribut erstellt. Beachten Sie, dass nach dem ersten Satz von durch Trennzeichen getrennten Koordinaten ein Kleinbuchstabe L (**LineTo** -Befehl) verwendet wird.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```





 

 