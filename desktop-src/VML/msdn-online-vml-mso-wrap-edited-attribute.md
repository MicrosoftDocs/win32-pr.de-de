---
title: VML-Attribut "mso-Wrap-bearbeitet"
description: VML-Attribut "mso-Wrap-bearbeitet"
ms.assetid: cb0e8618-e649-4a3c-9433-2be77c4b65f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a272a56b57d82ca0fee9f69fbde2757316439fd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340719"
---
# <a name="vml-mso-wrap-edited-attribute"></a>VML-Attribut "mso-Wrap-bearbeitet"

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt, ob die Wrap-Koordinaten vom Benutzer angepasst wurden. Lese-/Schreibzugriff. **Vgder State**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* Style = "mso-Wrap-bearbeitet: *Expression* " >

**Anmerkungen**

Wenn die Wrap-Koordinaten von einem Editor generiert werden, ist dieses Attribut **true**. Andernfalls wurden Sie von einem Benutzer angepasst.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Die Wrap-Koordinaten der Form wurden von einem Form-Editor generiert.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-edited:True"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 