---
title: VML-ImageAspect-Attribut
description: VML-ImageAspect-Attribut
ms.assetid: 9ae58a76-f097-4feb-9008-ab6212bae8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8f67d715d5cd10d36b4e8e7e32f939aeeef2bbdd894aba9da5a069ef03f0e3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118600353"
---
# <a name="vml-imageaspect-attribute"></a>VML-ImageAspect-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert, wie das Seitenverhältnis des Strichbilds beibehalten wird. Lese-/Schreibzugriff. **Zeichenfolge.**

**Gilt für**

[Takt](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v:

element *imageaspect="-Ausdruck* *">*

**Skriptsyntax**

element *.imageaspect="* expression *"*

*=**expression-Element .imageaspect*

**Anmerkungen**

Mögliche Werte:



| Wert   | BESCHREIBUNG                                |
|---------|--------------------------------------------|
| Ignorieren  | Ignorieren von Aspektproblemen.                      |
| Atleast | Das Image ist mindestens so groß wie **ImageSize.** |
| AtMost  | Image ist nicht größer als **ImageSize.**     |



 

In jedem Fall wird das **ImageSize-Attribut** angepasst, um den Aspekt des Bilds zu erhalten.

*VML-Standardattribut*

**Beispiel**

Das Strichbild ist mindestens so groß wie die Bildgröße.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imageaspect="AtLeast"/>
   </v:shape>
```



 

 