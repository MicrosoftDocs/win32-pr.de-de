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
# <a name="using-text-and-fonts"></a><span data-ttu-id="b8172-103">Verwenden von Text und Schriftarten</span><span class="sxs-lookup"><span data-stu-id="b8172-103">Using Text and Fonts</span></span>

<span data-ttu-id="b8172-104">Windows GDI+ stellt mehrere Klassen bereit, die die Grundlage für das Zeichnen von Text bilden.</span><span class="sxs-lookup"><span data-stu-id="b8172-104">Windows GDI+ provides several classes that form the foundation for drawing text.</span></span> <span data-ttu-id="b8172-105">Die [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse verfügt über mehrere [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) -Methoden, mit denen Sie verschiedene Funktionen von Text, z. b. Speicherort, Begrenzungs Rechteck, Schriftart und Format, angeben können.</span><span class="sxs-lookup"><span data-stu-id="b8172-105">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class has several [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) methods that allow you to specify various features of text, such as location, bounding rectangle, font, and format.</span></span> <span data-ttu-id="b8172-106">Weitere Klassen, die zum Text Rendering beitragen, sind [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat), [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection)und [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection).</span><span class="sxs-lookup"><span data-stu-id="b8172-106">Other classes that contribute to text rendering include [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat), [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection), and [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection).</span></span>

<span data-ttu-id="b8172-107">In den folgenden Themen werden Text und Schriftarten ausführlicher behandelt:</span><span class="sxs-lookup"><span data-stu-id="b8172-107">The following topics cover text and fonts in more detail:</span></span>

-   [<span data-ttu-id="b8172-108">Erstellen von Schriftfamilien und Schriftarten</span><span class="sxs-lookup"><span data-stu-id="b8172-108">Constructing Font Families and Fonts</span></span>](-gdiplus-constructing-font-families-and-fonts-use.md)
-   [<span data-ttu-id="b8172-109">Zeichnen von Text</span><span class="sxs-lookup"><span data-stu-id="b8172-109">Drawing Text</span></span>](-gdiplus-drawing-text-use.md)
-   [<span data-ttu-id="b8172-110">Formatieren von Text</span><span class="sxs-lookup"><span data-stu-id="b8172-110">Formatting Text</span></span>](-gdiplus-formatting-text-use.md)
-   [<span data-ttu-id="b8172-111">Auflisten der installierten Schriftarten</span><span class="sxs-lookup"><span data-stu-id="b8172-111">Enumerating Installed Fonts</span></span>](-gdiplus-enumerating-installed-fonts-use.md)
-   [<span data-ttu-id="b8172-112">Erstellen einer privaten Schriftartsammlung</span><span class="sxs-lookup"><span data-stu-id="b8172-112">Creating a Private Font Collection</span></span>](-gdiplus-creating-a-private-font-collection-use.md)
-   [<span data-ttu-id="b8172-113">Abrufen von Schriftart Metriken</span><span class="sxs-lookup"><span data-stu-id="b8172-113">Obtaining Font Metrics</span></span>](-gdiplus-obtaining-font-metrics-use.md)
-   [<span data-ttu-id="b8172-114">Antialiasing mit Text</span><span class="sxs-lookup"><span data-stu-id="b8172-114">Antialiasing with Text</span></span>](-gdiplus-antialiasing-with-text-use.md)

 

 



