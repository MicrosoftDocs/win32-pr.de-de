---
title: VML-Attribut "mso-Wrap-Distance-right"
description: VML-Attribut "mso-Wrap-Distance-right"
ms.assetid: 2f0ec7a3-036e-4f45-a330-f8ddccb75791
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf38fc62812b0ce300e4d18067a0f2497233f2e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858324"
---
# <a name="vml-mso-wrap-distance-right-attribute"></a>VML-Attribut "mso-Wrap-Distance-right"

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den Abstand zwischen dem rechten Rand der Form und dem Text, der diese umschließt. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* Style = "mso-Wrap-Distance-right: *Expression* " >

**Anmerkungen**

Beachten Sie, dass sich dieses Attribut vom CSS **Margin** -Attribut unterscheidet. Der **Rand** ändert den Ursprung der Form, sodass er die Randbereiche einschließt, aber der Umbruch Abstand in Microsoft Office ändert nicht den Ursprung der Form.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Die Form hat einen rechten Umbruch Abstand von 10 Punkten.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-right:10pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 