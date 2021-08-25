---
title: ID-Attribut (VML)
description: ID-Attribut (VML)
ms.assetid: 39575a1c-f8ea-43e0-9ad5-540e9d803748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc0ba0addd2d6af8a8b38af4085c79123d3178a3299269468abd73fff1951d9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007859"
---
# <a name="id-attribute-vml"></a>ID-Attribut (VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Stellt einen eindeutigen Bezeichner für ein Element bereit. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

Alle VML-Elemente.

**Tagsyntax**

<v: *elementname* id=" *idname* ">

**Skriptsyntax**

*elementname* .id =" *idname* "

*expression* = *Elementname*.id

**Anmerkungen**

Verwenden Sie **ID,** um auf ein bestimmtes Element zu verweisen. Nachdem Sie eine Form erstellt und ihr eine ID gegeben haben, können Sie den ID-Namen verwenden, wenn Sie das Element bearbeiten möchten.

**ID** ist erforderlich, um das [ShapeType-Element](msdn-online-vml-shapetype-element.md) zu verwenden.

Wenn VML von Microsoft Office generiert wird und der Form ein Objektmodellname zugewiesen wird, wird **id** auf diesen Namen festgelegt. Wenn der Objektmodellname nicht festgelegt ist, wird der Name mithilfe der *Spid* (interne Form-ID) plus einem Präfix (S für Form, M für Masterform, T für shapetype) generiert.

*VML-Standardattribut*.

**Beispiel**

Um die Attribute einer Form zu ändern, müssen Sie der Form zunächst eine ID geben. Beispiel: "myrect".


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```




```HTML
   myrect.style.width = 80
   myrect.style.height = 80
   myrect.fillColor = "green"
```



[ID-Attribut – Beispiel.](/previous-versions/office/developer/speech-technologies/ms872141(v=msdn.10)#example) (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 