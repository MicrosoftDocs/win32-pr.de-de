---
description: Eines der wichtigsten Features der Funktionen in der GDI-Druck-API ist die Unterstützung der Geräteunabhängigkeit.
ms.assetid: 3efcc6d0-14f0-4605-9603-ccc7ad0cc895
title: Informationen zur GDI-Druck-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6e8a34552a1198ebe618f463003fe28ded6aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364151"
---
# <a name="about-the-gdi-print-api"></a><span data-ttu-id="8ca49-103">Informationen zur GDI-Druck-API</span><span class="sxs-lookup"><span data-stu-id="8ca49-103">About the GDI Print API</span></span>

<span data-ttu-id="8ca49-104">Eines der wichtigsten Features der Funktionen in der GDI-Druck-API ist die Unterstützung der Geräteunabhängigkeit.</span><span class="sxs-lookup"><span data-stu-id="8ca49-104">One of the chief features of the functions in the GDI print API is their support of device independence.</span></span> <span data-ttu-id="8ca49-105">Anstatt gerätespezifische Befehle auszugeben, um die Ausgabe auf einem bestimmten Drucker oder einem anderen zu zeichnen, ruft eine Anwendung Funktionen auf hoher Ebene von der Graphics Device Interface (GDI) auf.</span><span class="sxs-lookup"><span data-stu-id="8ca49-105">Instead of issuing device-specific commands to draw output on a particular printer or plotter, an application calls high-level functions from the graphics device interface (GDI).</span></span> <span data-ttu-id="8ca49-106">Um z. b. ein Bitmap-Bild auszugeben, kann eine Anwendung die [**BitBLT**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) -Funktion aufzurufen und die Koordinaten für die Bitmap sowie Handles zur Identifizierung der Quell-und Zielgeräte Kontexte (DCS) bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8ca49-106">For example, to print a bitmapped image, an application can call the [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) function, supplying the coordinates for the bitmap as well as handles identifying the source and destination device contexts (DCs).</span></span> <span data-ttu-id="8ca49-107">Der **BitBLT** -Aufrufe wird dann von einem Druckertreiber in unformatierte Geräte Befehle konvertiert.</span><span class="sxs-lookup"><span data-stu-id="8ca49-107">The call to **BitBlt** is then converted to raw device commands by a printer driver.</span></span> <span data-ttu-id="8ca49-108">Ein Gerätetreiber ist eine Dynamic Link Library (dll), die die Gerätetreiber Schnittstelle (DDI) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8ca49-108">A device driver is a dynamic-link library (DLL) that supports the device driver interface (DDI).</span></span> <span data-ttu-id="8ca49-109">Ein Gerätetreiber generiert Rohgeräte Befehle, wenn er Aufrufe an von der Grafik-Engine vorgenommene DDI-Funktionen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="8ca49-109">A device driver generates raw device commands when it processes calls to DDI functions made by the graphics engine.</span></span> <span data-ttu-id="8ca49-110">Die Befehle werden vom Drucker beim Drucken des Bilds verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="8ca49-110">The commands are processed by the printer when it prints the image.</span></span> <span data-ttu-id="8ca49-111">Syntax, Zahl und Typ dieser Befehle variieren von Gerät zu Gerät.</span><span class="sxs-lookup"><span data-stu-id="8ca49-111">The syntax, number, and type of these commands vary from device to device.</span></span>

<span data-ttu-id="8ca49-112">Diese Übersicht enthält Informationen zu den folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="8ca49-112">This overview provides information on the following topics.</span></span>

<dl>

[<span data-ttu-id="8ca49-113">Standarddruck Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="8ca49-113">Default Printing Interface</span></span>](default-printing-interface.md)  
[<span data-ttu-id="8ca49-114">Drucker Geräte Kontexte</span><span class="sxs-lookup"><span data-stu-id="8ca49-114">Printer Device Contexts</span></span>](printer-output.md)  
[<span data-ttu-id="8ca49-115">Drucker Escapezeichen</span><span class="sxs-lookup"><span data-stu-id="8ca49-115">Printer Escapes</span></span>](printer-escapes.md)  
[<span data-ttu-id="8ca49-116">WYSIWYG-Anzeige und-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="8ca49-116">WYSIWYG Display and Output</span></span>](wysiwyg-display-and-output.md)  
[<span data-ttu-id="8ca49-117">DEVMODE pro Benutzer</span><span class="sxs-lookup"><span data-stu-id="8ca49-117">Per-User DEVMODE</span></span>](per-user-devmode.md)  
</dl>

 

 
