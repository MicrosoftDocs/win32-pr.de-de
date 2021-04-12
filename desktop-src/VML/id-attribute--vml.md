---
title: ID-Attribut (VML)
description: ID-Attribut (VML)
ms.assetid: 39575a1c-f8ea-43e0-9ad5-540e9d803748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a3925166a735b7813efd4cb9bc68f50bb8fa52
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473477"
---
# <a name="id-attribute-vml"></a>ID-Attribut (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Stellt einen eindeutigen Bezeichner für ein Element bereit. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

Alle VML-Elemente.

**Tagsyntax**

<v: *ElementName* ID = " *IDName* " >

**Skript Syntax**

*ElementName* . ID = " *IDName* "

*Ausdruck* = *ElementName*. ID

**Anmerkungen**

Verwenden Sie **ID** , um auf ein bestimmtes Element zu verweisen. Nachdem Sie eine Form erstellt und eine ID angegeben haben, können Sie den ID-Namen verwenden, wenn Sie das Element bearbeiten möchten.

**ID** ist erforderlich, um das [ShapeType](msdn-online-vml-shapetype-element.md) -Element zu verwenden.

Wenn VML durch Microsoft Office generiert wird, wird die **ID** auf diesen Namen festgelegt, wenn der Form ein Objektmodell Name zugewiesen ist. Wenn der Objektmodell Name nicht festgelegt ist, wird der Name mit der *SPID* (Internal Shape ID) und einem Präfix (en für Shape, M für die Master-Form, T für ShapeType) generiert.

*VML-Standard Attribut*.

**Beispiel**

Um die Attribute einer Form zu ändern, müssen Sie der Form zuerst eine ID zuordnen. Beispiel: "myRect".


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



[ID-Attribut Beispiel](/previous-versions/office/developer/speech-technologies/ms872141(v=msdn.10)#example). (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 