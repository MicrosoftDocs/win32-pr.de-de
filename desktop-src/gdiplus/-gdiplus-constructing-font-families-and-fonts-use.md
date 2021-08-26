---
description: Windows GDI+ gruppiert Schriftarten mit derselben Schriftart, aber unterschiedlichen Stilen in Schriftfamilien.
ms.assetid: 57428fae-6af4-47a5-a499-717dc378767a
title: Erstellen von Schriftfamilien und Schriftarten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cc405883eadd85b5b8018f75da270085197aed4792bf1c6848628cce02f457d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015192"
---
# <a name="constructing-font-families-and-fonts"></a>Erstellen von Schriftfamilien und Schriftarten

Windows GDI+ gruppiert Schriftarten mit derselben Schriftart, aber unterschiedlichen Stilen in Schriftfamilien. Die Schriftfamilie Arial enthält beispielsweise die folgenden Schriftarten:

-   Arial Regular
-   Arial Bold
-   Arial Italic
-   Arial Bold Kursiv

GDI+ verwendet vier Formatvorlagen, um Familien zu bilden: normal, fett, kursiv und fett kursiv. Adjektive wie *"narrow"* und *"rounded"* werden nicht als Stile betrachtet. stattdessen sind sie Teil des Familiennamens. Arial Narrow ist z. B. eine Schriftfamilie, deren Elemente die folgenden sind:

-   Arial Narrow Regular
-   Arial Narrow Bold
-   Arial Narrow Italic
-   Arial Narrow Bold Kursiv

Bevor Sie Text mit GDI+ zeichnen können, müssen Sie ein [**FontFamily-Objekt**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) und ein [**Font-Objekt**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) erstellen. Die **FontFamily-Objekte** geben die Schriftart (z. B. Arial) und das **Font-Objekt** die Größe, den Stil und die Einheiten an.

Im folgenden Beispiel wird eine reguläre Arial-Schriftart mit einer Größe von 16 Pixeln erstellt:


```
FontFamily fontFamily(L"Arial");
Font font(&fontFamily, 16, FontStyleRegular, UnitPixel);
            
```



Im vorangehenden Code ist das erste argument, das an den [**Font-Konstruktor**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) übergeben wird, die Adresse des [**FontFamily-Objekts.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) Das zweite Argument gibt die Größe der Schriftart in Einheiten an, die durch das vierte Argument identifiziert werden. Das dritte Argument identifiziert den Stil.

["UnitPixel"](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-unit) ist ein Member der **Unit-Enumeration,** und ["FontStyleRegular"](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-fontstyle) ist ein Member der **FontStyle-Enumeration.** Beide Enumerationen werden in Gdiplusenums.h deklariert.

 

 



