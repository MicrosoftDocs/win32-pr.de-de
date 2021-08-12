---
title: VML Imagedata-Element
description: VML Imagedata-Element
ms.assetid: 91004646-b031-4973-a32d-7afdd10dab48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3a307dd36daf0ff08d2fab7cd9086a3bc07447872cf36cb41972e4aa5a4d4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118600291"
---
# <a name="vml-imagedata-element"></a>VML Imagedata-Element

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert ein Bild für eine Form.

Die folgenden Attribute ändern ein Bild.



| attribute                                                          | BESCHREIBUNG                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| [ALTHRef](althref-attribute--imagedata--vml.md)                   | Gibt einen alternativen Verweis für ein Bild an.                        |
| [Bilevel](msdn-online-vml-bilevel-attribute.md)                   | Bestimmt, ob ein Bild schwarz und weiß angezeigt wird.          |
| [BlackLevel](msdn-online-vml-blacklevel-attribute.md)             | Bestimmt die Intensität von Schwarz in einem Bild.                        |
| [Key (Schlüssel)](msdn-online-vml-chromakey-attribute.md)               | Definiert die Farbe im Genuss, die als transparent behandelt wird. |
| [CropBottom](msdn-online-vml-cropbottom-attribute.md)             | Definiert den Prozentsatz der Entfernung des Bilds von der unteren Seite.       |
| [CropLeft](msdn-online-vml-cropleft-attribute.md)                 | Definiert den Prozentsatz der Entfernung des Bilds von der linken Seite.         |
| [CropRight](msdn-online-vml-cropright-attribute.md)               | Definiert den Prozentsatz der Entfernung des Bilds von der rechten Seite.        |
| [CropTop](msdn-online-vml-croptop-attribute.md)                   | Definiert den Prozentsatz der Entfernung des Bilds von der oberen Seite.          |
| [DetectMouseClick](detectmouseclick-attribute--imagedata--vml.md) | Bestimmt, ob ein Mausklick erkannt wird.                    |
| [EmbossColor](msdn-online-vml-embosscolor-attribute.md)           | Definiert die Farbe für einbettete Farbeffekte.                         |
| [Gewinnen](msdn-online-vml-gain-attribute.md)                         | Definiert die Intensität aller Farben in einem Bild.                      |
| [Gamma](msdn-online-vml-gamma-attribute.md)                       | Definiert den Kontrast für ein Bild.                          |
| [Graustufen](msdn-online-vml-grayscale-attribute.md)               | Bestimmt, ob ein Bild im Graustufenmodus angezeigt wird.          |
| [Href](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/bb229574(v=vs.85)) | Definiert eine URL für ein Bild.                                           |
| [ID](id-attribute--image--vml.md)                                 | Definiert einen eindeutigen Bezeichner für ein Bild.                             |
| [Film](msdn-online-vml-movie-attribute.md)                       | Definiert einen Zeiger auf ein Filmbild.                                   |
| [OLEID](msdn-online-vml-oleid-attribute.md)                       | Speichert die OLE-ID eines Bilds.                                        |
| [Src](src-attribute--imagedata--vml.md)                           | Definiert eine Quelle für das Image.                                       |
| [Titel](title-attribute--imagedata--vml.md)                       | Definiert den Titel eines Bilds.                                        |



 

**Anmerkungen**

Dieses Element muss innerhalb eines [Shape-Elements](shape-element--vml.md) definiert werden.

Darüber hinaus muss das [**Src-Attribut**](src-attribute--imagedata--vml.md) auf ein Bild verweisen.

Der folgende Code ist der Mindestcode, der zum Erstellen eines Bilds erforderlich ist.


```HTML
   <v:rect
   style="position:relative;top:1;left:1;width:50;height:50">
   <v:imagedata src="../art/kids.jpg"/>
   </v:rect>
```



> [!Note]  
> In Vorabversionen von VML wurde dieses Element **image** genannt.

 

**Beispiele**

-   [Einfaches ImageData-Beispiel](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/image/t_image.md)
-   [Dynamisches ImageData-Beispiel](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/image/x_image.md)

 

 