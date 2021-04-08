---
title: VML LineStyle-Attribut
description: VML LineStyle-Attribut
ms.assetid: eec5c1f3-5256-4104-b021-ebf799665752
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4e69371e61a3d81f97de0243af19381f36c0555
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727425"
---
# <a name="vml-linestyle-attribute"></a>VML LineStyle-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die Linienart des Strichs. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Stellung](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v: *Element* LineStyle = " *Expression* " >

**Skript Syntax**

*Element* . LineStyle = "*Ausdruck*"

*Ausdruck* = *Element*. LineStyle

**Anmerkungen**

Mögliche Werte:

-   Single (Standard)
-   Dünn
-   Dünn
-   Dickes dünn
-   Thickbetweenthin

*VML-Standard Attribut*

**Beispiel**

Eine doppelte Linie wird mit zwei schmalen Strichen gezeichnet.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke linestyle="thinthin" />
   </v:line>
```



 

 