---
title: VML-EndCap-Attribut
description: VML-EndCap-Attribut
ms.assetid: d8669a34-0fec-461e-90de-d9d5f7749a15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 726d2bba2128ebb1897f306ae608f4bebb48d63f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316418"
---
# <a name="vml-endcap-attribute"></a>VML-EndCap-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den Stil für das Ende eines Strichs. Lese-/Schreibzugriff. **Vglineendcapstyle**.

**Gilt für**

[Stellung](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v: *Element* EndCap = " *Ausdruck* " >

**Skript Syntax**

*Element* . EndCap = "*Ausdruck*"

*Ausdruck* = *Element*. EndCap

**Anmerkungen**

Mögliche Werte:

-   Flat (Standard)
-   Square
-   Round

*VML-Standard Attribut*

**Beispiel**

Eine Linie wird mit einer flachen Obergrenze am Ende des Strichs gezeichnet.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endcap="flat"/>
   </v:line>
```



 

 