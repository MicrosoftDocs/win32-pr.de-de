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
# <a name="printing-documents-and-printing"></a>Drucken (Dokumente und Drucken)

Windows bietet Anwendungen einen kompletten Satz von Funktionen, die das Drucken auf verschiedenen Geräten ermöglichen, z. b. auf Laserdruckern, Vektor Plottern, Raster Druckern und faxcomputern.

## <a name="desktop-app-printing"></a>Drucken von Desktop-Apps

Windows-Programmierer können aus verschiedenen Technologien auswählen, um Sie aus der Anwendung zu drucken.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Technologie</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/printdocs/tailored-app-printing-api">Drucken der Dokumenten Paket-API</a><br/></td>
<td>Stellt eine Schnittstelle bereit, die es einer Anwendung ermöglicht, auf das Druck Dokument Paket zuzugreifen und es zu verwalten. Diese API ist in Windows 8 und höheren Versionen von Windows verfügbar.<br/></td>
</tr>
<tr class="even">
<td><a href="print-spooler-api.md">Druckspoolerapi</a><br/></td>
<td>Stellt eine Schnittstelle zum Druck Spooler bereit, sodass Anwendungen Drucker und Druckaufträge verwalten können.<br/> Anwendungen verwenden die <a href="print-spooler-api.md">druckspoolerapi</a> , um Druckaufträge, die vom Druck Spooler verwaltet werden, zu starten, zu unterbinden, zu steuern und zu konfigurieren, unabhängig davon, ob Sie den Inhalt mit der <a href="/windows/desktop/printdocs/tailored-app-printing-api">API zum Drucken von Dokumenten Paketen</a> oder der <a href="gdi-printing.md">GDI-Druck-API</a><br/></td>
</tr>
<tr class="odd">
<td><a href="print-ticket-api.md">Print Ticket-API</a><br/></td>
<td>Bietet Anwendungen Funktionen zum Verwalten und Konvertieren von Druck Tickets.<br/></td>
</tr>
<tr class="even">
<td><a href="gdi-printing.md">GDI-Druck-API</a><br/></td>
<td>Stellt Anwendungen eine geräteunabhängige Druck Schnittstelle bereit. <br/>
<blockquote>
[!Note]<br />
Entwickler, die Anwendungen für Windows Vista und spätere Versionen von Windows schreiben, sollten die <a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">XPS-Dokument-API</a> in Ihrer Anwendung verwenden.
</blockquote>
<br/> Die <a href="gdi-printing.md">GDI-Druck-API</a> eignet sich für Anwendungen, die unter Windows XP und früheren Versionen von Windows ausgeführt werden müssen.<br/></td>
</tr>
</tbody>
</table>



 

Die folgende Abbildung bietet einen Überblick über die Beziehung zwischen den verschiedenen Druck-APIs.

![ein Diagramm, das zeigt, wie eine systemeigene Windows-Anwendung die Print-APIs verwenden kann](images/print-apis.png)

 

Die API für das Drucken von [Dokument Paketen](./tailored-app-printing-api.md)in diesem Abschnitt beschreibt die Schnittstellen "Druck Dokument Paket" und "Druckvorschau", die Sie mit Windows 8 und höheren Versionen von Windows Desktop verwenden können.

Weitere Informationen zum Drucken aus Windows Store-Apps, die in JavaScript und HTML geschrieben sind, finden Sie unter [Drucken (Windows Store-Apps mit JavaScript und HTML)](/previous-versions/windows/apps/hh465225(v=win.10)). Weitere Informationen zum Drucken aus Windows Store-Apps, die in c#, Microsoft Visual Basic oder C++ und XAML geschrieben sind, finden Sie unter [Drucken (Windows Store-Apps mit C)](/previous-versions/windows/apps/hh465196(v=win.10)).

> [!Note]  
> Unter [Win32 und com für Windows Store-Apps (Drucken und Dokumente)](/uwp/win32-and-com/win32-and-com-for-uwp-apps) finden Sie eine Liste der Drucker-APIs für die Desktop-App, die auch in Windows Store-Apps verwendet werden können.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[XPS-Dokument-API](/previous-versions/windows/desktop/dd316976(v=vs.85))
</dt> <dt>

[Bidirektionale Druckerkommunikation (Hardware dev Center)](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>

