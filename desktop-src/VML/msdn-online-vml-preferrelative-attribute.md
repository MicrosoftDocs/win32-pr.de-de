---
title: VML PreferRelative-Attribut
description: VML PreferRelative-Attribut
ms.assetid: 7de616e8-4fc3-4bcb-8e5e-ea153d6d4b54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 154297a528f18a3ac53f788ebbfe80ff59196f2872dd3dcb3789db16d5c91cb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654980"
---
# <a name="vml-preferrelative-attribute"></a>VML PreferRelative-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, ob die ursprüngliche Größe eines Objekts nach dem Neuformatieren gespeichert wird. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *element* o:preferrelative=" *expression* ">

**Anmerkungen**

Der Standardwert ist **False**. **True** gibt an, dass die ursprüngliche Größe des Objekts gespeichert wird, und die Größenänderung basiert auf einem Prozentsatz dieser ursprünglichen Größe. Andernfalls wird bei jeder Größenänderung die Skalierung auf 100 % zurückgesetzt.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Wenn die Größe der Form geändert wird, wird die ursprüngliche Größe nicht gespeichert.


```HTML
   <v:rect id=myrect fillcolor="red" preferrelative="False"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 