---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 296255b8-fe5c-46dd-b717-487aaae0db80
title: Farbverwaltung und das Druck Schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 134a598466fd52c66d632a28c750840d4123f529
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "103869652"
---
# <a name="color-management-and-the-print-schema"></a>Farbverwaltung und das Druck Schema

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Vom benutzerkonfigurierbare Element Schlüsselwörter können entweder XPS-spezifisch oder nicht-XPS-spezifisch sein. Wenn Sie nicht XPS-spezifisch sind, kann das-Schlüsselwort für das Legacy-GDI-basierte Drucken verwendet werden. Wenn eine Anwendung entscheidet, diese Schlüsselwörter in einem PrintTicket festzulegen, liegt es an dem Treiber, die ordnungsgemäße Aktion und das Verhalten zu ermitteln, die basierend auf den im Druck Schema dargestellten Definitionen ausgeführt werden. Jedes dieser Schlüsselwörter kann im Kontext von ICM verwendet werden. Weitere Informationen finden Sie unter Windows Vista SDK.



| Schlüsselwort für Benutzer konfigurierbares Druck Schema       | DEVMODE-Entsprechung     | XPS-spezifisch   |
|----------------------------------------------|------------------------|----------------|
| Pagecolormanagement<br/>               | dmicmmethod<br/> | Nein<br/>  |
| "Pgeblackgenerationprocessing"<br/>     | Keine<br/>        | Ja<br/> |
| "Pgeblendcolorspace"<br/>               | Keine<br/>        | Ja<br/> |
| Pagesourcecolorprofile<br/>            | Keine<br/>        | Nein<br/>  |
| Pagedestinationcolorprofile<br/>       | Keine<br/>        | Nein<br/>  |
| Pageicmrenderingintent<br/>            | dmicmintent<br/> | Nein<br/>  |
| Joboptimaldestinationcolorprofile<br/> | Keine<br/>        | Nein<br/>  |
| Pagede vicecolorspaceusage<br/>         | Keine<br/>        | Ja<br/> |



 

## <a name="pagecolormanagement-system-handling"></a>Behandlung von pagecolormanagement-Systemen

Für pagecolormanagement bietet das System bei Bedarf automatische Behandlung von PrintTicket in DEVMODE oder DEVMODE für die PrintTicket-Konvertierung. Dies hängt vom jeweiligen Druck Pfad zwischen der Anwendung (Win32 oder WPF) und dem Treiber (GDI-basiert oder XPSDrv) ab. Beim Drucken von einer Windows Presentation Foundation Anwendung auf einen Microsoft XPSDrv-Druckertreiber sollte die Public-Option "pagecolormanagement" des Systems nicht im PrintTicket-oder printfunktionalitäten-Dokument angekündigt werden. in diesem Fall kann die Farbverwaltung nicht automatisch vom System behandelt werden. Das Drucken aus einer Win32-Anwendung in einen Microsoft XPSDrv-Druckertreiber kann zu einer Farbverwaltung zwischen der Anwendung und GDI führen, nach der Konvertierung in das XPS-Format gibt es jedoch keine automatische System Behandlung der Farbverwaltung zwischen dem XPS-Dokument und dem Treiber und/oder dem Gerät, da im XPS-Format jedes Element mit vollen Farbinformationen versehen wird und es dem Treiber oder dem Gerät entspricht, diese Informationen zu verarbeiten.



| Öffentliche Optionen für pagecolormanagement | DEVMODE-Wert                  |
|------------------------------------|--------------------------------|
| Keine<br/>                    | dmicmmethod \_ None<br/>   |
| Sicherungsmedium<br/>                  | dmicmmethod- \_ Gerät<br/> |
| Treiber<br/>                  | dmicmmethod- \_ Treiber<br/> |
| System<br/>                  | dmicmmethod- \_ System<br/> |



 

## <a name="pageicmrenderingintent-system-handling"></a>Pageicmrenderingintent-System Behandlung

Bei pageicmrenderingintent ermöglicht das System die automatische Behandlung von PrintTicket in DEVMODE oder DEVMODE bei Bedarf für die PrintTicket-Konvertierung. Dies hängt vom jeweiligen Druck Pfad zwischen der Anwendung (Win32 oder Windows Presentation Foundation) und dem Treiber (GDI-basiert oder XPSDrv) ab.



| Öffentliche pageicmrenderingintent-Optionen | DEVMODE-Wert                       |
|---------------------------------------|-------------------------------------|
| Absolutecolormetric<br/>       | dmicm \_ ABS \_ farbige Metrik<br/> |
| Relativecolorimetric<br/>       | idcm- \_ farbige Metrik<br/>      |
| Fotos<br/>                | dmicm- \_ Kontrast<br/>          |
| Geschäftsgrafiken<br/>           | dmicm- \_ vollständig<br/>          |



 

Alle anderen Farb Verwaltungs Schlüsselwörter (neben pagecolormanagement oder pageicmrenderingintent) weisen keine solche automatische Behandlung auf.

## <a name="joboptimaldestinationcolorprofile-and-pagedestinationcolorprofile-usage"></a>Verwendung von "joboptimaldestinationcolorprofile" und "pagedestinationcolorprofile"

Eine Anwendung kann das Printworks-Dokument für joboptimaldestinationcolorprofile Abfragen. Dadurch kann eine Anwendung mit der aktuellen Gerätekonfiguration, die im Dokument printfunktionalitäten definiert ist, das optimale Farbprofil zugewiesen werden. Wenn die Anwendung entscheidet, dass der Treiber eine Farbverwaltung für das von joboptimaldestinationcolorprofile angegebene Ziel Farbprofil ausführen soll, werden pagecolormanagement und pagedestinationcolorprofile im PrintTicket auf Driver und driverconfiguration festgelegt. Wenn die Anwendung das joboptionaldestinationcolorprofile nicht verwenden möchte und sich für die Verwendung einer eigenen Anwendung entscheidet, sollte pagecolormanagement auf None festgelegt werden. Außerdem muss pagedestinationcolorprofile auf Anwendung im PrintTicket festgelegt werden, um zu übermitteln, dass die Anwendung bereits eine Farbverwaltung für das angegebene Ziel Farbprofil ausgeführt hat. Ein anderes Szenario kann eintreten, wenn die Anwendung sich für die Verwendung des optimalen Ziel Farbprofils entscheidet, das von den Treibern Printworks zurückgegeben wurde, sich jedoch für eine eigene Farbverwaltung entscheidet. In diesem Fall ist "pagecolormanagement" auf "None" und "pagedestinationcolorprofile" auf "Application" festgelegt.

## <a name="pagesourcecolorprofile-usage"></a>Verwendung von pagesourcecolorprofile

Für pagesourcecolorprofile kann eine Anwendung unabhängig von der für pagecolormanagement ausgewählten Option ein Quell Farbprofil für jede Seite im Print Ticket angeben. Unabhängig davon, ob es vorhanden ist oder nicht, kann der Treiber das Verhalten für jeden Fall basierend auf den im Druck Schema dargestellten Definitionen festlegen. Eine Anwendung kann z. b. pagecolormanagement auf None festlegen und dann pagesourcecolorprofile nicht in PrintTicket festlegen. Es ist auch möglich, dass eine Anwendung pagecolormanagement auf den Treiber festgelegt und dann pagesourcecolorprofile in PrintTicket festgelegt hat. der Treiber ist in diesem Fall für die Bestimmung des Verhaltens in den Richtlinien von PrintSchema verantwortlich.

## <a name="pagedevicecolorspaceusage"></a>Pagede vicecolorspaceusage

Pageendvicecolorspaceusage ist ein von der Anwendung fest gelegbares XPS-spezifisches Element, das von der Anwendung festgelegt wird. Es enthält Anweisungen für das Gerät, indem die entsprechende Option im PrintTicket für die in einem XPS-Dokument zugeordnete Farb Raum Profil-Verarbeitung festgelegt wird. Die Anwendung und/oder das vorhandene PrintTicket können dieses Schlüsselwort in einem PrintTicket angeben, das an das Gerät gesendet wird. Unabhängig davon, ob es vorhanden ist oder nicht, kann der Treiber das Verhalten für jeden Fall basierend auf den im Druck Schema dargestellten Definitionen festlegen.

## <a name="print-schema-color-management-example-flow"></a>Beispiel Fluss der Druck Schema Farbverwaltung

Das folgende Diagramm veranschaulicht den Datenfluss für die wahrscheinlichsten Szenarien für die Verwendung der Farbverwaltung und des Druck Schemas. Aus Gründen der Einfachheit und Lesbarkeit wurden nur die folgenden vom benutzerkonfigurierbaren Schlüsselwörter für das Druck Schema verwendet, um ihre Verwendung zu veranschaulichen: pagecolormanagement, joboptimaldestinaioncolorprofile, pagesourcecolorprofile und pagedestinationcolorprofile. Eine durch gestrichelte Linie stellt eine Aktion dar, die auftreten soll, und eine gestrichelte Linie stellt eine Aktion dar, die auftreten kann. Das folgende Szenario stellt nicht die garantierte Interaktion dar, die sich aus der Anwendung, dem Treiber und dem System ergibt. es stellt jedoch den häufigsten Verwendungs Fall dar, der auftritt.

![ein Diagramm, das zeigt, wie Farb Verwaltungs Einstellungen verarbeitet werden](images/local-1992284846-colormanagementtest3.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




