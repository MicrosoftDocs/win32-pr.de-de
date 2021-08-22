---
description: Windows GDI+ stellt mehrere Klassen bereit, die die Grundlage für das Zeichnen von Text bilden.
ms.assetid: 12bc38c3-5fbc-4d7b-902c-92a5f5057473
title: Verwenden von Text und Schriftarten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2cffc8c36da4c9dd8bbc78c6660a7cc85094071350003c5b23ce4d6a6ce7cad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119359600"
---
# <a name="using-text-and-fonts"></a>Verwenden von Text und Schriftarten

Windows GDI+ stellt mehrere Klassen bereit, die die Grundlage für das Zeichnen von Text bilden. Die [**Graphics-Klasse**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) verfügt über mehrere [DrawString-Methoden,](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) mit denen Sie verschiedene Textfeatures angeben können, z. B. Position, umgrenzendes Rechteck, Schriftart und Format. Andere Klassen, die zum Textrendering beitragen, sind [**FontFamily,**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) [**Font,**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) [**StringFormat,**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection)und [**PrivateFontCollection.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection)

In den folgenden Themen werden Text und Schriftarten ausführlicher behandelt:

-   [Erstellen von Schriftfamilien und Schriftarten](-gdiplus-constructing-font-families-and-fonts-use.md)
-   [Zeichnen von Text](-gdiplus-drawing-text-use.md)
-   [Formatieren von Text](-gdiplus-formatting-text-use.md)
-   [Auflisten der installierten Schriftarten](-gdiplus-enumerating-installed-fonts-use.md)
-   [Erstellen einer privaten Schriftartsammlung](-gdiplus-creating-a-private-font-collection-use.md)
-   [Abrufen von Schriftartmetriken](-gdiplus-obtaining-font-metrics-use.md)
-   [Antialiasing mit Text](-gdiplus-antialiasing-with-text-use.md)

 

 



