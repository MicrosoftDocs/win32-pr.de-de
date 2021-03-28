---
description: Windows GDI+ gruppiert Schriftarten mit derselben Schriftart, aber unterschiedlichen Stilen in Schriftfamilien.
ms.assetid: 57428fae-6af4-47a5-a499-717dc378767a
title: Erstellen von Schriftfamilien und Schriftarten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2761923847a15be6b1ad51eec0d683129b70b349
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994295"
---
# <a name="constructing-font-families-and-fonts"></a>Erstellen von Schriftfamilien und Schriftarten

Windows GDI+ gruppiert Schriftarten mit derselben Schriftart, aber unterschiedlichen Stilen in Schriftfamilien. Beispielsweise enthält die Familie "Arial Font" die folgenden Schriftarten:

-   Arial Normal
-   Arial Fett
-   Arial kursiv
-   Arial Fett kursiv

GDI+ verwendet vier Stile zum bilden von Familien: regulär, Fett, kursiv und fett formatiert. Adjektive, z. b. *schmale* und *abgerundete* , werden nicht als Stile betrachtet. Sie sind nicht Teil des Familiennamens. Beispielsweise ist Arial Narrow eine Schriftfamilie, deren Member wie folgt lauten:

-   Arial schmale reguläre
-   Arial schmale Fett Formatierung
-   Arial, schmale kursiv
-   Arial schmale Fett kursiv

Bevor Sie Text mit GDI+ zeichnen können, müssen Sie ein [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) -Objekt und ein [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) -Objekt erstellen. Das **FontFamily** -Objekt gibt die Schriftart (z. b. Arial) an, und das **Font** -Objekt gibt die Größe, den Stil und die Einheiten an.

Im folgenden Beispiel wird eine Schriftart mit einem regulären Stil mit einer Größe von 16 Pixeln erstellt:


```
FontFamily fontFamily(L"Arial");
Font font(&fontFamily, 16, FontStyleRegular, UnitPixel);
            
```



Im vorangehenden Code ist das erste Argument, das an den [**Schriftart**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) -Konstruktor übergeben wird, die Adresse des [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) -Objekts. Das zweite Argument gibt die Größe der Schriftart an, die in Einheiten gemessen wird, die durch das vierte Argument identifiziert werden. Das dritte Argument identifiziert den Stil.

[* * * * Unitpixel * * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-unit) * ist ein Member der **Unit** -Enumeration, und [* * * * fontstyleregfeiner * * * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-fontstyle) ist ein Member der **FontStyle** -Enumeration. Beide Enumerationen werden in "gdiplusenums. h" deklariert.

 

 



