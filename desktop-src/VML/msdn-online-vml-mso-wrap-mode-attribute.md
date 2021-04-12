---
title: VML mso-Wrap-Mode-Attribut
description: VML mso-Wrap-Mode-Attribut
ms.assetid: 51c4e90d-62cc-4646-9c71-8a6bf3366b2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5657192fcf9da72ff99dc25cff7930b6d2d9b6b9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315597"
---
# <a name="vml-mso-wrap-mode-attribute"></a>VML mso-Wrap-Mode-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den Wrapping Modus für Text. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* Style = "mso-Wrap-Mode: *Expression* " >

**Anmerkungen**

Mögliche Werte:



| Wert          | BESCHREIBUNG                          |
|----------------|--------------------------------------|
| square         | Umschließt Text um Form in einem Quadrat. |
| knapper          | Text wird in der Nähe der Form umschließt.  |
| oben und unten | Der Text springt von oben nach unten.       |
| bis        | Text wird durch die Form angezeigt.     |
| none           | Der Text wird nicht eingeschlossen.                   |



 

Wird von Microsoft PowerPoint zum Speichern in HTML verwendet, um anzugeben, ob der Zeilenumbruch innerhalb einer AutoForm ein (**quadratisch**) oder Off (**None**) ist.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Der folgende Code gibt an, dass WordWrap innerhalb einer AutoShape in PowerPoint aktiviert ist.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-mode:square"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 