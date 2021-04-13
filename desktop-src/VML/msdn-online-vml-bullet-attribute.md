---
title: VML-Aufzählungs Attribut
description: VML-Aufzählungs Attribut
ms.assetid: 17c24b97-191b-4170-8a2d-9284f500e728
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edcf1194a234284a70f928adad198ca77f597a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390539"
---
# <a name="vml-bullet-attribute"></a>VML-Aufzählungs Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt, ob eine Form eine grafische Kugel ist. **VGZ"** lesen/schreiben".

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* o:Bullet = " *Ausdruck* " >

**Anmerkungen**

Der Standardwert ist **False**. **True** gibt an, dass die Form eine grafische Kugel ist.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Die Form ist ein Aufzählungs Zeichen.


```HTML
   <v:rect id=myrect fillcolor="red" o:bullet="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 