---
title: Href-Attribut (Form) (VML)
description: Href-Attribut (Form) (VML)
ms.assetid: c44b3099-df3f-42e5-ad0c-10400630e884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ecbc0f97ca2fb9c1565b712d3677d007a62b035
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039516"
---
# <a name="href-attribute-shapevml"></a>Href-Attribut (Form) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert eine URL für eine Form. Beim Klicken auf die Form wird die URL vom Browser geladen. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* href = " *Expression* " >

**Skript Syntax**

*Element* . href = "*Ausdruck*"

*Ausdruck* = *Element*. href

**Anmerkungen**

Das **href** -Attribut ähnelt dem standardmäßigen HTML- **href** -Attribut von Ankern.

Die Verwendung von **href** erleichtert das Erstellen interessanter Schaltflächen auf einer Webseite.

*VML-Standard Attribut*

**Beispiel**

Beim Klicken auf das Rechteck lädt der Browser die Microsoft Corporation-Startseite.


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
   
```



[Href-Attribut Beispiel](/previous-versions/bb229672(v=vs.85)). (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 