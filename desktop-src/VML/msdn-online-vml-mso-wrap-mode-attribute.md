---
title: VML-MSO-Wrap-Mode-Attribut
description: VML-MSO-Wrap-Mode-Attribut
ms.assetid: 51c4e90d-62cc-4646-9c71-8a6bf3366b2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88e3743522b9286da8a7f30e9100e06205430b1b18fa3c62def60b57f54b65d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136983"
---
# <a name="vml-mso-wrap-mode-attribute"></a>VML-MSO-Wrap-Mode-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert den Umbruchmodus für Text. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Formen](shape-element--vml.md)

**Tagsyntax**

<v: *element* style="mso-wrap-mode: *expression* ">

**Anmerkungen**

Mögliche Werte:



| Wert          | Beschreibung                          |
|----------------|--------------------------------------|
| square         | Umschließt Text um Form in einem Quadrat. |
| Engen          | Text wird in der Nähe der Form umschlossen.  |
| oben und unten | Text springt von oben nach unten.       |
| bis        | Text wird durch die Form angezeigt.     |
| Keine           | Text wird nicht umbrochen.                   |



 

Wird von Microsoft PowerPoint zum Speichern in HTML verwendet, um anzugeben, ob der Zeilenumbruch innerhalb einer AutoShape auf **(quadratisch)** oder deaktiviert **(keine)** ist.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Der folgende Code gibt an, dass wordwrap innerhalb einer AutoShape in PowerPoint aktiviert ist.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-mode:square"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 