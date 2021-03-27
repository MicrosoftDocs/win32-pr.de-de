---
description: Zeichnen von Text
ms.assetid: 8a06f659-4e08-4738-b7a9-956b599c1344
title: Zeichnen von Text (Windows-GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7db44a756ff211bcae7605cb87bdac77005b34f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754424"
---
# <a name="drawing-text-windows-gdi"></a><span data-ttu-id="3ea57-103">Zeichnen von Text (Windows-GDI)</span><span class="sxs-lookup"><span data-stu-id="3ea57-103">Drawing Text (Windows GDI)</span></span>

<span data-ttu-id="3ea57-104">Nachdem eine Anwendung die entsprechende Schriftart ausgewählt hat, legt die erforderlichen Text Formatierungsoptionen fest und berechnet die erforderlichen Zeichen breiten-und Höhenwerte für eine Text Zeichenfolge. Sie kann beginnen, Zeichen und Symbole zu zeichnen, indem Sie eine der Textausgabe Funktionen aufrufen:</span><span class="sxs-lookup"><span data-stu-id="3ea57-104">After an application selects the appropriate font, sets the required text-formatting options, and computes the necessary character width and height values for a string of text, it can begin drawing characters and symbols by calling any of the text-output functions:</span></span>

-   [<span data-ttu-id="3ea57-105">DrawText</span><span class="sxs-lookup"><span data-stu-id="3ea57-105">DrawText</span></span>](/windows/desktop/api/Winuser/nf-winuser-drawtext)
-   [<span data-ttu-id="3ea57-106">Drawtextex</span><span class="sxs-lookup"><span data-stu-id="3ea57-106">DrawTextEx</span></span>](/windows/desktop/api/Winuser/nf-winuser-drawtextexa)
-   [<span data-ttu-id="3ea57-107">Exttextout</span><span class="sxs-lookup"><span data-stu-id="3ea57-107">ExtTextOut</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)
-   [<span data-ttu-id="3ea57-108">Polytextout</span><span class="sxs-lookup"><span data-stu-id="3ea57-108">PolyTextOut</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polytextouta)
-   [<span data-ttu-id="3ea57-109">Tabbedtextout</span><span class="sxs-lookup"><span data-stu-id="3ea57-109">TabbedTextOut</span></span>](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta)
-   [<span data-ttu-id="3ea57-110">TextOut</span><span class="sxs-lookup"><span data-stu-id="3ea57-110">TextOut</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-textouta)

<span data-ttu-id="3ea57-111">Wenn eine Anwendung eine dieser Funktionen aufruft, übergibt das Betriebssystem den Aufruf an die Grafik-Engine, die wiederum den Aufruf an den entsprechenden Gerätetreiber übergibt.</span><span class="sxs-lookup"><span data-stu-id="3ea57-111">When an application calls one of these functions, the operating system passes the call to the graphics engine, which in turn passes the call to the appropriate device driver.</span></span> <span data-ttu-id="3ea57-112">Auf der Gerätetreiber Ebene werden alle diese Aufrufe von einem oder mehreren Aufrufen der eigenen [exttextout](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta) -oder [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) -Funktion des Treibers unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3ea57-112">At the device driver level, all of these calls are supported by one or more calls to the driver's own [ExtTextOut](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta) or [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) function.</span></span> <span data-ttu-id="3ea57-113">Eine Anwendung erreicht die schnellste Ausführung durch Aufrufen von [**exttextout**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), die schnell in einen **exttextout** -Aufruf für das Gerät konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="3ea57-113">An application will achieve the fastest execution by calling [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), which is quickly converted into an **ExtTextOut** call for the device.</span></span> <span data-ttu-id="3ea57-114">Es gibt jedoch Instanzen, wenn eine Anwendung eine der anderen drei Funktionen aufruft. um z. b. mehrere Textzeilen innerhalb der Rahmen eines angegebenen rechteckigen Bereichs zu zeichnen, ist es effizienter, [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="3ea57-114">However, there are instances when an application should call one of the other three functions; for example, to draw multiple lines of text within the borders of a specified rectangular region, it is more efficient to call [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext).</span></span> <span data-ttu-id="3ea57-115">Zum Erstellen einer Tabelle mit mehreren Spalten mit begründeten Textspalten ist es effizienter, [**tabbedtextout**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="3ea57-115">To create a multicolumn table with justified columns of text, it is more efficient to call [**TabbedTextOut**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta).</span></span>

 

 
