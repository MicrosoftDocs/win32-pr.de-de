---
description: Erkunden Sie Druckschema-bezogene Technologien. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 360325dc-51b5-44d5-981b-b69f7d6c82fd
title: Print Schema-Related Technologies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c39d002b956fdd012a2b74a94ae0a4c58f568d8
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548787"
---
# <a name="print-schema-related-technologies"></a>Print Schema-Related Technologies

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Für .NET Framework 3.0, Windows Vista und spätere Versionen erweitern die PrintCapabilities- und PrintTicket-Technologien die Funktionen des Druckschemas, um eine vielfältigere Druckerfahrung zu ermöglichen.

## <a name="printcapabilities"></a>PrintCapabilities

Die PrintCapabilities-Technologie ist eine Methode zum Veröffentlichen von benutzersteuerbaren Einstellungsbeschreibungen für Auftragsattribute und -einstellungen. PrintCapabilities wird in einem eXtensible Markup Language (XML)-Dokument veröffentlicht, das als PrintCapabilities-Dokument bezeichnet wird und aus Begriffen besteht, die in den Schlüsselwörtern für Druckschemas und privaten Erweiterungen definiert sind. Das PrintCapabilities-Dokument kann als "Momentaufnahme" der benutzerkonfigurierbaren Zustandskonfiguration des aktuellen Geräts und als Beschreibung möglicher Konfigurationen bezeichnet werden. Geräte (oder Gerätetreiber) generieren ein PrintCapabilities-Dokument (die Momentaufnahme) ihrer aktuellen konfigurierbaren Optionen, wenn sie von Clients abgefragt werden. Dabei kann es sich entweder um Anwendungen oder um das Drucksubsystem geben. In diesem Dokument werden alle konfigurierbaren PrintCapabilities-Optionen beschrieben, die derzeit auf dem Gerät verfügbar sind, z. B. Abschlussoptionen und Seitenlayoutoptionen. Das PrintCapabilities-Dokument beschreibt explizit alle Attribute des Geräts und die zulässigen Einstellungen für jedes Attribut. Durch die Verwendung des Druckschemaframework können Geräteattribute genau beschrieben und effizient verglichen werden. Mithilfe der Schlüsselwörter im Dokument Print Schema Keywords und der im Print Schema Framework definierten Struktur können Geräte Clients ermöglichen, PrintCapabilities effektiver zu verwenden. Weitere Informationen finden Sie unter [PrintCapabilities-Schema und Dokumentkonstruktion.](printcapabilities-schema-and-document-construction.md)

Im Vergleich zum Drucksubsystem in Microsoft Windows Server 2003 und früher ermöglicht die PrintCapabilities-Technologie Client- und Drucksubsystemkomponenten, die in der aktuellen Win32-Systembinbindatei PrintCapabilities enthaltenen Informationen transparent anzeigen zu können. Dadurch kann der Client PrintCapabilities abfragen, eine konsistente und gut verständliche XML-Momentaufnahme erhalten und damit ein PrintTicket für ein Gerät erstellen, ohne die Benutzeroberfläche des Treibers aufrufen zu müssen.

## <a name="printticket"></a>PrintTicket

Die PrintTicket-Technologie ist der Nachfolger der aktuellen DEVMODE-Struktur. Es handelt sich um ein eXtensible Markup Language-basiertes Dokument, das Informationen zur Auftragsformatierung und Druckauftragskonfiguration angibt und beibehält. Eine PrintTicket-Instanz weist bestimmte Geräteeinstellungen zu und übermittelt die Absicht des Benutzers. Es gibt zwei Arten von PrintTickets: generische PrintTickets, die nicht für ein bestimmtes Gerät generiert werden. und gerätespezifische PrintTickets, die für ein bestimmtes Gerät erstellt werden. Generische PrintTickets, die geräteübergreifend portierbar sein sollen, leiten ihren Inhalt ab, indem Sie Einstellungen für jedes der Geräteattribute auswählen, die ausschließlich unter Print Schema Keywords (Schlüsselwörter für Druckschema) beschrieben werden. Gerätespezifische PrintTickets leiten ihre Inhalte von einem PrintCapabilities-Dokument ab und wählen Einstellungen für jedes Geräteattribut aus, das in diesem Dokument angekündigt wird. Diese PrintTickets können auch private Erweiterungen enthalten, die für ein Gerätemodell oder eine Gerätemodellfamilie spezifisch sind. Weitere Informationen finden Sie unter [PrintTicket Schema and Document Construction (PrintTicket-Schema und Dokumentkonstruktion).](printticket-schema-and-document-construction.md)

Im Vergleich zum aktuellen Drucksubsystem ermöglicht die PrintTicket-Technologie allen Komponenten und Clients des Drucksubsystems transparenten Zugriff auf die Informationen, die derzeit im öffentlichen und privaten Teil der DEVMODE-Struktur gespeichert sind, und verwendet dabei ein klar definiertes XML-Format. Dieser Entwurf löst aktuelle Probleme bei Treiberupgrades oder -downgrades und Treiberkonfliktszenarien in Treibern, die für die PrintTicket-Technologie entwickelt wurden. Diese Szenarien können derzeit zu einem Verlust von Einstellungen und somit zu einer negativen Kundenerfahrung führen. PrintTicket ermöglicht auch neue Szenarien, z. B. die Möglichkeit, dass ein Druckertreiber seine privaten DEVMODE-Einstellungen für Anwendungen und benutzerdefinierte Plug-Ins konsistent und eindeutig verfügbar macht. Dies ermöglicht es, Druckkomponenten transparenter zu gestalten und Einstellungsmigrationen übersichtlicher zu behandeln. Die PrintTicket-Schnittstellen werden Anwendungen über Methoden in verwalteten Codeobjekten zur Verfügung gestellt, die auch für Skripts verfügbar sind. Im neuen Anwendungsframework, das auf verwalteten Codeobjekten in .NET Framework 3.0 basiert, ist PrintTicket die Standardeinstellung zum Beschreiben von Dokumenteinstellungen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



