---
description: In diesen Themen werden die Dokumente und Druck Features von Windows beschrieben, mit denen Anwendungen gespeichert, angezeigt und gedruckt werden können.
ms.assetid: 20e56af6-9598-4d6a-a2bf-454cef8a3368
title: 'Dokumente und Drucken '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19b23ae7040586d550c47f3fedc59104d83fe818
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106350600"
---
# <a name="documents-and-printing"></a>Dokumente und Drucken 

In diesen Themen werden die Dokumente und Druck Features von Windows beschrieben, mit denen Anwendungen gespeichert, angezeigt und gedruckt werden können.

## <a name="in-this-section"></a>In diesem Abschnitt



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Thema</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/printdocs/what-s-new-for-printing-in-windows-vnext">Neues beim Drucken</a><br/></td>
<td>Windows 8 unterstützt das <a href="/previous-versions/windows/apps/hh465225(v=win.10)">Drucken für Windows Store-Apps mit JavaScript und HTML</a> und das <a href="/previous-versions/windows/apps/hh465196(v=win.10)">Drucken für Windows Store-Apps mithilfe von c#/VB/C + + und XAML</a>.<br/> Windows 8 umfasst auch eine neue COM-basierte API, die vollständige Unterstützung für Open XPS und Zugriff auf Teile der neuen Druckertreiber bietet, die von Windows 8 unterstützt werden. Weitere Informationen zur neuen API finden Sie unter <a href="/windows/desktop/printdocs/tailored-app-printing-api">Print Document Package API</a>.<br/> Das Eingangsbox-Programm für den Windows-Drucktreiber stellt sicher, dass Windows 8 Unterstützung für einen hohen Prozentsatz der beliebten Drucker umfasst<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/printdocs/jobbindalldocuments">XPS-Dokumente</a><br/></td>
<td>Informationen über die XPS-Dokument-API eine digitale XPS-Signatur.<br/>
<ul>
<li><a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">XPS-Dokument-API</a><br/> Die XPS-Dokument-API ist eine native Windows-API, die das XPS-OM unterstützt. Die XPS-Dokument-API wurde in Windows 7 eingeführt und kann im benutzermodusprogramm und in XPSDrv-Druckertreibern verwendet werden.<br/></li>
<li><a href="/previous-versions/windows/desktop/ff819108(v=vs.85)">XPS-API für digitale Signaturen</a><br/> Digitale XPS-Signaturen ermöglichen das Signieren von Dokumenten, die Überprüfung der Identität des Signatur Gebers und die Angabe, ob sich ein XPS-Dokument seit der Signierung geändert hat.<br/></li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="printdocs-printing.md">Drucken</a><br/></td>
<td>Informationen zu den von Windows unterstützten Druck Features. Zu den Features zählen:<br/>
<ul>
<li><a href="/windows/desktop/printdocs/tailored-app-printing-api">Drucken der Dokumenten Paket-API</a><br/> Stellt apps eine Schnittstelle bereit, die die Verwaltung des <strong>PrintDocument</strong> -Pakets ermöglicht.<br/></li>
<li><a href="print-spooler-api.md">Druckspoolerapi</a><br/> Stellt eine Schnittstelle zum Druck Spooler bereit, sodass Anwendungen Drucker und Druckaufträge verwalten können.<br/></li>
<li><a href="print-ticket-api.md">Print Ticket-API</a><br/> Bietet Anwendungen Funktionen zum Verwalten und Konvertieren von Druck Tickets.<br/></li>
<li><a href="gdi-printing.md">GDI-Druck-API</a><br/> Stellt Anwendungen eine geräteunabhängige Druck Schnittstelle bereit. <br/></li>
<li><p><a href="xps-printing.md">XPS-Druck-API</a><br/> Stellt eine Schnittstelle zum Druck Spooler bereit, die Anwendungen verwenden können, um XPS-Dokumente an einen Drucker zu senden.</p>
<blockquote>
[!Note]<br />
Die XPS-Druck-API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Client Anwendungen sollten stattdessen die <a href="/windows/desktop/printdocs/tailored-app-printing-api">API zum Drucken von Dokument Paketen</a> verwenden.
</blockquote>
<p><br/> <br/></p></li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/printdocs/printschema">Druck Schema</a><br/></td>
<td>Das Druck Schema und zugehörige Technologien beschreiben die Features eines Druckers und legen die Druckeinstellungen eines Dokuments für Drucker und das Anzeigen von Anwendungen fest. Die <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">Druck Schema Spezifikation</a> ist ein herunterladbares Dokument, das Informationen über das Druck Schema und seine Verwendung in Dokumenten und Drucken enthält. Die Online Informationen, die in diesem Abschnitt enthalten sind, werden nur für Ihre Informationen bereitgestellt und entsprechen möglicherweise nicht exakt der aktuellen Version der <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">Druck Schema Spezifikation</a>.<br/> Die aktuellen Entwurfs Informationen finden Sie in der <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">Druck Schema Spezifikation</a> .<br/></td>
</tr>
</tbody>
</table>



 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

Die [Beispiel-app "Print Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) " veranschaulicht, wie Sie ab Windows 8 aus einer Windows Store-App drucken.

Die in diesem Abschnitt beschriebenen Funktionen gelten für die systemeigene Windows-Programmierung. Weitere Informationen zur Verwendung ähnlicher Funktionen in der .NET-Programmierung (verwaltete Programmierung) finden Sie unter [Windows Presentation Foundation-Dokumenten](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).

XPS-Dokumente basieren auf der [Paketierungs](/previous-versions/windows/desktop/opc/packaging) -API. Weitere Informationen finden Sie in der Paket-API für den Zugriff auf die Inhalte eines XPS-Dokuments auf niedrigerer Ebene.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bidirektionale Druckerkommunikation (Hardware dev Center)](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>
