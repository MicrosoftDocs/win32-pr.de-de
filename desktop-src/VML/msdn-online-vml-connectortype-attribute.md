---
title: VML Connector Type-Attribut
description: VML Connector Type-Attribut
ms.assetid: acb9050d-c9e4-4d87-96c2-0bd2a1cf6e6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0be0309e478970b93324b98a5efaaae54964435
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340495"
---
# <a name="vml-connectortype-attribute"></a>VML Connector Type-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Gibt den Verbindungstyp an, der zum Verbinden von Formen verwendet wird. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* o:Connector Type = " *Expression* " >

**Anmerkungen**

Mögliche Werte:



| Wert    | BESCHREIBUNG                    |
|----------|--------------------------------|
| none     | Kein Connector.                  |
| direkte | Standard. Ein geradliniger Connector. |
| Bogens    | Ein von einem Elbow geformter Connector.     |
| MMT   | Ein gekrümmter Connector.            |



 

Dieses Attribut kann auch von einer Regel-Engine eines grafischen Editors verwendet werden.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Die Form verwendet eine gerade Linie als Connector.


```HTML
   <v:rect id=myrect fillcolor="red" o:connectortype="straight"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 