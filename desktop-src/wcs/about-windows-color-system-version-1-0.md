---
title: Informationen zu Windows Color System (WCS), Version 1.0
description: Informationen zu Windows Color System (WCS), Version 1.0
ms.assetid: 2a162840-660e-4a66-ad16-ef3c9b07925e
keywords:
- Windows Color System (WCS), Informationen zu
- WCS (Windows Color System), Informationen zu
- Bild Farbverwaltung, Windows Color System (WCS)
- Farbverwaltung, Windows Color System (WCS)
- Farben, Windows Color System (WCS)
- Farbverwaltung (Image Color Management; ICM)
- ICM (Bildfarben Verwaltung)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ad2673f8b0943e16a1fbbacde11c4469d00b4e
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "106361099"
---
# <a name="about-windows-color-system-version-10"></a><span data-ttu-id="43052-110">Informationen zu Windows Color System (WCS), Version 1.0</span><span class="sxs-lookup"><span data-stu-id="43052-110">About Windows Color System Version 1.0</span></span>

<span data-ttu-id="43052-111">Die Technologie von Microsoft Windows Color System (WCS) stellt sicher, dass ein Farbbild, eine Grafik oder ein Textobjekt so nah wie möglich an die ursprüngliche Absicht auf jedem Gerät gerendert wird, trotz der Unterschiede bei den Abbild Erstellungs Technologien und Farbfunktionen zwischen Geräten</span><span class="sxs-lookup"><span data-stu-id="43052-111">Microsoft Windows Color System (WCS) technology ensures that a color image, graphic or text object is rendered as close as possible to its original intent on any device, despite differences in imaging technologies and color capabilities between devices.</span></span> <span data-ttu-id="43052-112">Unabhängig davon, ob Sie ein Bild oder eine andere Grafik auf einem Farbscanner Scannen, es über das Internet herunterladen, auf dem Bildschirm anzeigen oder bearbeiten oder es für Papier, Film oder andere Medien auslassen, können Sie mit WCS 1,0 die Farben konsistent und genau halten.</span><span class="sxs-lookup"><span data-stu-id="43052-112">Whether you are scanning an image or other graphic on a color scanner, downloading it over the Internet, viewing or editing it on the screen, or outputting it to paper, film, or other media, WCS 1.0 helps you keep its colors consistent and accurate.</span></span>

<span data-ttu-id="43052-113">WCS 1,0 ist ein integraler Bestandteil von Microsoft Windows, da WCS 1,0 in der Windows-Betriebssystem Familie als Satz von Win32-API-Funktionen integriert ist. Sie ist problemlos für beliebige Anwendungen, Gerätetreiber, Geräte Kalibrierungs Tools oder Farb Verwaltungs Module (CMM) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="43052-113">WCS 1.0 is an integral part of Microsoft Windows Because WCS 1.0 is built into the Windows family of operating systems as a set of Win32 API functions, it is readily available to any application, device driver, device calibration tool, or color management module (CMM).</span></span>

<span data-ttu-id="43052-114">Version 1,0 der Abbild Farbverwaltung (Image Color Management, ICM) wurde in Microsoft Windows 95 bereitgestellt und stellt grundlegende Farb Verwaltungsfunktionen innerhalb von Windows-Geräte Kontexten bereit.</span><span class="sxs-lookup"><span data-stu-id="43052-114">Version 1.0 of Image Color Management (ICM) was delivered in Microsoft Windows 95, and provides basic color management capabilities within Windows device contexts.</span></span>

<span data-ttu-id="43052-115">Die ICM-Version 2,0 ist in Windows 98, Windows Millennium Edition, Windows 2000 und Windows XP enthalten und enthält Funktionen, die die Farbverwaltung außerhalb der Geräte Kontexte implementiert haben.</span><span class="sxs-lookup"><span data-stu-id="43052-115">ICM version 2.0 is included in Windows 98, Windows Millennium Edition, Windows 2000, and Windows XP and included functions that implemented color management outside of device contexts.</span></span> <span data-ttu-id="43052-116">Diese Funktionen waren für anspruchsvollere Anforderungen an die Farbverwaltung geeignet, und Anwendungen haben eine bessere Kontrolle über den Farb Verwaltungsprozess.</span><span class="sxs-lookup"><span data-stu-id="43052-116">These functions were suitable for more demanding color management requirements, and give applications greater control over the color-management process.</span></span>

<span data-ttu-id="43052-117">WCS-Version 1,0 ist in Windows Vista enthalten und umfasst eine Reihe von neuen Funktionen, die eine bedeutende Verbesserung der Flexibilität, Transparenz, Vorhersagbarkeit und Erweiterbarkeit von Anbietern bieten.</span><span class="sxs-lookup"><span data-stu-id="43052-117">WCS version 1.0 is included in Windows Vista and includes a variety of new functions that provides significant improvements in flexiblity, transparency, predictability and extensiblity for vendors.</span></span>

<span data-ttu-id="43052-118">Welche Arten von Anwendungen profitieren von der Verwendung von WCS 1,0?</span><span class="sxs-lookup"><span data-stu-id="43052-118">What kinds of applications will benefit from using WCS 1.0?</span></span> <span data-ttu-id="43052-119">Fast jede Anwendung, die heute in einer Windows Vista-Umgebung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="43052-119">Almost any application running in a Windows Vista environment today.</span></span> <span data-ttu-id="43052-120">Die grundlegende Farb Verwaltungsfunktion wird zu einer Anforderung für alle Arten von Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="43052-120">Basic color management capability is becoming a requirement for applications of all kinds.</span></span>

<span data-ttu-id="43052-121">Die Farbanzeige und das Drucken wurden in den letzten Jahren dahingehend verbessert, dass Foto-realistische Farbbilder und komplexe Farbgrafiken nun häufig nicht nur bei der Desktop Veröffentlichung, sondern auch über ein breites Spektrum an Daten-und Präsentations Anwendungen hinweg verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="43052-121">Color display and printing have improved in recent years to the point where photo-realistic color images and complex color graphics are now commonly used not only in desktop publishing, but also across a broad spectrum of data and presentation applications.</span></span> <span data-ttu-id="43052-122">Objekt Technologien wie com und ActiveX verfügen in praktisch jeder Art von Datenbereich über eingebettete Farb Objekte.</span><span class="sxs-lookup"><span data-stu-id="43052-122">Object technologies such as COM and ActiveX have embedded color objects in virtually every kind of data space.</span></span>

<span data-ttu-id="43052-123">Bekleidungs Kataloge, Online Grafiken, Fotoalben von Familien, Firmenlogos, Diagramme, Diagramme, Präsentationen, Druck Vorschauen und Farb Simulationen sind nur einige Beispiele für alltägliche Anwendungen, bei denen es sich um Farb Aspekte handelt.</span><span class="sxs-lookup"><span data-stu-id="43052-123">Clothing catalogs, online art, family photo albums, business logos, charts, graphs, presentations, print previews, and color simulations are just a few examples of everyday applications where color matters.</span></span>

<span data-ttu-id="43052-124">Daher erfordern mehr und mehr Benutzer, dass Ihre Anwendungen in der Lage sind, eine exakte Farbanzeige zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="43052-124">As a result, more and more users are requiring their applications to be capable of accurate color display.</span></span> <span data-ttu-id="43052-125">Das schlechte Farb Rendering ruiniert die Bilder und Grafiken, die für Benutzer zunehmend wichtig sind.</span><span class="sxs-lookup"><span data-stu-id="43052-125">Poor color rendering ruins the images and graphics that are increasingly important to users.</span></span>

<span data-ttu-id="43052-126">Auf einer grundlegenden Ebene sollte fast jede Anwendung in der Lage sein, die Farbe automatisch anzupassen, sodass die Ausgabe auf unterschiedlichen Monitoren und Druckern identisch aussieht.</span><span class="sxs-lookup"><span data-stu-id="43052-126">On a fundamental level, almost any application should be able to adjust color automatically so that its output looks the same on different monitors and printers.</span></span> <span data-ttu-id="43052-127">WCS 1,0 bietet eine Reihe von Funktionen, mit denen Sie diese Art von Farbverwaltung bereitstellen können, die für einen Benutzer transparent ist und nur wenig Aufwand in der Anwendung erfordert.</span><span class="sxs-lookup"><span data-stu-id="43052-127">WCS 1.0 provides a set of functions to deliver this kind of color management that is transparent to a user and requires little overhead in the application.</span></span>

<span data-ttu-id="43052-128">Auf höherer Ebene bietet WCS 1,0 zusätzliche Funktionen, die eine komplexere und steuerbare Farbverwaltung bieten.</span><span class="sxs-lookup"><span data-stu-id="43052-128">On a higher level, WCS 1.0 provides additional functions that deliver more complex and controllable color management.</span></span> <span data-ttu-id="43052-129">Grafiken und Desktop Publishing Anwendungen benötigen diese zusätzlichen Funktionen, damit Ihre Benutzer während eines Produktionsprozesses genau mit der konsistenten Farbe auf vielen Geräten arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="43052-129">Graphics and desktop publishing applications need these additional capabilities to let their users work precisely with consistent color across many devices throughout a production process.</span></span>

<span data-ttu-id="43052-130">Im Allgemeinen 1,0 finden Softwarehersteller, deren Produkte mit Farb Eingabe oder-Ausgabe und Hardwareanbietern von Farb Peripheriegeräten arbeiten, eine wichtige Technologie zum Vereinfachen der Übermittlung erfolgreicher Produkte.</span><span class="sxs-lookup"><span data-stu-id="43052-130">In general, software vendors whose products deal with color input or output and hardware vendors of color peripherals will find WCS 1.0 a key technology for simplifying the delivery of successful products.</span></span> <span data-ttu-id="43052-131">In den folgenden Abschnitten wird Folgendes erläutert:</span><span class="sxs-lookup"><span data-stu-id="43052-131">The following sections include:</span></span>

-   [<span data-ttu-id="43052-132">Neuerungen in Version 1.0 von WCS</span><span class="sxs-lookup"><span data-stu-id="43052-132">What's New in Version 1.0 of WCS</span></span>](what-s-new-in-version-1-0-of-wcs.md)
-   [<span data-ttu-id="43052-133">WCS 1.0-Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="43052-133">WCS 1.0 Availability</span></span>](wcs-1-0-availability.md)

 

 




