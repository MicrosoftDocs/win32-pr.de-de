---
title: VML-Inset-Attribut
description: VML-Inset-Attribut
ms.assetid: b50f900a-b0dc-4042-af9e-050011307765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1d4b44756034a3ebc7e46e1cdda43042f347e58cb87c02b00c90a14320a40f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118600236"
---
# <a name="vml-inset-attribute"></a>VML-Inset-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Gibt innere Randwerte für Textfeldtext an. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[TextBox](msdn-online-vml-textbox-element.md)

**Tagsyntax**

<v: *element* inset=" *ausdruck* ">

**Skriptsyntax**

*element* .inset="*expression*"

*expression* = .inset-Element

**Anmerkungen**

Der interne Textrandwert wird als Zeichenfolge mit vier Werten angegeben, die jeweils durch Kommas oder Leerzeichen getrennt sind. Die Werte messen Denkmenge von links, oben, rechts und unteren Rändern des Felds, das durch das [TextBoxRect-Attribut](msdn-online-vml-textboxrect-attribute.md) von **Path** angegeben wird. Fehlende Werte werden auf den Standardwert "0.1in, 0.05in, 0.1in, 0.05in" festgelegt.

Bei gedrehten Formen in Browsern, die keine Drehung unterstützen, wird der Begrenzungsfeld am nächsten Vielfachen von 90 Grad ausgerichtet.

*VML-Standardattribut*

**Beispiel**

Das Textfeld hat einen Eingangsrand von 10 Pixeln.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox id="mytextbox" inset="10px, 10px, 10px, 10px">
   VML
   </v:textbox/>
   </v:shape>
```



 

 