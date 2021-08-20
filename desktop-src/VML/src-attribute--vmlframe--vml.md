---
title: Src-Attribut (VMLFrame)(VML)
description: Src-Attribut (VMLFrame)(VML)
ms.assetid: 6ac7a3b5-3c1d-43a0-ab92-a03e3bd45733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a44f7761a55304eefc655d00ed58d84b7af8f7ce5daf86a3aaf462308b43c193
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057582"
---
# <a name="src-attribute-vmlframevml"></a>Src-Attribut (VMLFrame)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die Quelle der Daten für den Frame. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Tagsyntax**

<v: *element* src=" *ausdruck* ">

**Skriptsyntax**

*element* .src="*expression*"

*expression* = *.src-Element*

**Anmerkungen**

Das **Src-Attribut** kann die folgenden Syntaxen umfassen:

-   URL zur externen Datei. Die Datei muss eine XML-Datei im folgenden Format sein:
    ```HTML
       <xml xmlns:v = "urn:schemas-microsoft-com:vml">
       .
       .
       .
       </xml>
    ```

    

-   Innerhalb der Datei benötigen Sie mindestens eine VML-Form mit gültigen IDs, auf die mithilfe dieser Syntax verwiesen werden kann:
    ```HTML
       filename#shapename
    ```

    

-   In der folgenden Referenz haben externe Dateien die Erweiterung .vml, aber jede Erweiterung kann verwendet werden:
    ```HTML
       external.vml#image01
    ```

    

-   Sie können in derselben Datei mithilfe der folgenden Syntax auf eine Form verweisen:
    ```HTML
       #shapename
    ```

    

Wenn **Clip** **auf False** festgelegt ist, wird die Form an den Frame angepasst. **True** gibt an, dass teile der Form, die sich außerhalb des Rahmens befinden, nicht angezeigt werden.

Beachten Sie, dass [Ursprung](origin-attribute--vmlframe--vml.md) und [Größe](size-attribute--vmlframe.md) nur verwendet werden, wenn **Clip** **true** ist.

**VML-Standardattribut**

**Beispiel**

Das in der externen Datei definierte Bild wird abgeschnitten.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 