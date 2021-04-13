---
title: Schriftarten und Text (OpenGL)
description: Die Microsoft-Implementierung von OpenGL in Windows unterstützt GDI-Grafiken in einem Single-Buffered OpenGL-Fenster.
ms.assetid: 25a45e1a-6c1e-416b-8993-daeefc1100f3
keywords:
- OpenGL unter Windows, Schriftarten
- OpenGL unter Windows, Text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fba4ffe996bd88a6285f615ddacb31e57fc311
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391415"
---
# <a name="fonts-and-text-opengl"></a><span data-ttu-id="c442e-105">Schriftarten und Text (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="c442e-105">Fonts and Text (OpenGL)</span></span>

<span data-ttu-id="c442e-106">Die Microsoft-Implementierung von OpenGL in Windows unterstützt GDI-Grafiken in einem Single-Buffered OpenGL-Fenster.</span><span class="sxs-lookup"><span data-stu-id="c442e-106">Microsoft's implementation of OpenGL in Windows supports GDI graphics in a single-buffered OpenGL window.</span></span> <span data-ttu-id="c442e-107">GDI-Grafiken in einem doppelt gepufferten OpenGL-Fenster werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c442e-107">It does not support GDI graphics in a double-buffered OpenGL window.</span></span> <span data-ttu-id="c442e-108">Daher können Sie nur die Standardfunktionen für GDI-Schriftart und-Text aufrufen, um Text in einem Single-Buffered OpenGL-Fenster zu zeichnen. Sie können diese Funktionen nicht aufrufen, um Text in einem doppelt gepufferten OpenGL-Fenster zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="c442e-108">Thus, you can call only the standard GDI font and text functions to draw text in a single-buffered OpenGL window; you cannot call those functions to draw text in a double-buffered OpenGL window.</span></span>

<span data-ttu-id="c442e-109">Es gibt eine Problem Umgehung für diese Einschränkung bei Text in doppelt gepufferten Fenstern: Build OpenGL-Anzeigelisten für Bitmap-Bilder von Zeichen und führen dann diese anzeigen Listen aus, um Zeichen zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="c442e-109">There is a workaround for this restriction on text in double-buffered windows: build OpenGL display lists for bitmap images of characters, and then execute those display lists to draw characters.</span></span> <span data-ttu-id="c442e-110">Dieser Prozess umfasst drei Hauptschritte:</span><span class="sxs-lookup"><span data-stu-id="c442e-110">There are three main steps in this process:</span></span>

1.  <span data-ttu-id="c442e-111">Wählen Sie eine Schriftart für einen Gerätekontext aus, und legen Sie die Eigenschaften der Schriftart wie gewünscht fest.</span><span class="sxs-lookup"><span data-stu-id="c442e-111">Select a font for a device context, setting the font's properties as desired.</span></span>
2.  <span data-ttu-id="c442e-112">Erstellen Sie eine Reihe von Bitmap-Anzeigelisten basierend auf den Symbolen in der Schriftart des Geräte Kontexts, einer Anzeigeliste für jedes Symbol, das von der Anwendung gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="c442e-112">Create a set of bitmap display lists based on the glyphs in the device context's font, one display list for each glyph that the application will draw.</span></span>
3.  <span data-ttu-id="c442e-113">Zeichnen Sie jedes Symbol mithilfe dieser Bitmap-Anzeigelisten in einer Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c442e-113">Draw each glyph in a string, using those bitmap display lists.</span></span>

<span data-ttu-id="c442e-114">Um die Anzeigelisten zu erstellen, rufen Sie die Funktionen [**wgluseefontbitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) und [**wglusetfontgliederungen**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) auf.</span><span class="sxs-lookup"><span data-stu-id="c442e-114">To create the display lists, call the [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) and [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) functions.</span></span> <span data-ttu-id="c442e-115">Rufen Sie zum Zeichnen von Zeichen in einer Zeichenfolge mithilfe dieser Anzeigelisten die " [**glcalllists**](glcalllists.md)" auf.</span><span class="sxs-lookup"><span data-stu-id="c442e-115">To draw characters in a string using those display lists, call [**glCallLists**](glcalllists.md).</span></span>

<span data-ttu-id="c442e-116">Zum Erstellen von Anwendungen, die leicht lokalisiert werden können und die Ressourcen sparsam verwenden, müssen die Erstellung und Speicherung dieser Symbol Listen der Symbol Anzeige sorgfältig verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="c442e-116">To create applications that are easy to localize and that use resources sparingly, the creation and storage of these glyph image display lists must be managed carefully.</span></span> <span data-ttu-id="c442e-117">Im Gegensatz zu Englisch verfügen viele Sprachen über Alphabete, deren Zeichen Codes über einen relativ großen Satz von Werten reichen.</span><span class="sxs-lookup"><span data-stu-id="c442e-117">Many languages, unlike English, have alphabets whose character codes range over a relatively large set of values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c442e-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c442e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c442e-119">Schriftart-und Text Funktionen</span><span class="sxs-lookup"><span data-stu-id="c442e-119">Font and Text Functions</span></span>](font-and-text-functions.md)
</dt> </dl>

 

 




