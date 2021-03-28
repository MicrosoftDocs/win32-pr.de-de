---
description: Windows GDI+ ist das Subsystem des Betriebssystems Windows XP oder Windows Server 2003, das für die Anzeige von Informationen auf Bildschirmen und Druckern zuständig ist. GDI+ ist eine API, die über einen Satz von C++-Klassen verfügbar gemacht wird.
ms.assetid: 8797e7c4-44d8-49f7-aec8-37ee48c24747
title: Übersicht über GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb6eb3885d33ad332ac61454525367788d7aed56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994190"
---
# <a name="overview-of-gdi"></a><span data-ttu-id="e1e13-104">Übersicht über GDI+</span><span class="sxs-lookup"><span data-stu-id="e1e13-104">Overview of GDI+</span></span>

<span data-ttu-id="e1e13-105">Windows GDI+ ist das Subsystem des Betriebssystems Windows XP oder Windows Server 2003, das für die Anzeige von Informationen auf Bildschirmen und Druckern zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="e1e13-105">Windows GDI+ is the subsystem of the Windows XP operating system or Windows Server 2003 that is responsible for displaying information on screens and printers.</span></span> <span data-ttu-id="e1e13-106">GDI+ ist eine API, die über einen Satz von C++-Klassen verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="e1e13-106">GDI+ is an API that is exposed through a set of C++ classes.</span></span>

<span data-ttu-id="e1e13-107">Wie der Name schon sagt, ist GDI+ der Nachfolger von Windows Graphics Device Interface (GDI), der Grafikgeräte Schnittstelle, die in früheren Versionen von Windows enthalten war.</span><span class="sxs-lookup"><span data-stu-id="e1e13-107">As its name suggests, GDI+ is the successor to Windows Graphics Device Interface (GDI), the graphics device interface included with earlier versions of Windows.</span></span> <span data-ttu-id="e1e13-108">Windows XP oder Windows Server 2003 unterstützt GDI in Bezug auf die Kompatibilität mit vorhandenen Anwendungen, Programmierer neuer Anwendungen sollten GDI+ jedoch für alle Ihre Grafik Anforderungen verwenden, da GDI+ viele der Funktionen von GDI optimiert und außerdem zusätzliche Funktionen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="e1e13-108">Windows XP or Windows Server 2003 supports GDI for compatibility with existing applications, but programmers of new applications should use GDI+ for all their graphics needs because GDI+ optimizes many of the capabilities of GDI and also provides additional features.</span></span>

<span data-ttu-id="e1e13-109">Eine Grafikgeräte Schnittstelle, wie z. b. GDI+, ermöglicht Anwendungs Programmierern, Informationen auf einem Bildschirm oder Drucker anzuzeigen, ohne sich um die Details eines bestimmten Anzeige Geräts kümmern zu müssen.</span><span class="sxs-lookup"><span data-stu-id="e1e13-109">A graphics device interface, such as GDI+, allows application programmers to display information on a screen or printer without having to be concerned about the details of a particular display device.</span></span> <span data-ttu-id="e1e13-110">Der Anwendungsprogrammierer führt Aufrufe an Methoden aus, die von GDI+-Klassen bereitgestellt werden, und diese Methoden führen wiederum die entsprechenden Aufrufe an bestimmte Gerätetreiber aus.</span><span class="sxs-lookup"><span data-stu-id="e1e13-110">The application programmer makes calls to methods provided by GDI+ classes and those methods in turn make the appropriate calls to specific device drivers.</span></span> <span data-ttu-id="e1e13-111">GDI+ isoliert die Anwendung von der Grafikhardware. diese Isolierung ermöglicht es Entwicklern, geräteunabhängige Anwendungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e1e13-111">GDI+ insulates the application from the graphics hardware, and it is this insulation that allows developers to create device-independent applications.</span></span>

 

 



