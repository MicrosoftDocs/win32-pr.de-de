---
description: Mit einigen geringfügigen Anpassungen an Ihrem Code können Sie die Windows GDI+-Ausgabe an einen Drucker anstatt an einen Bildschirm senden.
ms.assetid: be6286e9-d125-40ad-b33e-b4e734ac2709
title: Drucken (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e3b60010bcb63c553a96c5d70826f3fe0d3d4aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978953"
---
# <a name="printing-gdi"></a><span data-ttu-id="efca4-103">Drucken (GDI+)</span><span class="sxs-lookup"><span data-stu-id="efca4-103">Printing (GDI+)</span></span>

<span data-ttu-id="efca4-104">Mit einigen geringfügigen Anpassungen an Ihrem Code können Sie die Windows GDI+-Ausgabe an einen Drucker anstatt an einen Bildschirm senden.</span><span class="sxs-lookup"><span data-stu-id="efca4-104">With a few minor adjustments to your code, you can send Windows GDI+ output to a printer rather than to a screen.</span></span> <span data-ttu-id="efca4-105">Um auf einem Drucker zu zeichnen, rufen Sie ein Gerätekontext Handle für den Drucker ab, und übergeben [](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Sie dieses Handle an einen grafikkonstruktor.</span><span class="sxs-lookup"><span data-stu-id="efca4-105">To draw on a printer, obtain a device context handle for the printer and pass that handle to a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor.</span></span> <span data-ttu-id="efca4-106">Platzieren Sie die GDI+-Zeichnungs Befehle zwischen Aufrufen von [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) und [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc).</span><span class="sxs-lookup"><span data-stu-id="efca4-106">Place your GDI+ drawing commands in between calls to [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) and [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc).</span></span>

<span data-ttu-id="efca4-107">In den folgenden Themen wird das Senden der GDI+-Ausgabe an Drucker ausführlicher behandelt:</span><span class="sxs-lookup"><span data-stu-id="efca4-107">The following topics cover sending GDI+ output to printers in more detail:</span></span>

-   [<span data-ttu-id="efca4-108">Senden von GDI+-Ausgabe an einen Drucker</span><span class="sxs-lookup"><span data-stu-id="efca4-108">Sending GDI+ Output to a Printer</span></span>](-gdiplus-sending-gdi-output-to-a-printer-use.md)
-   [<span data-ttu-id="efca4-109">Anzeigen eines Druck Dialogfelds</span><span class="sxs-lookup"><span data-stu-id="efca4-109">Displaying a Print Dialog Box</span></span>](-gdiplus-displaying-a-print-dialog-box-use.md)
-   [<span data-ttu-id="efca4-110">Optimieren der Druckausgabe durch Bereitstellen eines Druckerhandles</span><span class="sxs-lookup"><span data-stu-id="efca4-110">Optimizing Printing by Providing a Printer Handle</span></span>](-gdiplus-optimizing-printing-by-providing-a-printer-handle-use.md)

 

 



