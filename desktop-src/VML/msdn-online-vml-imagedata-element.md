---
title: VML-Image Data-Element
description: VML-Image Data-Element
ms.assetid: 91004646-b031-4973-a32d-7afdd10dab48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b416a53f97efc8a1f1875eda0e842c4cfbe96bf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338469"
---
# <a name="vml-imagedata-element"></a>VML-Image Data-Element

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert ein Bild für eine Form.

Die folgenden Attribute ändern ein Bild.



| Attribut                                                          | BESCHREIBUNG                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Althref](althref-attribute--imagedata--vml.md)                   | Gibt einen alternativen Verweis für ein Bild an.                        |
| [BiLevel](msdn-online-vml-bilevel-attribute.md)                   | Bestimmt, ob ein Bild in schwarz und weiß angezeigt wird.          |
| [Blacklevel](msdn-online-vml-blacklevel-attribute.md)             | Bestimmt die Intensität von schwarz in einem Bild.                        |
| [Chromakey](msdn-online-vml-chromakey-attribute.md)               | Definiert die Farbe im palatte, die als transparent behandelt wird. |
| [CropBottom](msdn-online-vml-cropbottom-attribute.md)             | Definiert den Prozentsatz der Bild Entfernung von der unteren Seite.       |
| [Durchforsten](msdn-online-vml-cropleft-attribute.md)                 | Definiert den Prozentsatz der Bild Entfernung von der linken Seite.         |
| [Durchschnitt](msdn-online-vml-cropright-attribute.md)               | Definiert den Prozentsatz der Bild Entfernung von der rechten Seite.        |
| [CropTop](msdn-online-vml-croptop-attribute.md)                   | Definiert den Prozentsatz der Bild Entfernung von der oberen Seite aus.          |
| [Detectmoukliklicke](detectmouseclick-attribute--imagedata--vml.md) | Bestimmt, ob ein Mausklick erkannt wird.                    |
| [Embosscolor](msdn-online-vml-embosscolor-attribute.md)           | Definiert die Farbe für Effekte der geprägten Farbe.                         |
| [Erzielen](msdn-online-vml-gain-attribute.md)                         | Definiert die Intensität aller Farben in einem Bild.                      |
| [GAM](msdn-online-vml-gamma-attribute.md)                       | Definiert den Kontrast eines Bilds.                          |
| [Graustufen](msdn-online-vml-grayscale-attribute.md)               | Bestimmt, ob ein Bild im Graustufen Modus angezeigt wird.          |
| [HRef](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/bb229574(v=vs.85)) | Definiert eine URL für ein Bild.                                           |
| [ID](id-attribute--image--vml.md)                                 | Definiert einen eindeutigen Bezeichner für ein Bild.                             |
| [Film](msdn-online-vml-movie-attribute.md)                       | Definiert einen Zeiger auf ein Filmbild.                                   |
| [Oleid](msdn-online-vml-oleid-attribute.md)                       | Speichert die OLE-ID eines Bilds.                                        |
| [Src](src-attribute--imagedata--vml.md)                           | Definiert eine Quelle für das Bild.                                       |
| [Titel](title-attribute--imagedata--vml.md)                       | Definiert den Titel eines Bilds.                                        |



 

**Anmerkungen**

Dieses Element muss innerhalb eines [Shape](shape-element--vml.md) -Elements definiert werden.

Außerdem muss das [**src**](src-attribute--imagedata--vml.md) -Attribut auf ein Bild zeigen.

Im folgenden finden Sie den minimalen Code, der zum Entwickeln eines Bilds erforderlich ist.


```HTML
   <v:rect
   style="position:relative;top:1;left:1;width:50;height:50">
   <v:imagedata src="../art/kids.jpg"/>
   </v:rect>
```



> [!Note]  
> In vorab Versionen von VML hieß dieses Element **Image** .

 

**Beispiele**

-   [Einfaches imagedata-Beispiel](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/image/t_image.md)
-   [Dynamisches imagedata-Beispiel](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/image/x_image.md)

 

 