---
description: Der Drucker-DC kann beim Drucken auf einem Punkt-Matrix-Drucker, einem frei Hand Strahl Drucker, einem Laserdrucker oder einem-Plotter verwendet werden.
ms.assetid: c53f15d8-5a02-4095-8f05-ae309d4553ff
title: Drucker Geräte Kontexte (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7475776a3d13394b210f8289b458b8e99c474c93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978385"
---
# <a name="printer-device-contexts-windows-gdi"></a><span data-ttu-id="b38b1-103">Drucker Geräte Kontexte (Windows GDI)</span><span class="sxs-lookup"><span data-stu-id="b38b1-103">Printer Device Contexts (Windows GDI)</span></span>

<span data-ttu-id="b38b1-104">Der Drucker-DC kann beim Drucken auf einem Punkt-Matrix-Drucker, einem frei Hand Strahl Drucker, einem Laserdrucker oder einem-Plotter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b38b1-104">The printer DC can be used when printing on a dot-matrix printer, ink-jet printer, laser printer, or plotter.</span></span> <span data-ttu-id="b38b1-105">Eine Anwendung erstellt einen Drucker-DC durch Aufrufen der [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) -Funktion und Bereitstellen der entsprechenden Argumente (der Name des Druckertreibers, der Name des Druckers, der Datei-oder Gerätename für das physische Ausgabe Medium und andere Initialisierungs Daten).</span><span class="sxs-lookup"><span data-stu-id="b38b1-105">An application creates a printer DC by calling the [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) function and supplying the appropriate arguments (the name of the printer driver, the name of the printer, the file or device name for the physical output medium, and other initialization data).</span></span> <span data-ttu-id="b38b1-106">Wenn eine Anwendung den Druckvorgang abgeschlossen hat, wird der Drucker-DC durch Aufrufen der [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) -Funktion gelöscht.</span><span class="sxs-lookup"><span data-stu-id="b38b1-106">When an application has finished printing, it deletes the printer DC by calling the [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) function.</span></span> <span data-ttu-id="b38b1-107">Ein Drucker-DC muss von einer Anwendung gelöscht werden. die [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) -Funktion schlägt fehl, wenn eine Anwendung versucht, Sie zum Freigeben eines Drucker-DC zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b38b1-107">An application must delete (rather than release) a printer DC; the [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) function fails when an application attempts to use it to release a printer DC.</span></span>

<span data-ttu-id="b38b1-108">Weitere Informationen finden Sie unter [Druckerausgabe](../printdocs/printer-output.md).</span><span class="sxs-lookup"><span data-stu-id="b38b1-108">For more information, see [Printer Output](../printdocs/printer-output.md).</span></span>

 

 
