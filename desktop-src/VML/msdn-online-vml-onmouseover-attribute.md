---
title: VML OnMouseOver-Attribut
description: VML OnMouseOver-Attribut
ms.assetid: 68f0fa7a-0d22-4ede-8404-e007296960e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d2bb65864987988996cfad710360fd908a5248c11857e8df1eb5a941b1b895b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999130"
---
# <a name="vml-onmouseover-attribute"></a>VML OnMouseOver-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Löst ein Mausereignis für eine Form aus. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Formen](shape-element--vml.md)

**Tagsyntax**

<v: *element* onmouseover=" *ausdruck* ">

**Anmerkungen**

Ein "Mouseover"-Ereignis wird generiert, wenn sich der Mauszeiger in der Form befindet. Der Wert wird mithilfe des **Schlüsselworts this** (als Verweis auf das -Objekt) gefolgt von der Objektmodellsyntax generiert. Verwenden Sie beispielsweise Folgendes, um die Füllfarbe in Rot zu ändern:

onmouseover="this.fillcolor='red'"

Beachten Sie die Verwendung von einfachen und doppelten Anführungszeichen, um den Ausdruck festzulegen.

*VML-Standardattribut*

**Beispiel**

Wenn sich der Mauszeiger auf der Form befindet, wird die Füllfarbe von Rot in Grün umgeschaltet.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20"
   onmouseover='this.fillcolor="green"'>
   </v:rect>
```



[OnMouseOver-Attribut – Beispiel.](/previous-versions/bb264088(v=vs.85)) (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 