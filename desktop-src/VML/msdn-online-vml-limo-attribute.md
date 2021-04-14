---
title: VML Limo-Attribut
description: VML Limo-Attribut
ms.assetid: 61919d48-0cc8-4693-a8bb-a8a4498ef840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a364aebfc2384ac9e19c9dc5f2f0ae52f09228a8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390380"
---
# <a name="vml-limo-attribute"></a>VML Limo-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert einen streckungs Punkt auf dem Pfad. Lese-/Schreibzugriff. **Vector2D**.

**Gilt für**

[Pfad](msdn-online-vml-path-element.md)

**Tagsyntax**

<v: *Element* Limo = " *Ausdruck* " >

**Skript Syntax**

*Element* . Limo = "*Ausdruck*"

*Ausdruck* = *Element*. Limo

**Anmerkungen**

Der Standardwert ist "0 0". Limo-Strecken sind Punkte auf dem Edge einer Form, die definieren, wo und wie eine Form von einem Benutzer in einem grafischen Editor gestreckt werden kann.

*VML-Standard Attribut*

**Beispiel**

Ein Limo-streckungs Punkt wird in der Mitte entlang der horizontalen Linie definiert.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" from="20pt,20pt" to="100pt,20pt">
   <v:path limo="60pt,20pt"/>
   </v:line>
```



 

 