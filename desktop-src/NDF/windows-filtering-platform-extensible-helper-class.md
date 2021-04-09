---
title: Erweiterbare Hilfsklasse der Windows-Filter Plattform
description: Die Windows-Filter Plattform (Windows Filtering Platform, WFP) enthält eine Hilfsklasse für das Netzwerk Diagnose Framework (ndf), die als Filtering Platform Helper Class (fphc) bezeichnet wird.
ms.assetid: 006ea30c-8682-4a3d-803a-73dba5162696
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858835c1a649602293ed042c13205ca982de9258
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948821"
---
# <a name="windows-filtering-platform-extensible-helper-class"></a>Erweiterbare Hilfsklasse der Windows-Filter Plattform

Die [Windows-Filter Plattform (Windows Filtering Platform, WFP)](/windows/desktop/FWP/windows-filtering-platform-start-page) enthält eine Hilfsklasse für das Netzwerk Diagnose Framework (ndf), die als Filtering Platform Helper Class (fphc) bezeichnet wird. Fphc kann helfen, die Hauptursachen von Konnektivitätsproblemen zu identifizieren, die von WFP verursacht Entwickler von Drittanbieter-Firewall können Ihre eigenen NDF-Hilfsklassen implementieren. Durch die Erweiterbarkeit von fphc können diese Hilfsklassen von Drittanbietern während der Diagnose aufgerufen werden.

In diesem Thema wird die Vertrautheit mit der [WFP-API](/windows/desktop/FWP/windows-filtering-platform-start-page)vorausgesetzt.

## <a name="why-extend-the-fphc"></a>Gründe für die Erweiterung des "f"

Alle Entwickler, die Anwendungen schreiben, die die WFP-API anrufen, sollten eine NDF-Hilfsklasse schreiben, die das fphc erweitert.

Mit "f-c" kann WFP als Ursache für ein Konnektivitätsproblem identifiziert werden. Falls verfügbar, kann der Anbieter auch den Anbieter identifizieren, der den Filter erstellt hat, der den Netzwerk Datenverkehr blockiert. Fphc übergibt diese Informationen an NDF, das wiederum den Benutzer benachrichtigen kann, dass WFP das Konnektivitätsproblem verursacht, und gibt den Namen des Anbieters an, der den Datenverkehr blockiert.

Der fphc kann dem Benutzer jedoch keine Korrekturmaßnahmen vorschlagen, und er kann nicht angeben, warum der Filter den Datenverkehr für den Benutzer blockiert. Nur eine voll qualifizierte Erweiterung kann diese Aufgaben ausführen.

Stellen Sie sich eine Drittanbieter-Firewall-Anwendung vor, die die WFP-API aufruft. Wenn die Drittanbieter-Firewall eine fphc-Erweiterung implementiert, können benutzerdefinierte Aktionen implementiert werden, um Konnektivitätsprobleme zu behandeln, die von NDF identifiziert werden. Wenn die NDF diagnostiziert, dass eine Anwendung durch die Drittanbieter-Firewall blockiert wurde, kann die f-Erweiterung das blockierende Ereignis verarbeiten. Eine Möglichkeit, dass die fphc-Erweiterung ein Ereignis verarbeiten könnte, besteht darin, dem Benutzer eine Eingabeaufforderung zum Entsperren eines Programms mithilfe der Firewall zu präsentieren und die Blockierung des Programms nach der Bestätigung des Benutzers zu deaktivieren. Alternativ kann die Dateierweiterung ein Ereignis verarbeiten, indem der Benutzer über den Grund benachrichtigt wird, warum die Anwendung blockiert wurde, z. b. Wenn eine Anwendung blockiert wurde, weil Sie von der Firewall als Schadsoftware eingestuft wurde.

## <a name="about-wfp-diagnostics"></a>Informationen zur WFP-Diagnose

Wenn NDF aufgerufen wird, um ein Netzwerkproblem zu diagnostizieren, werden Hilfsklassen kontaktiert, um die Ursache des Problems zu ermitteln. Wenn eine Hilfsklasse auf höherer Ebene feststellt, dass ein Netzwerkfehler von WFP verursacht werden kann, generiert Sie eine Hypothese für fphc basierend auf den verfügbaren Informationen. NDF übergibt diese Hypothese in Form mehrerer Ereignis Attribute an fphc. Diese Attribute werden im nachfolgenden Abschnitt " [f-Ereignis Attribute](#windows-filtering-platform-extensible-helper-class) " ausführlich beschrieben.

Ein Netzwerkproblem kann als Konnektivitätsproblem beschrieben werden, das einen bestimmten Verbindungsversuch beeinträchtigt. Beispielsweise kann es sein, dass der Benutzer versehentlich eine Anwendung blockiert hat, indem er versehentlich auf **nicht zulassen** geklickt hat. Die Firewall blockiert dann die Bindung der Anwendung an einen beliebigen Port. Der Benutzer, der nicht weiß, warum die Anwendung blockiert wird, versucht möglicherweise, das Problem über einen von der Anwendung angebotenen Einstiegspunkt zu diagnostizieren. Fphc prüft die Protokolle, und wenn eine entsprechende gefunden wird, werden die Filter-ID und die Anbieter-ID des jeweiligen Filters abgerufen. An diesem Punkt weiß fphc, wer der Besitzer dieses Filters ist, und gibt den Diagnoseprozess zur weiteren Diagnose an die entsprechende Hilfsklasse weiter.

Das letzte Ereignis in den WFP-Ereignisprotokollen, das den Attributen entspricht, wird als relevant für das Netzwerkproblem ausgewählt. Wenn keine übereinstimmenden Ereignisse gefunden werden und die Uhrzeit, zu der das Ereignis aufgetreten ist, im WFP-Protokoll abgedeckt ist, weist fphc an, dass die NDF fehlerfrei ist. Wenn keine übereinstimmenden Ereignisse gefunden werden und die Zeit, in der das Ereignis aufgetreten ist, nicht in den WFP-Protokollen enthalten ist, gibt fphc einen unbestimmten Status an NDF zurück.

Wenn ein übereinstimmendes Ereignis gefunden wird, verwendet fphc die Anbieter-ID des Filters, der bewirkt hat, dass das Ereignis den Anbieter der Sicherheitsregel identifiziert, die die Verbindung blockiert hat. Fphc überprüft dann, ob für diesen Anbieter eine hilfsklassenerweiterung vorhanden ist. Wenn ein solcher gefunden wird, generiert der Verschlüsselungs Anbieter eine Hypothese für diesen Anbieter, und die Erweiterung wird von NDF aufgerufen. Die Erweiterung sollte nützliche Diagnose-und Reparaturinformationen an den Benutzer zurückgeben.

## <a name="helper-class-registration"></a>Registrierungs Klassen Registrierung

Eine fphc-Erweiterung muss registriert werden, wie unter [Registrieren von NDF-Hilfsklassen Erweiterungen](registering-ndf-helper-class-extensions.md)beschrieben. Entwickler, die eine Hilfsklasse implementieren, müssen Ihre Erweiterungen registrieren, um sicherzustellen, dass die Erweiterung bei Bedarf von NDF aufgerufen wird. Das unten beschriebene *übereinstimmende Attribut* muss in der Registrierung unter " **HKLM \\ System \\ CurrentControlSet \\ Control \\ netdiagfx** \\ *VendorName* \\ **hostdlls** \\ *Helper Class dll* \\ **helperclasses** \\ *Helper Class Name* \\ **MatchAttribute**" gespeichert werden.

Die folgende Tabelle zeigt das passende Attribut, mit dem die Hypothese identifiziert wird, die bei der Diagnose im WFP-Ereignisprotokoll verwendet werden soll. 

| Name       | type    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                 |
|------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ProviderID | REG- \_ SZ | Der GUID der-Erweiterung. Dieser Wert muss mit der GUID des WFP-Anbieters identisch sein. <br/> Bei dieser Zeichenfolge wird die Groß-/Kleinschreibung beachtet Er sollte in der Registrierung in Großbuchstaben mit einschließenden geschweiften Klammern und Bindestrichen gespeichert werden. Beispielsweise ist {C200E360-38C5-11CE-AE62-08002B2B79EF} eine gültige ProviderID.<br/> |



 

Wenn die ProviderID eines blockierenden Filters mit der einer registrierten Hilfsklasse übereinstimmt, informiert fphc NDF, dass diese Hilfsklasse aufgerufen wird, wodurch die Diagnosefunktion von fphc erweitert wird.

## <a name="fphc-event-attributes"></a>Attribute für das Attribut "f"

In der folgenden Tabelle sind die Ereignis Attribute aufgeführt, die jedem entsprechenden Ereignis zugeordnet sind. Jedes Ereignis Attribut wird in einer [**\_ hilfsattributstruktur**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) gespeichert. Diese Attribute werden von NDF an fphc übergeben, wenn ein übereinstimmendes Ereignis gefunden wird. Diese können wiederum an fphc-Erweiterungen übermittelt werden.



| Attribut     | [**Attribut \_ Typwert**](/windows/win32/api/ndattrib/ne-ndattrib-attribute_type) | BESCHREIBUNG                                                                                                                               |
|---------------|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Anbieter-GUID | bei \_ GUID                                        | Die GUID des Anbieters, der dem Filter zugeordnet ist.                                                                                      |
| Timestamp     | bei \_ Oktett- \_ Zeichenfolge                               | Ein Puffer vom Typ FILETIME, der den Zeitpunkt angibt, zu dem das Ereignis aufgetreten ist. Dieser Zeitstempel kann verwendet werden, um ein Ereignis eindeutig zu identifizieren. |
| ipprotocol    | Unter \_ UInt32                                      | Das Transport Layer-Protokoll im Uint8-Format.                                                                                            |
| Localaddr     | bei \_ sockaddr                                    | Die lokale IP-Adresse und der Port, die in einer [**Diag- \_ sockaddr**](/windows/win32/api/ndattrib/ns-ndattrib-diag_sockaddr) -Struktur gespeichert sind.                                             |
| RemoteAddr    | bei \_ sockaddr                                    | Die Remote-IP-Adresse und der Port, die in einer [**Diag- \_ sockaddr**](/windows/win32/api/ndattrib/ns-ndattrib-diag_sockaddr) -Struktur gespeichert sind.                                            |
| userId        | bei \_ Oktett- \_ Zeichenfolge                               | Ein Puffer vom Typ sid, der die UserID darstellt. Wenn die UserID eine Länge von 0 hat, ist die SID nicht verfügbar.                                        |
| appId         | bei \_ Zeichenfolge                                      | Ein Puffer, in dem der abgerufene Anwendungs Bezeichner gespeichert wird. Wenn AppID den Wert L "" hat, ist der Anwendungs Bezeichner nicht verfügbar.        |



 

## <a name="handling-fphc-events"></a>Behandeln von Ereignis Ereignissen

Bevor dem Benutzer Diagnose-und Reparaturinformationen vorgeschlagen werden, sollte eine fphc-Erweiterung mehr Daten erfassen, als von den fphc-Benachrichtigungen bereitgestellt werden. Diese Daten können über die [WFP-Ereignis Verwaltungsfunktionen](/windows/desktop/FWP/fwp-mgmt-functions)abgerufen werden. Diese Funktionen werden im Beispiel zum [Anzeigen von NET-Ereignissen](/windows/desktop/FWP/displaying-net-events) veranschaulicht.

Ein ausführlicheres Ereignis Verwaltungs Beispiel ist im SDK enthalten. Den Quellcode für das Beispiel finden Sie im SDK-Installationsverzeichnis unter C: \\ Program Files \\ Microsoft SDKs \\ Windows \\ <version number> \\ Samples \\ netds \\ WFP \\ diagevents. Das Windows Vista SDK ist im [Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)verfügbar.

## <a name="built-in-fphc-diagnostics"></a>Integrierte f-Diagnose

Wenn keine "f"-Erweiterung vorhanden ist, kann "f" die unten aufgeführten Szenarien diagnostizieren. Die meisten Konnektivitätsprobleme, die von einem fehlerhaften Gerät diagnostiziert werden, treten auf Die IPSec-Szenarien sind weniger häufig.

In der folgenden Tabelle werden einige Szenarien angezeigt, die Verbindungsfehler verursachen, die von fphc diagnostiziert werden können, sowie die an NDF übergebenen Beschreibungen und Reparaturinformationen.



| Szenario                   | Beschreibung der unteren Integrität                                                                                                               | Reparaturinformationen                   |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| Firewalldrop              | Die Verbindung wird durch die Firewalleinstellungen auf diesem Computer blockiert.                                                                  | Überprüfen Sie die Firewalleinstellungen.       |
| Hauptmodusfehler          | Aufgrund eines Konflikts mit der IPSec-Sicherheitsrichtlinie kann keine Verbindung hergestellt werden.                                                                     | Wenden Sie sich an den IPSec-Richtlinien Besitzer.      |
| Schnellmodusfehler         | Aufgrund eines Konflikts mit der IPSec-Sicherheitsrichtlinie kann keine Verbindung hergestellt werden.                                                                     | Wenden Sie sich an den IPSec-Richtlinien Besitzer.      |
| Benutzermodusfehler          | Aufgrund eines Konflikts mit der IPSec-Sicherheitsrichtlinie kann keine Verbindung hergestellt werden.                                                                     | Wenden Sie sich an den IPSec-Richtlinien Besitzer.      |
| Fehler bei Anmelde Informationen         | Sie können keine Verbindung herstellen, da die Stamm Zertifizierungsstelle auf diesem Computer nicht der Stamm Zertifizierungsstelle auf dem Remote Computer entspricht. | Aktualisieren Sie das vertrauenswürdige Stamm Zertifikat. |
| Abgelaufenes Zertifikat        | Das für die IPSec-Authentifizierung verwendete Zertifikat ist abgelaufen.                                                                           | Fordern Sie ein Zertifikat an.               |
| Andere Zertifikat Fehler | Ein gültiges Zertifikat für die IPSec-Authentifizierung wurde nicht gefunden.                                                                          | Fordern Sie ein Zertifikat an.               |
| Kerberos-Fehler           | Der Computer ist nicht Teil dieser Domäne.                                                                                             | Fügen Sie den Computer einer Domäne hinzu.      |
| Vorinstaltzter Schlüssel              | Setzt die vorinstallierten Schlüssel zurück.                                                                                                            | Setzt die vorinstallierten Schlüssel zurück.            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Filterplattform](/windows/desktop/FWP/windows-filtering-platform-start-page)
</dt> <dt>

[Entwerfen von NDF-Hilfsklassen Erweiterungen](designing-ndf-helper-class-extensions.md)
</dt> <dt>

[Registrieren von NDF-Hilfsklassen Erweiterungen](registering-ndf-helper-class-extensions.md)
</dt> <dt>

[Beispiele für die NDF-Hilfsklasse](ndf-helper-class-examples.md)
</dt> </dl>

 

