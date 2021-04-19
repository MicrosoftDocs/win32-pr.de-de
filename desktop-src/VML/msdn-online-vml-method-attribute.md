---
title: VML-Methoden Attribut
description: VML-Methoden Attribut
ms.assetid: 42ab9d78-f004-4571-a566-03edd8341d19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2f7440e1e793e7ad34860524f63a3bfc38456f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339896"
---
# <a name="vml-method-attribute"></a>VML-Methoden Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die Methode, die zum Generieren einer Farbverlaufsfüllung verwendet wird. Lese-/Schreibzugriff. **Vgsigmatype**.

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *Element* Method = " *Expression* " >

**Skript Syntax**

*Element* . Method = "*Ausdruck*"

*Ausdruck* = *Element*. Method

**Anmerkungen**

Mögliche Werte:



| Wert  | BESCHREIBUNG          |
|--------|----------------------|
| Keine   | Keine Sigma-Füllung.       |
| Linear | Lineare Sigma-Füllung.   |
| Sigma  | Sigma-Füllung. Standard. |
| Any    | Eine beliebige Sigma-Füllung.      |



 

*VML-Standard Attribut*

**Beispiel**

Die Form hat eine rote lineare Farbverlaufsfüllung.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" type="gradient" method="linear"/>
   </v:shape>
```



 

 