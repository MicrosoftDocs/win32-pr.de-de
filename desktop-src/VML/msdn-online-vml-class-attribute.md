---
title: VML-Klassen Attribut
description: VML-Klassen Attribut
ms.assetid: 4030b8b7-fcc9-4153-8004-81935a347a09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94bdc723ba9be335afc43023ab89b88834c55474
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948905"
---
# <a name="vml-class-attribute"></a>VML-Klassen Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Verweist auf eine Definition eines CSS-Stils. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* Class = " *Expression* " >

**Skript Syntax**

*Element* . ClassName = "*Ausdruck*"

*Ausdruck* = *Element*. ClassName

**Anmerkungen**

Das **Class** -Attribut ähnelt dem Standard-HTML- **Klassen** Attribut, das mit CSS-Stylesheets verwendet wird.

Beachten Sie, dass **className** anstelle der- **Klasse** für die Skripterstellung verwendet wird. Beachten Sie außerdem, dass für die Skripterstellung nur der **Klassenname** gelesen werden kann. Wenn Sie den Wert von **className** ändern, wird das Rendering der Form nicht geändert.

*VML-Standard Attribut*

**Siehe auch**

[Form](shape-element--vml.md)

**Beispiel**

Eine Klasse für die **Breite** wird mit dem Stil erstellt.


```HTML
   .narrowstyle {width:50;height:100}
```



Dann wird auf die Breite durch Einschließen des Stils verwiesen. Beachten Sie, dass die Width-und Height-Eigenschaft nicht im **Style** -Attribut definiert ist, sondern durch den-Stil definiert wird.


```HTML
   <v:shape id="rect01" class="narrowstyle"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



Beachten Sie, dass die **Klasse** nur auf CSS-Type-Attribute angewendet wird.

 

 