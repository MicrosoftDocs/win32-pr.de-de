---
title: Windows Filtering Platform Extensible Helper Class
description: Die Windows Filtering Platform (WFP) enthält eine Hilfsklasse des Network Diagnostics Framework (NDF), die als Filtering Platform Helper Class (FPHC) bezeichnet wird.
ms.assetid: 006ea30c-8682-4a3d-803a-73dba5162696
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff972beffebb44b33eb68a0439193307639522738ac1f8766845404c03d3cd9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065210"
---
# <a name="windows-filtering-platform-extensible-helper-class"></a>Windows Filtering Platform Extensible Helper Class

Die [Windows Filtering Platform (WFP)](/windows/desktop/FWP/windows-filtering-platform-start-page) enthält eine NDF-Hilfsklasse (Network Diagnostics Framework), die als Filtering Platform Helper Class (FPHC) bezeichnet wird. FPHC kann dabei helfen, die Grundursachen von Konnektivitätsproblemen zu identifizieren, die durch WFP verursacht werden. Firewallentwickler von Drittanbietern können ihre eigenen NDF-Hilfsklassen implementieren. Die FPHC-Erweiterbarkeit ermöglicht es, diese Hilfsklassen von Drittanbietern während der Diagnose aufzurufen.

In diesem Thema wird vorausgesetzt, dass Sie mit der [WFP-API](/windows/desktop/FWP/windows-filtering-platform-start-page)vertraut sind.

## <a name="why-extend-the-fphc"></a>Gründe für die Erweiterung des FPHC

Alle Entwickler, die Anwendungen schreiben, die die WFP-API aufrufen, sollten eine NDF-Hilfsklasse schreiben, die FPHC erweitert.

FPHC kann WFP als Ursache eines Konnektivitätsproblems identifizieren. Falls verfügbar, kann FPHC auch den Anbieter identifizieren, der den Filter erstellt hat, der den Netzwerkdatenverkehr blockiert. FPHC übergibt diese Informationen an NDF, die wiederum den Benutzer benachrichtigen kann, dass WFP das Konnektivitätsproblem verursacht, und den Namen des Anbieters geben kann, der den Datenverkehr blockiert.

Der FPHC kann dem Benutzer jedoch keine Korrekturmaßnahmen vorschlagen und auch nicht den Grund angeben, warum der Filter den Datenverkehr für den Benutzer blockiert. Nur eine FPHC-Erweiterung kann diese Aufgaben ausführen.

Betrachten Sie eine Firewallanwendung eines Drittanbieters, die die WFP-API aufruft. Wenn die Firewall eines Drittanbieters eine FPHC-Erweiterung implementiert, können benutzerdefinierte Aktionen implementiert werden, um Konnektivitätsprobleme zu behandeln, die von NDF identifiziert werden. Wenn NDF diagnostiziert, dass eine Anwendung durch die Firewall eines Drittanbieters blockiert wurde, kann die FPHC-Erweiterung das Blockierungsereignis behandeln. Eine Möglichkeit, mit der die FPHC-Erweiterung ein Ereignis behandeln kann, besteht darin, dem Benutzer eine Eingabeaufforderung zum Aufheben der Blockierung eines Programms mithilfe der Firewall zu zeigen und das Programm dann nach der Benutzerbestätigung zu entsperren. Alternativ kann die FPHC-Erweiterung ein Ereignis behandeln, indem sie den Benutzer über den Grund informiert, warum die Anwendung blockiert wurde, z. B. dass eine Anwendung blockiert wurde, da sie von der Firewall als Schadsoftware angesehen wurde.

## <a name="about-wfp-diagnostics"></a>Informationen zur WFP-Diagnose

Wenn NDF aufgerufen wird, um ein Netzwerkproblem zu diagnostizieren, werden Hilfsklassen kontaktiert, um die Ursache des Problems zu ermitteln. Wenn eine Hilfsklasse auf höherer Ebene feststellt, dass ein Netzwerkfehler durch WFP verursacht werden kann, generiert sie basierend auf verfügbaren Informationen eine Hypothese für FPHC. NDF übergibt diese Hypothese in Form mehrerer Ereignisattribute an FPHC. Diese Attribute werden unten im Abschnitt [FPHC-Ereignisattribute](#windows-filtering-platform-extensible-helper-class) ausführlich beschrieben.

Ein Netzwerkproblem kann als Konnektivitätsproblem beschrieben werden, das sich auf einen bestimmten Verbindungsversuch auswirkt. Beispielsweise hat der Benutzer eine Anwendung möglicherweise versehentlich blockiert, indem er versehentlich auf **Nicht zulassen** klickt. Die Firewall blockiert dann die Bindung der Anwendung an einen beliebigen Port. Der Benutzer weiß nicht, warum die Anwendung blockiert ist, kann versuchen, das Problem über einen einstiegspunkt zu diagnostizieren, der von der Anwendung angeboten wird. FPHC untersucht die Protokolle, und wenn eine Übereinstimmung gefunden wird, werden die Filter-ID und die Anbieter-ID des jeweiligen Filters abgerufen. An diesem Punkt weiß FPHC, wer der Besitzer dieses Filters ist, und übergibt den Diagnoseprozess zur weiteren Diagnose an die entsprechende Hilfsklasse.

Das letzte Ereignis in den WFP-Ereignisprotokollen, das den Attributen entspricht, wird als relevant für das Netzwerkproblem ausgewählt. Wenn keine übereinstimmenden Ereignisse gefunden werden und der Zeitpunkt, zu dem das Ereignis eingetreten ist, im WFP-Protokoll abgedeckt wird, gibt FPHC NDF an, dass es fehlerfrei ist. Wenn keine übereinstimmenden Ereignisse gefunden werden und die WFP-Protokolle nicht den Zeitpunkt des Ereignisses enthalten, gibt FPHC einen unbestimmten Status an NDF zurück.

Wenn ein übereinstimmendes Ereignis gefunden wird, verwendet FPHC die Anbieter-ID des Filters, der dazu geführt hat, dass das Ereignis den Anbieter der Sicherheitsregel identifiziert, die die Konnektivität blockiert hat. FPHC überprüft dann, ob eine Hilfsklassenerweiterung für diesen Anbieter vorhanden ist. Wenn eine gefunden wird, generiert FPHC eine Hypothese für diesen Anbieter, und dann ruft NDF die Erweiterung auf. Die Erweiterung sollte hilfreiche Diagnose- und Reparaturinformationen an den Benutzer zurückgeben.

## <a name="helper-class-registration"></a>Hilfsklassenregistrierung

Eine FPHC-Erweiterung muss wie unter [Registrieren von NDF-Hilfsklassenerweiterungen](registering-ndf-helper-class-extensions.md)beschrieben registriert werden. Entwickler, die eine Hilfsklasse implementieren, müssen ihre Erweiterungen registrieren, um sicherzustellen, dass die Erweiterung bei Bedarf von NDF aufgerufen wird. Das unten beschriebene *übereinstimmende Attribut* muss in der Registrierung unter **HKLM \\ System \\ CurrentControlSet \\ Control \\ NetDiagFx** \\ *VendorName* \\ **HostDLLs** \\ *Helper Class DLL* \\ **HelperClasses** \\ *Helper Class Name* \\ **MatchAttributes** gespeichert werden.

Die folgende Tabelle zeigt das übereinstimmende Attribut, das verwendet wird, um die Hypothese zu identifizieren, die in der Diagnose im WFP-Ereignisprotokoll verwendet werden soll. 

| Name       | type    | Beschreibung                                                                                                                                                                                                                                                                                                 |
|------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ProviderID | REG \_ SZ | Die GUID der FPHC-Erweiterung. Dieser Wert muss mit der WFP-Anbieter-GUID identisch sein. <br/> Bei dieser Zeichenfolge wird die Groß-/Kleinschreibung beachtet. Sie sollte in der Registrierung in Großbuchstaben mit einschließenden Klammern und Bindestrichen gespeichert werden. {C200E360-38C5-11CE-AE62-08002B2B79EF} ist beispielsweise eine gültige ProviderID.<br/> |



 

Wenn die ProviderID eines blockierenden Filters mit der einer registrierten Hilfsklasse übereinstimmt, informiert FPHC NDF, diese Hilfsklasse aufzurufen und so die Diagnosefunktion von FPHC zu erweitern.

## <a name="fphc-event-attributes"></a>FPHC-Ereignisattribute

In der folgenden Tabelle sind die Ereignisattribute aufgeführt, die jedem übereinstimmenden Ereignis zugeordnet sind. Jedes Ereignisattribut wird in einer [**HELPER \_ ATTRIBUTE-Struktur**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) gespeichert. Diese Attribute werden von NDF an FPHC übergeben, wenn ein übereinstimmendes Ereignis gefunden wird. Diese können wiederum an FPHC-Erweiterungen übergeben werden.



| attribute     | [**ATTRIBUTE \_ TYPE-Wert**](/windows/win32/api/ndattrib/ne-ndattrib-attribute_type) | Beschreibung                                                                                                                               |
|---------------|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Anbieter-GUID | AT \_ GUID                                        | Die GUID des Anbieters, der dem Filter zugeordnet ist.                                                                                      |
| Timestamp     | AT \_ OCTET \_ STRING                               | Ein Puffer vom Typ FILETIME, der den Zeitpunkt angibt, zu dem das Ereignis aufgetreten ist. Dieser Zeitstempel kann verwendet werden, um ein Ereignis eindeutig zu identifizieren. |
| ipProtocol    | AT \_ UINT32                                      | Das Transportschichtprotokoll im UINT8-Format.                                                                                            |
| LocalAddr     | AT \_ SOCKADDR                                    | Die lokale IP-Adresse und der Port, die in einer [**\_ DIAG-SOCKADDR-Struktur**](/windows/win32/api/ndattrib/ns-ndattrib-diag_sockaddr) gespeichert sind.                                             |
| RemoteAddr    | AT \_ SOCKADDR                                    | Die Remote-IP-Adresse und der Port, die in einer [**\_ DIAG-SOCKADDR-Struktur**](/windows/win32/api/ndattrib/ns-ndattrib-diag_sockaddr) gespeichert sind.                                            |
| userId        | AT \_ OCTET \_ STRING                               | Ein Puffer vom Typ SID, der die userid darstellt. Wenn userId die Länge 0 hat, ist die SID nicht verfügbar.                                        |
| appId         | AT \_ STRING                                      | Ein Puffer, der den abgerufenen Anwendungsbezeichner speichert. Wenn appId den Wert L" hat, ist der Anwendungsbezeichner nicht verfügbar.        |



 

## <a name="handling-fphc-events"></a>Behandeln von FPHC-Ereignissen

Bevor dem Benutzer Diagnose- und Reparaturinformationen vorgeschlagen werden, sollte eine FPHC-Erweiterung mehr Daten sammeln, als von den FPHC-Benachrichtigungen bereitgestellt werden. Diese Daten können von den [WFP-Ereignisverwaltungsfunktionen](/windows/desktop/FWP/fwp-mgmt-functions)bezogen werden. Diese Funktionen werden im Beispiel [Anzeigen von Net Events](/windows/desktop/FWP/displaying-net-events) veranschaulicht.

Ein ausführlicheres Ereignisverwaltungsbeispiel ist im SDK enthalten. Den Quellcode für das Beispiel finden Sie im SDK-Installationspfad unter C: \\ \\ Programme Microsoft SDKs Windows Samples \\ \\ <version number> \\ \\ NetDs \\ WFP \\ DiagEvents. Das Windows Vista SDK ist im [Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)verfügbar.

## <a name="built-in-fphc-diagnostics"></a>Integrierte FPHC-Diagnose

Wenn keine FPHC-Erweiterung vorhanden ist, kann FPHC die unten aufgeführten Szenarien diagnostizieren. Die meisten konnektivitätsfehler, die von FPHC diagnostiziert werden, treten auf, weil Firewalls den Datenverkehr blockieren. Die IPsec-Szenarien sind weniger häufig.

Die folgende Tabelle zeigt einige Szenarien, die Konnektivitätsfehler verursachen, die von FPHC diagnostiziert werden können, zusammen mit der Beschreibung und den Reparaturinformationen, die an NDF übergeben werden.



| Szenario                   | Beschreibung der niedrigen Integrität                                                                                                               | Reparaturinformationen                   |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| Firewall löschen              | Die Firewalleinstellungen auf diesem Computer blockieren die Verbindung.                                                                  | Überprüfen Sie Ihre Firewalleinstellungen.       |
| Hauptmodusfehler          | Eine Verbindung kann aufgrund eines IPsec-Sicherheitsrichtlinienkonflikts nicht hergestellt werden.                                                                     | Wenden Sie sich an den IPsec-Richtlinienbesitzer.      |
| Fehler im Schnellmodus         | Eine Verbindung kann aufgrund eines IPsec-Sicherheitsrichtlinienkonflikts nicht hergestellt werden.                                                                     | Wenden Sie sich an den IPsec-Richtlinienbesitzer.      |
| Fehler im Benutzermodus          | Eine Verbindung kann aufgrund eines IPsec-Sicherheitsrichtlinienkonflikts nicht hergestellt werden.                                                                     | Wenden Sie sich an den IPsec-Richtlinienbesitzer.      |
| Fehler bei Anmeldeinformationen         | Sie können keine Verbindung herstellen, da die Stammzertifizierungsstelle auf diesem Computer nicht mit der Stammzertifizierungsstelle auf dem Remotecomputer übereinstimmt. | Aktualisieren Sie das vertrauenswürdige Stammzertifikat. |
| Abgelaufenes Zertifikat        | Das für die IPsec-Authentifizierung verwendete Zertifikat ist abgelaufen.                                                                           | Fordern Sie ein Zertifikat an.               |
| Andere Zertifikatfehler | Für die IPsec-Authentifizierung wurde kein gültiges Zertifikat gefunden.                                                                          | Fordern Sie ein Zertifikat an.               |
| Kerberos-Fehler           | Der Computer ist nicht Teil dieser Domäne.                                                                                             | Verbinden Sie diesen Computer mit einer Domäne.      |
| Vorinstallierte Schlüssel              | Setzen Sie die vorinstallierten Schlüssel zurück.                                                                                                            | Setzen Sie die vorinstallierten Schlüssel zurück.            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Filterplattform](/windows/desktop/FWP/windows-filtering-platform-start-page)
</dt> <dt>

[Entwerfen von NDF-Hilfsklassenerweiterungen](designing-ndf-helper-class-extensions.md)
</dt> <dt>

[Registrieren von NDF-Hilfsklassenerweiterungen](registering-ndf-helper-class-extensions.md)
</dt> <dt>

[Beispiele für die NDF-Hilfsklasse](ndf-helper-class-examples.md)
</dt> </dl>

 

