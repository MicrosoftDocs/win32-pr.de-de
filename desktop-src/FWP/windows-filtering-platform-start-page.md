---
title: Windows-Filterplattform
description: Windows Filtering Platform (WFP) ist ein Satz von API-und System Diensten, die eine Plattform zum Erstellen von Netzwerk Filterungs Anwendungen bereitstellen.
ms.assetid: 0436f559-20e6-4199-8391-10eb7d85df23
keywords:
- Windows-Filterplattform
- Startseite der Windows-Filter Plattform, Startseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cf63f995b44be607977dd0c70c6c91eed024e81
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "106338096"
---
# <a name="windows-filtering-platform"></a>Windows-Filterplattform

## <a name="purpose"></a>Zweck

Windows Filtering Platform (WFP) ist ein Satz von API-und System Diensten, die eine Plattform zum Erstellen von Netzwerk Filterungs Anwendungen bereitstellen. Mithilfe der WFP-API können Entwickler Code schreiben, der mit der Paketverarbeitung interagiert, die auf verschiedenen Ebenen im Netzwerkstapel des Betriebssystems erfolgt. Netzwerkdaten können gefiltert und auch geändert werden, bevor sie ihr Ziel erreichen.

Durch die Bereitstellung einer einfacheren Entwicklungsplattform ist WFP darauf ausgelegt, vorherige Paket Filterungs Technologien wie Transport Driver Interface (TDI)-Filter, Network Driver Interface Specification (NDIS)-Filter und Winsock-Schicht-Dienstanbieter (LSP) zu ersetzen. Ab Windows Server 2008 und Windows Vista sind der firewallhook und die Filter Hook-Treiber nicht verfügbar. Anwendungen, die diese Treiber verwenden, sollten stattdessen WFP verwenden.

Mit der WFP-API können Entwickler Firewalls, Angriffs Erkennungssysteme, Antivirussoftware, Netzwerk Überwachungstools und elterliche Kontrollen implementieren. WFP ist in integriert und bietet Unterstützung für Firewallfeatures, wie z. b. authentifizierte Kommunikation und dynamische Firewallkonfiguration, basierend auf der Verwendung der Sockets-API (Anwendungs basierte Richtlinie) der Anwendungen. WFP bietet auch eine Infrastruktur für die IPSec-Richtlinien Verwaltung, Änderungs Benachrichtigungen, Netzwerk Diagnose und Zustands behaftete Filterung.

Die Windows-Filter Plattform ist eine Entwicklungsplattform und keine Firewall selbst. Die Firewall-Anwendung, die in Windows Vista, Windows Server 2008 und spätere Betriebssysteme Windows-Firewall mit erweiterter Sicherheit (wfas) integriert ist, wird mithilfe von WFP implementiert. Aus diesem Grund verwenden Anwendungen, die mit der WFP-API oder der [wfas-API](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) entwickelt wurden, die gängige Filterungs Logik, die in WFP integriert ist.

Die WFP-API besteht aus einer benutzermodusapi und einer kernelmodusapi. Dieser Abschnitt enthält eine Übersicht über die gesamte WFP und beschreibt ausführlich nur den benutzermodusbereich der WFP-API. Eine ausführliche Beschreibung der kernelmoduswfp-API finden Sie in der Online Hilfe zum [Windows-Treiberkit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) .

## <a name="developer-audience"></a>Entwicklergruppe

Die Windows-Filter Plattform-API ist für die Verwendung durch Programmierer mit C/C++-Entwicklungssoftware konzipiert. Programmierer sollten mit den Netzwerk Konzepten und dem Entwurf von Systemen im Benutzermodus und im Kernel Modus vertraut sein.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Die Windows-Filter Plattform wird auf Clients unterstützt, auf denen Windows Vista und höher ausgeführt wird, sowie auf Servern unter Windows Server 2008 und höher. Informationen zu den Lauf Zeitanforderungen für ein bestimmtes Programmier Element finden Sie im Abschnitt "Anforderungen" der Referenzseite für dieses Element.





 

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                               | BESCHREIBUNG                                                                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Neues in der Windows-Filter Plattform](what-s-new-in-windows-filtering-platform.md)<br/> | Informationen zu neuen Features und APIs in der Windows-Filter Plattform.<br/>                    |
| [Informationen zur Windows-Filter Plattform](about-windows-filtering-platform.md)<br/>                 | Eine Übersicht über die Windows-Filter Plattform.<br/>                                             |
| [Verwenden der Windows-Filter Plattform](using-windows-filtering-platform.md)<br/>                 | Beispielcode, der die Windows-Filter Plattform-API verwendet. <br/>                                |
| [API-Referenz zur Windows-Filter Plattform](fwp-reference.md)<br/>                            | Dokumentation für die Funktionen, Strukturen und Konstanten der Windows-Filter Plattform.<br/> |



 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

Um Fragen zu stellen und Diskussionen zur Verwendung der WFP-API zu erhalten, besuchen Sie das [Forum Windows-Filter Plattform](https://social.msdn.microsoft.com/forums/wfp/threads/).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kernelmodusfilter für Windows-Filter Plattform-Entwurfs Handbuch](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[Kernel Modus Windows-Filter Plattform-API-Referenz](/windows-hardware/drivers/ddi/_netvista/)
</dt> <dt>

[Windows-Firewall mit erweiterter Sicherheit](/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page)
</dt> <dt>

[Erweiterbare Hilfsklasse der WFP-Diagnose](/windows/desktop/NDF/windows-filtering-platform-extensible-helper-class)
</dt> <dt>

[Winsock Secure Socket Extensions](/windows/desktop/WinSock/winsock-secure-socket-extensions)
</dt> </dl>

 

