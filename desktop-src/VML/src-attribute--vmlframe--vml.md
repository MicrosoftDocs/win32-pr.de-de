---
title: Src-Attribut (vmlframe) (VML)
description: Src-Attribut (vmlframe) (VML)
ms.assetid: 6ac7a3b5-3c1d-43a0-ab92-a03e3bd45733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a9c3ec4849098c9469fba56f26d4c3dd514746
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315494"
---
# <a name="src-attribute-vmlframevml"></a>Src-Attribut (vmlframe) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die Datenquelle für den Frame. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Vmlframe](msdn-online-vml-vmlframe-element.md)

**Tagsyntax**

<v: *Element* src = " *Expression* " >

**Skript Syntax**

*Element* . src = "*Ausdruck*"

*Ausdruck* = *Element*. src

**Anmerkungen**

Das **src** -Attribut kann die folgenden Syntaxen einschließen:

-   URL zu externer Datei. Die Datei muss eine XML-Datei mit folgendem Format sein:
    ```HTML
       <xml xmlns:v = "urn:schemas-microsoft-com:vml">
       .
       .
       .
       </xml>
    ```

    

-   In der Datei müssen Sie über eine oder mehrere VML-Formen mit gültigen IDs verfügen, auf die mit der folgenden Syntax verwiesen werden kann:
    ```HTML
       filename#shapename
    ```

    

-   In der folgenden Referenz haben externe Dateien die Erweiterung. VML, aber es kann eine beliebige Erweiterung verwendet werden:
    ```HTML
       external.vml#image01
    ```

    

-   Sie können auf eine Form innerhalb derselben Datei verweisen, indem Sie die folgende Syntax verwenden:
    ```HTML
       #shapename
    ```

    

Wenn **Clip** **false** ist, wird die Form so skaliert, dass Sie dem Frame entspricht. **True** gibt an, dass Teile der Form, die sich außerhalb des Rahmens befinden, nicht angezeigt werden.

Beachten Sie, dass [Origin](origin-attribute--vmlframe--vml.md) und [size](size-attribute--vmlframe.md) nicht verwendet werden, es sei denn, **Clip** ist **true**.

**VML-Standard Attribut**

**Beispiel**

Das in der externen Datei definierte Bild wird abgeschnitten.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 