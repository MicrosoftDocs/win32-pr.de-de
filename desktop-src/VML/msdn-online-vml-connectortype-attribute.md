---
title: VML-ConnectorType-Attribut
description: VML-ConnectorType-Attribut
ms.assetid: acb9050d-c9e4-4d87-96c2-0bd2a1cf6e6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a552324582729c74ae87c9fcf1cd512334423bb84c43992f265c0b47fffcd98d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601973"
---
# <a name="vml-connectortype-attribute"></a>VML-ConnectorType-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Gibt den Typ des Connectors an, der zum Verknüpfen von Formen verwendet wird. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Formen](shape-element--vml.md)

**Tagsyntax**

<v: *element* o:connectortype=" *ausdruck* ">

**Anmerkungen**

Mögliche Werte:



| Wert    | BESCHREIBUNG                    |
|----------|--------------------------------|
| Keine     | Kein Connector.                  |
| Gerade | Standard. Ein gerader Konnektor. |
| Ellenbogen    | Ein Ellbogenförmiger Konnektor.     |
| Gebogene   | Ein gekrümmte Verbindung.            |



 

Dieses Attribut kann auch von einer Regel-Engine eines grafischen Editors verwendet werden.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Die Form verwendet eine gerade Linie als Verbindung.


```HTML
   <v:rect id=myrect fillcolor="red" o:connectortype="straight"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 