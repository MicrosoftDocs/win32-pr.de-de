---
title: VML-V-Text-Anker-Attribut
description: VML-V-Text-Anker-Attribut
ms.assetid: d6e2f60c-5cc7-4340-a9cd-b6c2b0b5b0be
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 603f118a260c8ce9c271128fa642e9e2ae569806
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390668"
---
# <a name="vml-v-text-anchor-attribute"></a>VML-V-Text-Anker-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert das vertikale Verankern von Text in einem Textfeld. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[TextBox](msdn-online-vml-textbox-element.md)

**Tagsyntax**

<v: *Element* v-Text-Anchor = " *Expression* " >

**Anmerkungen**

Mögliche Werte:

-   **Top** (Standard)
-   **Naher**
-   **unten**
-   **Top-Center**
-   **mittlere Mitte**
-   **unten zentriert**
-   **Top-Baseline**
-   **untere Baseline**
-   **Top-Center-Baseline**
-   **Bottom-Center-Baseline**

Der Text wird an eine vertikale Position im Textfeld verankert, wie durch den-Attribut Wert angegeben. Die Ausrichtung eines Text Ankers wird nur dann ersichtlich, wenn " [mso-fit-Text-to-Shape](msdn-online-vml-mso-fit-text-to-shape-attribute.md) " den Wert " **false**" hat. Dieses Attribut unterscheidet sich von dem Attribut mit **vertikaler Ausrichtung** , das für ideografische Sprachen verwendet wird.

Dieses Attribut wird von Microsoft Office zum Speichern von Daten in Webdokumenten verwendet, aber nicht in Microsoft Internet Explorer 5 oder höher.

*VML-Standard Attribut*

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



 

 