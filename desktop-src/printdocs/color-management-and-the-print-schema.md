---
description: Erfahren Sie mehr über benutzerkonfigurierbare Schlüsselwörter im Druckschema für die Farbverwaltung, z. B. PageColorManagement und PageBlackGenerationProcessing.
ms.assetid: 296255b8-fe5c-46dd-b717-487aaae0db80
title: Farbverwaltung und das Druckschema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9258d9dcc59ab24f9cfca8e170bf3f3f62841b21
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409673"
---
# <a name="color-management-and-the-print-schema"></a>Farbverwaltung und das Druckschema

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Benutzerkonfigurierbare Elementschlüsselwörter können xps-spezifisch oder nicht XPS-spezifisch sein. Falls sie nicht XPS-spezifisch sind, kann das Schlüsselwort für legacy-GDI-basiertes Drucken verwendet werden. Wenn eine Anwendung beschließt, diese Schlüsselwörter in einem PrintTicket festzulegen, liegt es in der Verantwortung des Treibers, die richtige Aktion und das richtige Verhalten basierend auf den definitionen zu bestimmen, die im Druckschema dargestellt werden. Jedes dieser Schlüsselwörter kann im Kontext von ICM verwendet werden. Weitere Informationen finden Sie im Windows Vista SDK.



| Vom Benutzer konfigurierbares Schlüsselwort "Print Schema"       | DEVMODE-Entsprechung     | XPS-spezifisch   |
|----------------------------------------------|------------------------|----------------|
| PageColorManagement<br/>               | dmICMMethod<br/> | Nein<br/>  |
| PageBlackGenerationProcessing<br/>     | Keine<br/>        | Ja<br/> |
| PageBlendColorSpace<br/>               | Keine<br/>        | Ja<br/> |
| PageSourceColorProfile<br/>            | Keine<br/>        | Nein<br/>  |
| PageDestinationColorProfile<br/>       | Keine<br/>        | Nein<br/>  |
| PageICMRenderingIntent<br/>            | dmICMIntent<br/> | Nein<br/>  |
| JobOptimalDestinationColorProfile<br/> | Keine<br/>        | Nein<br/>  |
| PageDeviceColorSpaceUsage<br/>         | Keine<br/>        | Ja<br/> |



 

## <a name="pagecolormanagement-system-handling"></a>PageColorManagement-Systembehandlung

Für PageColorManagement ermöglicht das System bei Bedarf die automatische Verarbeitung der Konvertierung von PrintTicket in DEVMODE oder DEVMODE in PrintTicket. Dies hängt vom spezifischen Druckpfad zwischen der Anwendung (Win32 oder WPF) und dem Treiber (GDI-basiert oder XPSDrv) ab. Beim Drucken von einer Windows Presentation Foundation-Anwendung in einen Microsoft XPSDrv-Druckertreiber sollte eine öffentliche PageColorManagement-Option von System NICHT im PrintTicket- oder PrintCapabilities-Dokument angekündigt werden. In diesem Fall kann die Farbverwaltung nicht automatisch vom System ausgeführt werden. Das Drucken aus einer Win32-Anwendung in einen Microsoft XPSDrv-Druckertreiber kann zu einer Farbverwaltung zwischen der Anwendung und GDI führen. Nach der Konvertierung in das XPS-Format erfolgt jedoch keine automatische Systembehandlung der Farbverwaltung zwischen dem XPS-Dokument und dem Treiber und/oder Gerät, da das XPS-Format jedes Element mit vollständigen Farbinformationen markiert und es dem Treiber oder dem Gerät ob liegt, diese Informationen zu verarbeiten.



| PageColorManagement – Öffentliche Optionen | DEVMODE-Wert                  |
|------------------------------------|--------------------------------|
| Keine<br/>                    | DMICMMETHOD \_ NONE<br/>   |
| Gerät<br/>                  | DMICMMETHOD-GERÄT \_<br/> |
| Treiber<br/>                  | DMICMMETHOD-TREIBER \_<br/> |
| System<br/>                  | DMICMMETHOD-SYSTEM \_<br/> |



 

## <a name="pageicmrenderingintent-system-handling"></a>PageICMRenderingIntent-Systembehandlung

Für PageICMRenderingIntent ermöglicht das System bei Bedarf die automatische Verarbeitung von PrintTicket in DEVMODE oder DEVMODE in die PrintTicket-Konvertierung. Dies hängt vom spezifischen Druckpfad zwischen der Anwendung (Win32 oder Windows Presentation Foundation) und dem Treiber (GDI-basiert oder XPSDrv) ab.



| PageICMRenderingIntent Öffentliche Optionen | DEVMODE-Wert                       |
|---------------------------------------|-------------------------------------|
| AbsoluteColorimetric<br/>       | DMICM \_ ABS \_ COLORIMETRIC<br/> |
| RelativeColorimetric<br/>       | DMICM \_ COLORIMETRIC<br/>      |
| Fotos<br/>                | DMICM-KONTRAST \_<br/>          |
| BusinessGraphics<br/>           | DMICM \_ SATURATE<br/>          |



 

Alle anderen Schlüsselwörter im Zusammenhang mit der Farbverwaltung (außer PageColorManagement oder PageICMRenderingIntent) verfügen nicht über eine solche automatische Behandlung.

## <a name="joboptimaldestinationcolorprofile-and-pagedestinationcolorprofile-usage"></a>Verwendung von JobOptimalDestinationColorProfile und PageDestinationColorProfile

Eine Anwendung KANN das PrintCapabilities-Dokument für JobOptimalDestinationColorProfile abfragen. Dadurch könnte eine Anwendung das optimale Farbprofil erhalten, wenn die aktuelle Gerätekonfiguration wie im PrintCapabilities-Dokument definiert ist. Wenn die Anwendung entscheidet, dass der Treiber die Farbverwaltung für das zielfarbene Profil durchführen soll, das von JobOptimalDestinationColorProfile angegeben wird, werden PageColorManagement und PageDestinationColorProfile im PrintTicket auf Driver bzw. DriverConfiguration festgelegt. Wenn die Anwendung das JobOptionalDestinationColorProfile nicht verwenden möchte und ein eigenes verwendet, sollte pageColorManagement auf None festgelegt werden. Außerdem sollte pageDestinationColorProfile im PrintTicket auf Anwendung festgelegt werden, um zu vermitteln, dass die Anwendung bereits eine Farbverwaltung für das angegebene Zielfarbprofil durchgeführt hat. Ein anderes Szenario kann auftreten, wenn die Anwendung das optimale Zielfarbprofil verwendet, das von den PrintCapabilities-Treibern zurückgegeben wird, sich aber für die Farbverwaltung selbst entscheidet. In diesem Fall wird PageColorManagement auf None und PageDestinationColorProfile auf Application festgelegt.

## <a name="pagesourcecolorprofile-usage"></a>PageSourceColorProfile-Verwendung

Für PageSourceColorProfile kann eine Anwendung ein Quellfarbprofil für jede Seite im PrintTicket angeben, unabhängig von der für PageColorManagement ausgewählten Option. Unabhängig davon, ob es vorhanden ist oder nicht, muss der Treiber das Verhalten für jeden Fall basierend auf den Definitionen im Druckschema festlegen. Beispielsweise kann eine Anwendung PageColorManagement auf None und dann nicht PageSourceColorProfile im PrintTicket festlegen. Es ist auch möglich, dass eine Anwendung PageColorManagement auf Driver und dann PageSourceColorProfile im PrintTicket festgelegt hat. In diesem Fall ist der Treiber dafür verantwortlich, das Verhalten innerhalb der Richtlinien von PrintSchema zu bestimmen.

## <a name="pagedevicecolorspaceusage"></a>PageDeviceColorSpaceUsage

PageDeviceColorSpaceUsage ist ein XPS-spezifisches benutzerkonfigurierbares Element, das von der Anwendung festgelegt wird. Es enthält Anweisungen für das Gerät, indem die entsprechende Option im PrintTicket für die Behandlung von Farbraumprofilen innerhalb eines XPS-Dokuments eingestellt wird. Die Anwendung und/oder das vorhandene PrintTicket können dieses Schlüsselwort in einem printTicket angeben, das an das Gerät gesendet wird. Unabhängig davon, ob es vorhanden ist oder nicht, muss der Treiber das Verhalten für jeden Fall basierend auf den Definitionen im Druckschema festlegen.

## <a name="print-schema-color-management-example-flow"></a>Beispielablauf für die Farbverwaltung des Druckschemas

Das folgende Diagramm veranschaulicht den Ablauf für die wahrscheinlichsten Szenarien für die Verwendung der Farbverwaltung und des Druckschemas. Der Einfachheit und Lesbarkeit halber wurden nur die folgenden benutzerkonfigurierbaren Print Schema-Schlüsselwörter verwendet, um ihre Verwendung zu veranschaulichen: PageColorManagement, JobOptimalDesoptimionColorProfile, PageSourceColorProfile und PageDestinationColorProfile. Eine durchstrichene Linie stellt eine Aktion dar, die AUFTRETEN SOLLTE, und eine gestrichelte Linie stellt eine Aktion dar, die auftreten kann. Das folgende Szenario ist nicht die garantierte Interaktion, die zwischen Anwendung, Treiber und System entsteht. Es stellt jedoch den häufigsten Anwendungsfall dar, der eintritt.

![Diagramm zur Verarbeitung von Farbverwaltungseinstellungen](images/local-1992284846-colormanagementtest3.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




