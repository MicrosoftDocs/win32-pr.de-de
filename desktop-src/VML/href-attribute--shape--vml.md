---
title: HRef-Attribut (Form)(VML)
description: HRef-Attribut (Form)(VML)
ms.assetid: c44b3099-df3f-42e5-ad0c-10400630e884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe4b545aa27d311b0e1d0c73f0107aa6fdb357d524d3150ce6ab7dfb1e0f009
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072040"
---
# <a name="href-attribute-shapevml"></a>HRef-Attribut (Form)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert eine URL für eine Form. Wenn auf die Form geklickt wird, wird die URL vom Browser geladen. Lese-/Schreibzugriff. **Zeichenfolge.**

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *element* href="-Ausdruck "> 

**Skriptsyntax**

*element* .href="*expression*"

*expression* = *Element*.href

**Anmerkungen**

Das **HRef-Attribut** ähnelt dem HTML **HRef-Standardattribut** von Ankern.

Die **Verwendung von HRef** erleichtert das Erstellen interessanter Schaltflächen auf einer Webseite.

*VML-Standardattribut*

**Beispiel**

Wenn auf das Rechteck geklickt wird, wird die Startseite Microsoft Corporation Browser geladen.


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
   
```



[HRef-Attribut – Beispiel.](/previous-versions/bb229672(v=vs.85)) (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 