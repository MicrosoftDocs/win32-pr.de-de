---
title: VML-Attribut "mso-Wrap-Distance-Top"
description: VML-Attribut "mso-Wrap-Distance-Top"
ms.assetid: 20444d16-fa84-4685-911c-288150c2674b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a16898733ead7bf3728d8f520888c8a05ef5fe6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340505"
---
# <a name="vml-mso-wrap-distance-top-attribute"></a>VML-Attribut "mso-Wrap-Distance-Top"

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den Abstand zwischen der Form und dem Text, der diese umschließt. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* Style = "mso-Wrap-Distance-Top: *Expression* " >

**Anmerkungen**

Beachten Sie, dass sich dieses Attribut vom CSS **Margin** -Attribut unterscheidet. Der **Rand** ändert den Ursprung der Form, sodass er die Randbereiche einschließt, aber der Umbruch Abstand in Microsoft Office ändert nicht den Ursprung der Form.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Die Form weist einen oberen Umschlag Abstand von 10 Punkten auf.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 