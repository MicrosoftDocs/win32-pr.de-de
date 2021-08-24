---
title: Windows-Filterplattform
description: Windows Filterplattform (WFP) ist eine Reihe von API- und Systemdiensten, die eine Plattform zum Erstellen von Netzwerkfilteranwendungen bereitstellen.
ms.assetid: 0436f559-20e6-4199-8391-10eb7d85df23
keywords:
- Windows-Filterplattform
- Windows Startseite der Filterplattform,Startseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9c1f0e412426dd2bae7e5861d3b328d4e285c303aef046970e725a02965b974
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766490"
---
# <a name="windows-filtering-platform"></a>Windows-Filterplattform

## <a name="purpose"></a>Zweck

Windows Filterplattform (WFP) ist eine Reihe von API- und Systemdiensten, die eine Plattform zum Erstellen von Netzwerkfilteranwendungen bereitstellen. Mithilfe der WFP-API können Entwickler Code schreiben, der mit der Paketverarbeitung interagiert, die auf verschiedenen Ebenen im Netzwerkstapel des Betriebssystems erfolgt. Netzwerkdaten können gefiltert und auch geändert werden, bevor sie ihr Ziel erreichen.

Durch die Bereitstellung einer einfacheren Entwicklungsplattform ist WFP so konzipiert, dass frühere Paketfiltertechnologien wie Transport Driver Interface (TDI)-Filter, NDIS-Filter (Network Driver Interface Specification) und Winsock Layered Service Providers (LSP) ersetzt werden. Ab Windows Server 2008 und Windows Vista sind der Firewallhook und die Filterhooktreiber nicht verfügbar. -Anwendungen, die diese Treiber verwendet haben, sollten stattdessen WFP verwenden.

Mit der WFP-API können Entwickler Firewalls, Angriffserkennungssysteme, Antivirenprogramme, Netzwerküberwachungstools und Jugendschutz implementieren. WFP ist in integriert und bietet Unterstützung für Firewallfeatures wie authentifizierte Kommunikation und dynamische Firewallkonfiguration basierend auf der Verwendung der Sockets-API (anwendungsbasierte Richtlinie) durch Anwendungen. WFP bietet auch Infrastruktur für IPsec-Richtlinienverwaltung, Änderungsbenachrichtigungen, Netzwerkdiagnose und zustandsbehaftete Filterung.

Windows Die Filterplattform ist eine Entwicklungsplattform und keine Firewall selbst. Die Firewallanwendung, die in Windows Vista, Windows Server 2008 und höheren Betriebssystemen Windows Firewall mit erweiterter Sicherheit (WFAS) integriert ist, wird mithilfe von WFP implementiert. Daher verwenden Anwendungen, die mit der WFP-API oder der [WFAS-API](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) entwickelt wurden, die in WFP integrierte gemeinsame Filterverfahrenslogik.

Die WFP-API besteht aus einer Benutzermodus-API und einer Kernelmodus-API. Dieser Abschnitt bietet eine Übersicht über das gesamte WFP und beschreibt im Detail nur den Benutzermodusteil der WFP-API. Eine ausführliche Beschreibung der Kernelmodus-WFP-API finden Sie in der [Onlinehilfe Windows Driver Kit.](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)

## <a name="developer-audience"></a>Entwicklergruppe

Die Windows Filtering Platform-API ist für die Verwendung durch Programmierer mit C/C++-Entwicklungssoftware konzipiert. Programmierer sollten mit Netzwerkkonzepten und dem Entwurf von Systemen vertraut sein, die Benutzermodus- und Kernelmoduskomponenten verwenden.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Die Windows Filterplattform wird auf Clients mit Windows Vista und höher und auf Servern mit Windows Server 2008 und höher unterstützt. Informationen zu den Laufzeitanforderungen für ein bestimmtes Programmierelement finden Sie im Abschnitt Anforderungen der Referenzseite für dieses Element.





 

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                               | Beschreibung                                                                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Neuerungen bei Windows Filterplattform](what-s-new-in-windows-filtering-platform.md)<br/> | Informationen zu neuen Features und APIs in Windows Filterplattform.<br/>                    |
| [Informationen Windows Filterplattform](about-windows-filtering-platform.md)<br/>                 | Eine Übersicht über Windows Filterplattform.<br/>                                             |
| [Verwenden Windows Filterplattform](using-windows-filtering-platform.md)<br/>                 | Beispielcode mithilfe der Windows Filtering Platform-API. <br/>                                |
| [Windows Referenz zur Filterplattform-API](fwp-reference.md)<br/>                            | Dokumentation für die Windows Funktionen, Strukturen und Konstanten der Filterplattform.<br/> |



 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

Um Fragen zu stellen und Diskussionen zur Verwendung der WFP-API zu führen, besuchen Sie das [Windows Filtering Platform Forum](https://social.msdn.microsoft.com/forums/wfp/threads/).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kernelmodus Windows Filterplattform-API – Entwurfshandbuch](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[Kernelmodus Windows Filterplattform-API – Referenz](/windows-hardware/drivers/ddi/_netvista/)
</dt> <dt>

[Windows-Firewall mit erweiterter Sicherheit](/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page)
</dt> <dt>

[WFP Diagnostics Extensible Helper-Klasse](/windows/desktop/NDF/windows-filtering-platform-extensible-helper-class)
</dt> <dt>

[Winsock Secure Socket-Erweiterungen](/windows/desktop/WinSock/winsock-secure-socket-extensions)
</dt> </dl>

 

