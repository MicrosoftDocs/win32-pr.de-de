---
title: VML MSO-Wrap-Distance-Top-Attribut
description: VML MSO-Wrap-Distance-Top-Attribut
ms.assetid: 20444d16-fa84-4685-911c-288150c2674b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 856082665ab1b46b9d9294bffdd2821e2fb5db4b6e066effef5dd2f081185f38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124290"
---
# <a name="vml-mso-wrap-distance-top-attribute"></a>VML MSO-Wrap-Distance-Top-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert den Abstand von der Form oben zu dem Text, der ihn umschließt. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *element* style="mso-wrap-distance-top: *expression* ">

**Anmerkungen**

Beachten Sie, dass sich dieses Attribut vom CSS **Margin-Attribut** unterscheidet. **Margin** ändert den Ursprung der Form, um die Randbereiche einzuschließen, aber der Umbruchabstand in Microsoft Office ändert nicht den Ursprung der Form.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Die Form hat einen oberen Umbruchabstand von 10 Punkten.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 