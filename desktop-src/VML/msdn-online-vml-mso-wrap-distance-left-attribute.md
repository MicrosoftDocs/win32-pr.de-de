---
title: VML-Attribut "mso-Wrap-Distance-Left"
description: VML-Attribut "mso-Wrap-Distance-Left"
ms.assetid: 25dcb5d0-a839-4a4b-8969-8e5dcf1baa47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d1e47fff0f9dceff5fd98ad526208bf487d851
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315429"
---
# <a name="vml-mso-wrap-distance-left-attribute"></a>VML-Attribut "mso-Wrap-Distance-Left"

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den Abstand zwischen der linken Seite der Form und dem Text, der diese umschließt. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* Style = "mso-Wrap-Distance-left: *Expression* " >

**Anmerkungen**

Beachten Sie, dass sich dieses Attribut vom CSS **Margin** -Attribut unterscheidet. Der **Rand** ändert den Ursprung der Form, sodass er die Randbereiche einschließt, aber der Umbruch Abstand in Microsoft Office ändert nicht den Ursprung der Form.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Die Form hat einen linken Umbruch Abstand von 10 Punkten.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-left:10pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 