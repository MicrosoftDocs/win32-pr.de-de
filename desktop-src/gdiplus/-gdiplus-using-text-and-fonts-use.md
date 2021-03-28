---
description: Windows GDI+ stellt mehrere Klassen bereit, die die Grundlage für das Zeichnen von Text bilden.
ms.assetid: 12bc38c3-5fbc-4d7b-902c-92a5f5057473
title: Verwenden von Text und Schriftarten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f28ec157888dcf45b309237eb0f7eefff17808c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526057"
---
# <a name="using-text-and-fonts"></a>Verwenden von Text und Schriftarten

Windows GDI+ stellt mehrere Klassen bereit, die die Grundlage für das Zeichnen von Text bilden. Die [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse verfügt über mehrere [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) -Methoden, mit denen Sie verschiedene Funktionen von Text, z. b. Speicherort, Begrenzungs Rechteck, Schriftart und Format, angeben können. Weitere Klassen, die zum Text Rendering beitragen, sind [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat), [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection)und [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection).

In den folgenden Themen werden Text und Schriftarten ausführlicher behandelt:

-   [Erstellen von Schriftfamilien und Schriftarten](-gdiplus-constructing-font-families-and-fonts-use.md)
-   [Zeichnen von Text](-gdiplus-drawing-text-use.md)
-   [Formatieren von Text](-gdiplus-formatting-text-use.md)
-   [Auflisten der installierten Schriftarten](-gdiplus-enumerating-installed-fonts-use.md)
-   [Erstellen einer privaten Schriftartsammlung](-gdiplus-creating-a-private-font-collection-use.md)
-   [Abrufen von Schriftart Metriken](-gdiplus-obtaining-font-metrics-use.md)
-   [Antialiasing mit Text](-gdiplus-antialiasing-with-text-use.md)

 

 



