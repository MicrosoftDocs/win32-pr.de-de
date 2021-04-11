---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 360325dc-51b5-44d5-981b-b69f7d6c82fd
title: Druck Schema-Related Technologien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8618493c2d24e8aebd7609c893d9de5a675bf24f
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104132209"
---
# <a name="print-schema-related-technologies"></a>Druck Schema-Related Technologien

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Bei den .NET Framework 3,0, Windows Vista und höheren Versionen erweitern die printfunktionen und PrintTicket-Technologien die Funktionen des Druck Schemas, um eine umfassendere Druck Funktionalität zu ermöglichen.

## <a name="printcapabilities"></a>PrintCapabilities

Die Printworks-Technologie ist eine Methode zum Veröffentlichen von Einstellungen für Benutzer steuerbare Einstellungen für auftragsspezifische Attribute und Einstellungen. Print-Funktionen werden in einem XML-Dokument (Extensible Markup Language) veröffentlicht, das das Dokument printfunktionalitäten heißt, das aus den in den Druck Schema Schlüsselwörtern und privaten Erweiterungen definierten Begriffen besteht. Das Printworks-Dokument kann als "Momentaufnahme" der vom benutzerkonfigurierbaren Status der aktuellen Gerätekonfiguration sowie eine Beschreibung möglicher Konfigurationen angesehen werden. Geräte (oder Gerätetreiber) generieren ein printfunktionalitäten-Dokument (die Momentaufnahme) Ihrer aktuellen Gruppe konfiguribarer Optionen, wenn Sie von Clients abgefragt werden. dabei kann es sich um Anwendungen oder das Druck Subsystem handeln. In diesem Dokument werden alle konfigurierbaren Print-Funktionen beschrieben, die derzeit auf dem Gerät verfügbar sind, z. b. die Optionen zum Abschließen und Seitenlayout. Das printfunktionalitäten-Dokument beschreibt explizit alle Attribute des Geräts und die zulässigen Einstellungen für jedes Attribut. Durch die Verwendung des Druck Schema-Frameworks können Geräte Attribute exakt beschrieben und effizient verglichen werden. Mithilfe der Schlüsselwörter, die im Dokument mit den Schlüsselwörtern des Druck Schemas enthalten sind, und der Struktur, die im Druck Schema Framework definiert ist, können Geräte Clients die Verwendung von printfunktionen effektiver ermöglichen. Weitere Informationen finden Sie unter [printfunktionalitäten Schema und Dokument Erstellung](printcapabilities-schema-and-document-construction.md).

Relativ zum Druck Subsystem in Microsoft Windows Server 2003 und früher ermöglicht die Printworks-Technologie den Client-und Druck subsystemkomponenten die transparente Anzeige der Informationen, die in den aktuellen printfunktionen des Win32-Systems enthalten sind. Dadurch kann der Client Print-Funktionen Abfragen, eine konsistente und gut verständliche XML-Momentaufnahme erhalten und ihn verwenden, um ein Print Ticket für ein Gerät zu erstellen, ohne die Benutzeroberfläche des Treibers aufrufen zu müssen.

## <a name="printticket"></a>PrintTicket

Die PrintTicket-Technologie ist der Nachfolger der aktuellen DEVMODE-Struktur. Es handelt sich um ein erweiterbares Markup sprach basiertes Dokument, das Informationen zur Auftrags Formatierung und zur Druckauftrags Konfiguration angibt und speichert. Eine PrintTicket-Instanz weist bestimmte Geräteeinstellungen zu und vermittelt die Benutzer Absicht. Es gibt zwei Arten von PrintTickets: generische PrintTickets, die nicht für ein bestimmtes Gerät generiert werden. und gerätespezifische PrintTickets, die für ein bestimmtes Gerät erstellt werden. Allgemeine PrintTickets, die für die Geräte übergreifende Portier barkeit vorgesehen sind, leiten ihren Inhalt ab, indem Sie Einstellungen für jedes der Geräte Attribute auswählen, die ausschließlich in den Print Schema-Schlüsselwörtern beschrieben werden. Gerätespezifische PrintTickets leiten ihren Inhalt aus einem Printworks-Dokument ab und wählen Einstellungen für jedes Geräte Attribut aus, das von diesem Dokument angekündigt wird. Diese PrintTickets können auch private Erweiterungen enthalten, die für ein Gerätemodell oder eine Gerätemodell Familie spezifisch sind. Weitere Informationen finden Sie unter [PrintTicket-Schema und Dokument Erstellung](printticket-schema-and-document-construction.md).

Relativ zum aktuellen Druck Subsystem ermöglicht die PrintTicket-Technologie, dass alle Komponenten und Clients des Druck Subsystems transparenten Zugriff auf die Informationen haben, die derzeit in den öffentlichen und privaten Teilen der DEVMODE-Struktur gespeichert sind. dabei wird ein klar definiertes XML-Format verwendet. Dieser Entwurf löst aktuelle Probleme, die bei Treiber Upgrades oder Downgrade auftreten, sowie Treiber Konfliktszenarien in Treibern, die für die PrintTicket-Technologie entwickelt wurden. Diese Szenarien können derzeit zu einem Verlust von Einstellungen und somit zu einer negativen Kundenfreundlichkeit führen. Das PrintTicket ermöglicht auch neue Szenarios, z. b. das Aktivieren eines Druckertreibers, um seine privaten DEVMODE-Einstellungen für Anwendungen und benutzerdefinierte Plug-Ins auf konsistente und eindeutige Weise verfügbar zu machen. Dies ermöglicht das Ausführen von Druckkomponenten transparenter und die Bereinigung von Einstellungs Migrationen. Die PrintTicket-Schnittstellen werden für Anwendungen über Methoden auf verwalteten Code Objekten verfügbar gemacht, die auch für Skripts verfügbar sind. Im neuen Anwendungs Framework, das auf verwalteten Code Objekten in der .NET Framework 3,0 basiert, ist das PrintTicket die Standardmethode zum Beschreiben von Dokument Einstellungen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



