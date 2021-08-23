---
title: VML V-Text-Anchor-Attribut
description: VML V-Text-Anchor-Attribut
ms.assetid: d6e2f60c-5cc7-4340-a9cd-b6c2b0b5b0be
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7c4b355aa4e56e3b0320200a092a66aa1f504b16be02f697e1335cd295627c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057698"
---
# <a name="vml-v-text-anchor-attribute"></a>VML V-Text-Anchor-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die vertikale Verankerung von Text in einem Textfeld. Lese-/Schreibzugriff. **Zeichenfolge.**

**Gilt für**

[TextBox](msdn-online-vml-textbox-element.md)

**Tagsyntax**

<v: *element* v-text-anchor="-Ausdruck "> 

**Anmerkungen**

Mögliche Werte:

-   **top** (Standard)
-   **Mitte**
-   **Unteres**
-   **top-center**
-   **Mittlere Mitte**
-   **Unten zentriert**
-   **Top-Baseline**
-   **Bottom-Baseline**
-   **Top-Center-Baseline**
-   **Bottom-Center-Baseline**

Der Text wird an einer vertikalen Position im Textfeld verankert, wie durch den Attributwert angegeben. Die Ausrichtung eines Textankers wird nur deutlich, wenn [MSO-Fit-Text-To-Shape](msdn-online-vml-mso-fit-text-to-shape-attribute.md) auf **False festgelegt ist.** Dieses Attribut ist anders als das **Attribut "Vertical-Align** Style", das für ideografische Sprachen verwendet wird.

Dieses Attribut wird von Microsoft Office zum Speichern von Daten in Webdokumenten verwendet, wird jedoch nicht in Microsoft Internet Explorer 5 oder höher gerendert.

*VML-Standardattribut*

**Beispiel**

Der Text wird am unteren Rand des Textfelds ausgerichtet.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox style="v-text-anchor:bottom" id="mytextbox">
   VML
   </v:textbox/>
   </v:shape>
```



 

 