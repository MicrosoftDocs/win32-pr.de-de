---
title: VML JOINSTYLE-Attribut
description: VML JOINSTYLE-Attribut
ms.assetid: d947d115-2064-446a-8c12-e8063fe10953
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657d3c815d6165cecd853f394780237ad0b89f0d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338670"
---
# <a name="vml-joinstyle-attribute"></a>VML JOINSTYLE-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die joinart einer Polylinie. Lese-/Schreibzugriff. Eine Zeichenfolge.

**Gilt für**

[Stellung](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v: *Element* JOINSTYLE = " *Expression* " >

**Skript Syntax**

*Element* . JOINSTYLE = "*Ausdruck*"

*Ausdruck* = *Element*. JOINSTYLE

**Anmerkungen**

Mögliche Werte:

-   Round (Standard)
-   Abschrägung
-   Gehrungs

*VML-Standard Attribut*

**Beispiel**

Die Gelenke auf der Polylinie werden gevelht.


```HTML
   <v:polyline
   strokecolor="red" strokeweight="2pt"
   points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt">
   <v:stroke joinstyle="bevel"/>
   </v:polyline>
```



 

 