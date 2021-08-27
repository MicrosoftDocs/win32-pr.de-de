---
description: In diesen Themen werden die Dokumente und Druckfeatures von Windows beschrieben, mit denen Anwendungen speichern, anzeigen und drucken können.
ms.assetid: 20e56af6-9598-4d6a-a2bf-454cef8a3368
title: 'Dokumente und Drucken '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87d7af92af0615dcb11d2623be8f2e21ae813aa1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472366"
---
# <a name="documents-and-printing"></a>Dokumente und Drucken 

In diesen Themen werden die Dokumente und Druckfeatures von Windows beschrieben, mit denen Anwendungen speichern, anzeigen und drucken können.

## <a name="in-this-section"></a>In diesem Abschnitt




| Thema | BESCHREIBUNG | 
|-------|-------------|
| <a href="/windows/desktop/printdocs/what-s-new-for-printing-in-windows-vnext">Neues beim Drucken</a><br /> | Windows 8 unterstützt das Drucken für Windows Store-Apps mit <a href="/previous-versions/windows/apps/hh465225(v=win.10)">JavaScript</a> und HTML sowie das Drucken für Windows Store-Apps mit <a href="/previous-versions/windows/apps/hh465196(v=win.10)">C#/VB/C++ und XAML.</a><br /> Windows 8 enthält auch eine neue COM-basierte API, die vollständige Unterstützung für Open XPS und Zugriff auf Teile der neuen Druckertreiber bietet, die von Windows 8 werden. Weitere Informationen zur neuen API finden Sie unter <a href="/windows/desktop/printdocs/tailored-app-printing-api">Druckdokumentpaket-API</a>.<br /> Das Windows Print Driver Inbox Program stellt sicher, dass Windows 8 einen hohen Prozentsatz der beliebten Drucker unterstützt.<br /> | 
| <a href="/windows/desktop/printdocs/jobbindalldocuments">XPS-Dokumente</a><br /> | Informationen zur XPS-Dokument-API und XPS Digital Signatures.<br /><ul><li><a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">XPS-Dokument-API</a><br /> Die XPS-Dokument-API ist eine native Windows-API, die XPS OM unterstützt. Die XPS-Dokument-API wurde in Windows 7 eingeführt und kann in Benutzermodusprogrammen und XPSDrv-Druckertreibern verwendet werden.<br /></li><li><a href="/previous-versions/windows/desktop/ff819108(v=vs.85)">XPS Digital Signature-API</a><br /> XPS Digital Signatures ermöglichen das Signieren von Dokumenten, die Überprüfung der Identität des Signaturers und das Anzeigen, ob sich ein XPS-Dokument seit seiner Signierung geändert hat.<br /></li></ul> | 
| <a href="printdocs-printing.md">Drucken</a><br /> | Informationen zu den Druckfunktionen, die von der Windows. Zu diesen Features zählen:<br /><ul><li><a href="/windows/desktop/printdocs/tailored-app-printing-api">Druckdokumentpaket-API</a><br /> Stellt Apps eine Schnittstelle bereit, die die Verwaltung des <strong>PrintDocument-Pakets</strong> ermöglicht.<br /></li><li><a href="print-spooler-api.md">Druckspooler-API</a><br /> Stellt eine Schnittstelle für den Druckspooler bereit, damit Anwendungen Drucker und Druckaufträge verwalten können.<br /></li><li><a href="print-ticket-api.md">Druckticket-API</a><br /> Stellt Anwendungen Funktionen zum Verwalten und Konvertieren von Drucktickets zur Verfügung.<br /></li><li><a href="gdi-printing.md">GDI-Druck-API</a><br /> Stellt Anwendungen eine geräteunabhängige Druckschnittstelle bereit. <br /></li><li><p><a href="xps-printing.md">XPS-Druck-API</a><br /> Stellt eine Schnittstelle für den Druckspooler bereit, mit dem Anwendungen XPS-Dokumente an einen Drucker senden können.</p><blockquote>[!Note]<br />Die XPS-Druck-API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Clientanwendungen sollten stattdessen die <a href="/windows/desktop/printdocs/tailored-app-printing-api">Druckdokumentpaket-API</a> verwenden.</blockquote><p><br /><br /></p></li></ul> | 
| <a href="/windows/desktop/printdocs/printschema">Druckschema</a><br /> | Das Druckschema und verwandte Technologien beschreiben die Funktionen eines Druckers und geben die Druckeinstellungen eines Dokuments für Drucker und das Anzeigen von Anwendungen an. Die <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">Druckschemaspezifikation ist</a> ein herunterladbares Dokument, das Informationen zum Druckschema und zur Verwendung in Dokumenten und zum Drucken enthält. Die Onlineinformationen in diesem Abschnitt werden nur für Ihre Informationen bereitgestellt und spiegeln möglicherweise nicht genau die aktuelle Version der <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">Druckschemaspezifikation wider.</a><br /> Die aktuellen <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">Entwurfsinformationen finden Sie</a> unter Spezifikation des Druckschemas.<br /> | 




 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

Die [Beispiel-App "Beispiel drucken"](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) veranschaulicht, wie sie aus einer Windows Store-App aus druckt, beginnend mit Windows 8.

Die in diesem Abschnitt beschriebenen Features gelten für die native Windows Programmierung. Informationen zur Verwendung ähnlicher Funktionen in der .NET-Programmierung (verwaltet) finden Sie unter [Windows Presentation Foundation Documents](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85))( Dokumente ).

XPS-Dokumente bauen auf der [Paketierungs-API](/previous-versions/windows/desktop/opc/packaging) auf. Informationen zum Zugriff auf inhalte eines XPS-Dokuments auf niedrigerer Ebene finden Sie in der Paket-API.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bidirektionale Druckerkommunikation (Hardware Dev Center)](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>
