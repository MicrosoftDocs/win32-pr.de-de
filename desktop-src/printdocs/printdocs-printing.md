---
description: Windows bietet Anwendungen einen kompletten Satz von Funktionen, die das Drucken auf verschiedenen Geräten ermöglichen, z. b. auf Laserdruckern, Vektor Plottern, Raster Druckern und faxcomputern.
ms.assetid: e5c115b0-9c1e-46e7-8fb5-eddbc2c75298
title: Drucken (Dokumente und Drucken)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 607e845ffc525701489a53c2a6b4628eceb5840d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350305"
---
# <a name="printing-documents-and-printing"></a><span data-ttu-id="faea3-103">Drucken (Dokumente und Drucken)</span><span class="sxs-lookup"><span data-stu-id="faea3-103">Printing (Documents and Printing)</span></span>

<span data-ttu-id="faea3-104">Windows bietet Anwendungen einen kompletten Satz von Funktionen, die das Drucken auf verschiedenen Geräten ermöglichen, z. b. auf Laserdruckern, Vektor Plottern, Raster Druckern und faxcomputern.</span><span class="sxs-lookup"><span data-stu-id="faea3-104">Windows provides applications with a complete set of functions that allow printing to various devices, such as laser printers, vector plotters, raster printers, and fax machines.</span></span>

## <a name="desktop-app-printing"></a><span data-ttu-id="faea3-105">Drucken von Desktop-Apps</span><span class="sxs-lookup"><span data-stu-id="faea3-105">Desktop App Printing</span></span>

<span data-ttu-id="faea3-106">Windows-Programmierer können aus verschiedenen Technologien auswählen, um Sie aus der Anwendung zu drucken.</span><span class="sxs-lookup"><span data-stu-id="faea3-106">Windows programmers can select from several different technologies to print from their application.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="faea3-107">Technologie</span><span class="sxs-lookup"><span data-stu-id="faea3-107">Technology</span></span></th>
<th><span data-ttu-id="faea3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="faea3-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="faea3-109"><a href="/windows/desktop/printdocs/tailored-app-printing-api">Drucken der Dokumenten Paket-API</a></span><span class="sxs-lookup"><span data-stu-id="faea3-109"><a href="/windows/desktop/printdocs/tailored-app-printing-api">Print Document Package API</a></span></span><br/></td>
<td><span data-ttu-id="faea3-110">Stellt eine Schnittstelle bereit, die es einer Anwendung ermöglicht, auf das Druck Dokument Paket zuzugreifen und es zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="faea3-110">Provides an interface that allows an application to access and manage the print document package.</span></span> <span data-ttu-id="faea3-111">Diese API ist in Windows 8 und höheren Versionen von Windows verfügbar.</span><span class="sxs-lookup"><span data-stu-id="faea3-111">This API is available with Windows 8 and later versions of Windows.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="faea3-112"><a href="print-spooler-api.md">Druckspoolerapi</a></span><span class="sxs-lookup"><span data-stu-id="faea3-112"><a href="print-spooler-api.md">Print Spooler API</a></span></span><br/></td>
<td><span data-ttu-id="faea3-113">Stellt eine Schnittstelle zum Druck Spooler bereit, sodass Anwendungen Drucker und Druckaufträge verwalten können.</span><span class="sxs-lookup"><span data-stu-id="faea3-113">Provides an interface to the print spooler so that applications can manage printers and print jobs.</span></span><br/> <span data-ttu-id="faea3-114">Anwendungen verwenden die <a href="print-spooler-api.md">druckspoolerapi</a> , um Druckaufträge, die vom Druck Spooler verwaltet werden, zu starten, zu unterbinden, zu steuern und zu konfigurieren, unabhängig davon, ob Sie den Inhalt mit der <a href="/windows/desktop/printdocs/tailored-app-printing-api">API zum Drucken von Dokumenten Paketen</a> oder der <a href="gdi-printing.md">GDI-Druck-API</a></span><span class="sxs-lookup"><span data-stu-id="faea3-114">Applications use the <a href="print-spooler-api.md">Print Spooler API</a> to start, stop, control, and configure print jobs managed by the print spooler whether they use the <a href="/windows/desktop/printdocs/tailored-app-printing-api">Print Document Package API</a> or the <a href="gdi-printing.md">GDI Print API</a> to print the content.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="faea3-115"><a href="print-ticket-api.md">Print Ticket-API</a></span><span class="sxs-lookup"><span data-stu-id="faea3-115"><a href="print-ticket-api.md">Print Ticket API</a></span></span><br/></td>
<td><span data-ttu-id="faea3-116">Bietet Anwendungen Funktionen zum Verwalten und Konvertieren von Druck Tickets.</span><span class="sxs-lookup"><span data-stu-id="faea3-116">Provides applications with functions to manage and convert print tickets.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="faea3-117"><a href="gdi-printing.md">GDI-Druck-API</a></span><span class="sxs-lookup"><span data-stu-id="faea3-117"><a href="gdi-printing.md">GDI Print API</a></span></span><br/></td>
<td><span data-ttu-id="faea3-118">Stellt Anwendungen eine geräteunabhängige Druck Schnittstelle bereit.</span><span class="sxs-lookup"><span data-stu-id="faea3-118">Provides applications with a device-independent printing interface.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="faea3-119">Entwickler, die Anwendungen für Windows Vista und spätere Versionen von Windows schreiben, sollten die <a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">XPS-Dokument-API</a> in Ihrer Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="faea3-119">Developers who are writing applications for Windows Vista and later versions of Windows should consider using the <a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">XPS Document API</a> in their application.</span></span>
</blockquote>
<br/> <span data-ttu-id="faea3-120">Die <a href="gdi-printing.md">GDI-Druck-API</a> eignet sich für Anwendungen, die unter Windows XP und früheren Versionen von Windows ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="faea3-120">The <a href="gdi-printing.md">GDI Print API</a> is suitable for applications that must run on Windows XP and earlier versions of Windows.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="faea3-121">Die folgende Abbildung bietet einen Überblick über die Beziehung zwischen den verschiedenen Druck-APIs.</span><span class="sxs-lookup"><span data-stu-id="faea3-121">The following illustration provides a high-level view of how the different printing APIs are related.</span></span>

![ein Diagramm, das zeigt, wie eine systemeigene Windows-Anwendung die Print-APIs verwenden kann](images/print-apis.png)

 

<span data-ttu-id="faea3-123">Die API für das Drucken von [Dokument Paketen](./tailored-app-printing-api.md)in diesem Abschnitt beschreibt die Schnittstellen "Druck Dokument Paket" und "Druckvorschau", die Sie mit Windows 8 und höheren Versionen von Windows Desktop verwenden können.</span><span class="sxs-lookup"><span data-stu-id="faea3-123">The [Print Document Package API](./tailored-app-printing-api.md)s in this section describe the print document package and print preview interfaces that you can use with Windows 8 and later versions of Windows desktop.</span></span>

<span data-ttu-id="faea3-124">Weitere Informationen zum Drucken aus Windows Store-Apps, die in JavaScript und HTML geschrieben sind, finden Sie unter [Drucken (Windows Store-Apps mit JavaScript und HTML)](/previous-versions/windows/apps/hh465225(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="faea3-124">For more info about printing from Windows Store apps that are written in JavaScript and HTML, see [Printing (Windows Store apps using JavaScript and HTML)](/previous-versions/windows/apps/hh465225(v=win.10)).</span></span> <span data-ttu-id="faea3-125">Weitere Informationen zum Drucken aus Windows Store-Apps, die in c#, Microsoft Visual Basic oder C++ und XAML geschrieben sind, finden Sie unter [Drucken (Windows Store-Apps mit C)](/previous-versions/windows/apps/hh465196(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="faea3-125">For more info about printing from Windows Store apps that are written in C#, Microsoft Visual Basic, or C++ and XAML, see [Printing (Windows Store apps using C)](/previous-versions/windows/apps/hh465196(v=win.10)).</span></span>

> [!Note]  
> <span data-ttu-id="faea3-126">Unter [Win32 und com für Windows Store-Apps (Drucken und Dokumente)](/uwp/win32-and-com/win32-and-com-for-uwp-apps) finden Sie eine Liste der Drucker-APIs für die Desktop-App, die auch in Windows Store-Apps verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="faea3-126">See [Win32 and COM for Windows Store apps (printing and documents)](/uwp/win32-and-com/win32-and-com-for-uwp-apps) for the list of the Desktop App Printing APIs that can also be used in Windows Store apps.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="faea3-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="faea3-127">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="faea3-128">[XPS-Dokument-API](/previous-versions/windows/desktop/dd316976(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="faea3-128">[XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="faea3-129">Bidirektionale Druckerkommunikation (Hardware dev Center)</span><span class="sxs-lookup"><span data-stu-id="faea3-129">Bidirectional printer communications (Hardware Dev Center)</span></span>](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>

