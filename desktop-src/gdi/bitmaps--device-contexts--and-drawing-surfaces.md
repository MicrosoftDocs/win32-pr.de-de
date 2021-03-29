---
description: Ein Gerätekontext (DC) ist eine Datenstruktur, die die Grafik Objekte, ihre zugeordneten Attribute und die Grafikmodi zum beeinflussen der Ausgabe auf einem Gerät definiert. Um einen Domänen Controller zu erstellen, rufen Sie die Funktion "-Funktion" auf. Rufen Sie zum Abrufen eines DC die GetDC-Funktion auf.
ms.assetid: 4feafb23-bf5a-493a-9d1d-96170711b907
title: Bitmaps, Geräte Kontexte und Zeichnungs Oberflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6297eb3446d05d0fa21ac23c9de9f3416a300746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215216"
---
# <a name="bitmaps-device-contexts-and-drawing-surfaces"></a><span data-ttu-id="9f1fa-104">Bitmaps, Geräte Kontexte und Zeichnungs Oberflächen</span><span class="sxs-lookup"><span data-stu-id="9f1fa-104">Bitmaps, Device Contexts, and Drawing Surfaces</span></span>

<span data-ttu-id="9f1fa-105">Ein *Gerätekontext* (DC) ist eine Datenstruktur, die die Grafik Objekte, ihre zugeordneten Attribute und die Grafikmodi zum beeinflussen der Ausgabe auf einem Gerät definiert.</span><span class="sxs-lookup"><span data-stu-id="9f1fa-105">A *device context* (DC) is a data structure defining the graphics objects, their associated attributes, and the graphics modes affecting output on a device.</span></span> <span data-ttu-id="9f1fa-106">Um einen Domänen Controller zu erstellen, rufen Sie [**die Funktion "**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) -Funktion" auf. Rufen Sie zum Abrufen eines DC die [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="9f1fa-106">To create a DC, call the [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) function; to retrieve a DC, call the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) function.</span></span>

<span data-ttu-id="9f1fa-107">Vor dem Zurückgeben eines Handles, das diesen DC identifiziert, wählt das System eine Zeichen Oberfläche in den DC aus.</span><span class="sxs-lookup"><span data-stu-id="9f1fa-107">Before returning a handle that identifies that DC, the system selects a drawing surface into the DC.</span></span> <span data-ttu-id="9f1fa-108">Wenn die Anwendung die Funktion " [**deedc**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) " aufgerufen hat, um einen Gerätekontext für eine VGA-Anzeige zu erstellen, sind die Dimensionen dieser Zeichnungs Oberfläche 640 x 480 Pixel.</span><span class="sxs-lookup"><span data-stu-id="9f1fa-108">If the application called the [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) function to create a device context for a VGA display, the dimensions of this drawing surface are 640-by-480 pixels.</span></span> <span data-ttu-id="9f1fa-109">Wenn die Anwendung die [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) -Funktion aufrief, entsprechen die Dimensionen der Größe des Client Bereichs.</span><span class="sxs-lookup"><span data-stu-id="9f1fa-109">If the application called the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) function, the dimensions reflect the size of the client area.</span></span>

<span data-ttu-id="9f1fa-110">Bevor eine Anwendung mit dem Zeichnen beginnen kann, muss Sie durch Aufrufen der [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) -Funktion eine Bitmap mit der entsprechenden Breite und Höhe in den DC auswählen.</span><span class="sxs-lookup"><span data-stu-id="9f1fa-110">Before an application can begin drawing, it must select a bitmap with the appropriate width and height into the DC by calling the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function.</span></span> <span data-ttu-id="9f1fa-111">Wenn eine Anwendung das Handle an den Domänen Controller an eine der Zeichenfunktionen der Grafikgeräte Schnittstelle (GDI) übergibt, wird die angeforderte Ausgabe auf der Zeichen Oberfläche angezeigt, die im DC ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="9f1fa-111">When an application passes the handle to the DC to one of the graphics device interface (GDI) drawing functions, the requested output appears on the drawing surface selected into the DC.</span></span>

<span data-ttu-id="9f1fa-112">Weitere Informationen finden Sie unter Arbeits [Speicher-Geräte Kontexte](memory-device-contexts.md).</span><span class="sxs-lookup"><span data-stu-id="9f1fa-112">For more information, see [Memory Device Contexts](memory-device-contexts.md).</span></span>

 

 



