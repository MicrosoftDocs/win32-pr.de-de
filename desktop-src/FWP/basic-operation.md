---
title: WFP-Vorgang
description: Windows Die Filterplattform (WFP) führt ihre Aufgaben aus, indem die folgenden grundlegenden Entitäten Layer, Filters, Shims und Callouts integriert werden.
ms.assetid: bf88ace7-1160-434b-9be0-3f9db6aa2e87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8254ed468b856392477a643ce13f2b609245031f7363865b8c93ccfda64ba9fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015388"
---
# <a name="wfp-operation"></a>WFP-Vorgang

Windows Die Filterplattform (WFP) führt ihre Aufgaben aus, indem die folgenden grundlegenden Entitäten integriert werden: *Ebenen,* *Filter,* *Shims* und *Callouts*.

## <a name="layers"></a>Ebenen

Eine *Ebene ist* ein Container, der von der Filter-Engine verwaltet wird, deren Funktion das Organisieren von Filtern in Sätzen ist. Eine Ebene ist kein Modul im Netzwerkstapel. Jede Ebene verfügt über ein Schema, das den Typ der Filter definiert, die ihr hinzugefügt werden können. Weitere [Informationen finden Sie unter Verfügbare Filterbedingungen auf](filtering-conditions-available-at-each-filtering-layer.md) jeder Filterebene.

Ebenen können Unterebenen enthalten, um in Konflikt stehende Filteranforderungen zu verwalten, z. B. "TCP-Ports über 1024 blockieren" und "Port 1080 öffnen". Die Regeln für die Verwaltung von Filterkonflikten werden durch [Filterschlichtung bestimmt.](filter-arbitration.md)

WFP enthält eine Reihe [integrierter Unterebenen.](management-filtering-sublayer-identifiers.md) Jede Ebene erbt alle integrierten Unterebenen. Benutzer können auch eigene Unterebenen hinzufügen.

Die Liste der Filter-Engine-Ebenen finden Sie im Referenzabschnitt [**Thema Filtern von Ebenenbezeichnern.**](management-filtering-layer-identifiers-.md)

## <a name="filters"></a>Filter

Ein *Filter* ist eine Regel, die mit eingehenden oder ausgehenden Paketen übereinstimmen. Die Regel teilt der Filter-Engine mit, was mit dem Paket zu tun ist, einschließlich des Aufrufs eines Calloutmoduls für die tiefe Paket- oder Streamüberprüfung. Ein Filter kann z. B. "Datenverkehr mit einem TCP-Port über 1024 blockieren" oder "Call out to IDS for all traffic that is not secured" (Aufruf an IDS für sämtlichen Datenverkehr, der nicht gesichert ist) angeben.

Ein Startzeitfilter ist ein Filter, der zur Startzeit erzwungen wird, sobald der TCP/IP-Stapeltreiber (tcpip.sys) gestartet wird. Ein Startzeitfilter wird deaktiviert, wenn BFE gestartet wird. Ein Filter wird als Startzeit gekennzeichnet, indem das [**FWPM \_ FILTER \_ FLAG \_ BOOTTIME-Flag**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0) beim [**Aufrufen von FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0) aktiviert wird.

Ein Laufzeitfilter ist ein Filter, der nach dem Start von BFE erzwungen wird. Ein Laufzeitfilter kann je nach Art der Erstellten statisch, dynamisch oder persistent sein. Weitere [Informationen zu den](object-management.md) verschiedenen Typen von Laufzeitfiltern und deren Lebensdauer finden Sie unter Objektverwaltung.

## <a name="shims"></a>Shims

Ein *Shim ist* eine Komponente im Kernelmodus, die Filterentscheidungen trifft, indem er anhand der Filter-Engine-Ebenen klassifiziert wird. Jeder Shim wird für eine oder mehrere Ebenen klassifiziert. Der Shim transport layer module klassifiziert z. B. für das erste Paket eines Datenflusses die Eingangstransportebene, die Ausgehende Transportebene und die ALE Verbinden- und Receive-Accept-Schichten.

Während Pakete, Datenströme und Ereignisse den Netzwerkstapel durchlaufen, analysieren die Shims sie, um die durchklassifizierbaren Bedingungen und Werte zu extrahieren, und rufen dann die Filter-Engine auf, um sie anhand der Filter in einer bestimmten Ebene zu bewerten. Die Filter-Engine kann im Rahmen der Klassifizierung eine oder mehrere Aufrufe aufrufen. Die Shims führen das tatsächliche Löschen von Paketen, Streams und Ereignissen basierend auf dem Ergebnis der Klassifizierung durch, die von der Filter-Engine ausgeführt wird.

## <a name="callouts"></a>Aufrufe

Eine *Rückruffunktion ist* eine Reihe von Funktionen, die von einem Treiber verfügbar gemacht und für spezielle Filterung verwendet werden. Sie werden verwendet, um die Pakete zu analysieren und zu manipulieren, z. B. Virenscan, Überprüfung der Jugendschutz auf ungeeigneten Inhalt, Paketdatenanalyse für Überwachungstools. Einige Aufrufe, z. B. der NAT-Treiber (Network Address Translation), sind in das Betriebssystem integriert. Andere, wie z. B. eine HTTP-Jugendschutz-Callout oder die IDS-Rückrufe (Intrusion Detection System), können von unabhängigen Softwareherstellern (INDEPENDENT Software Vendors, ISVs) bereitgestellt werden. Die Calloutfunktionen werden von der Filter-Engine aufgerufen, wenn ein entsprechender Aufruffilter auf einer bestimmten Ebene übereinstimmen.

Callouts können auf allen WFP-Ebenen im Kernelmodus registriert werden. Rückrufe können eine Aktion ("Blockieren", "Zulassen" und bei der Streamüberprüfung "Zurückstellen", "Weitere Daten benötigen", "Verbindung ablegen") zurückgeben und eingehenden und ausgehenden Netzwerkdatenverkehr ändern und schützen.

Sobald eine Rückrufliste bei der Filter-Engine registriert wurde, kann sie zu verarbeitenden Netzwerkdatenverkehr empfangen. Der Datenverkehr kann je nach Ebene Pakete, Streams oder Ereignisse sein. Eine Anwendung oder ein Firewall-Agent bewirkt, dass Datenverkehr an eine Rückrufliste übergeben wird, indem ein Filter hinzugefügt wird, dessen Aktion "Callout" ist und dessen Aufruf-ID der Bezeichner dieser Rückrufliste ist. Durch Aufrufe kann die Filter-Engine angewiesen werden, "Block" oder "Permit" an den Shim zurück zu geben. Rückrufe können auch "Continue" zurückgeben, damit andere Filter das Paket verarbeiten können.

Mehrere Aufrufe können von einem Callouttreiber verfügbar gemacht werden.

Eine Aufrufe müssen hinzugefügt (mit [**FwpmCalloutAdd0)**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutadd0)und registriert (mit [FwpsCalloutRegister)](/windows-hardware/drivers/ddi/_netvista/)werden, bevor sie verwendet werden kann. Vor der Erstellung von Filtern, die auf die Rückrufe verweisen, ist ein Aufruf von **FwpmCalloutAdd0** erforderlich. Ein Aufruf von FwpsCalloutRegister ist erforderlich, bevor WFP die Aufrufe aufrufen kann, wenn die Aufruffilter übereinstimmen. Standardmäßig werden Filter, die auf Aufrufe verweisen, die hinzugefügt, aber noch nicht bei der Filter-Engine registriert wurden, als "Blockieren"-Filter behandelt. Die Reihenfolge des Aufrufs **von FwpmCalloutAdd0** und FwpsCalloutRegister spielt keine Rolle. Eine persistente Rückrufe muss nur einmal hinzugefügt werden und muss jedes Mal registriert werden, wenn der Treiber, der die Callout implementiert, gestartet wird (z. B. nach einem Neustart).

## <a name="classification"></a>Klassifizierung

Klassifizierung ist der Prozess der Anwendung von Filtern auf Netzwerkdatenverkehr (Paket, Stream oder Ereignis), um das Ergebnis von "Zulassen" oder "Blockieren" für diesen Datenverkehr zu bestimmen. Für ein Paket, einen Stream oder ein Ereignis gibt es einen Klassifizierungsaufruf pro Ebene.

Während der Klassifizierung werden die Eigenschaften (z. B. die Quelladresse) des Pakets, Streams oder Ereignisses mit Filterbedingungen verglichen, die für Filter auf der Ebene festgelegt werden, auf der die Klassifizierung aufgerufen wird. Wenn Übereinstimmungen gefunden werden, wird der [Filter-Vermittlungsalgorithmus](filter-arbitration.md) verwendet, um das Ergebnis des Klassifizierungsprozesses zu bestimmen.

Eine Klassifizierungsanforderung wird durch einen Shim ausgelöst.

Klassifizierungsaktionen können eine der beiden aktionen sein:

-   Zulassen
-   Blockieren
-   Legende
    -   Zulassen
    -   Blockieren
    -   Weiter
    -   Verschieben
    -   Weitere Daten benötigen
    -   Verbindung verdringen

## <a name="wfp-operation"></a>WFP-Vorgang

Sobald der TCP/IP-Stapeltreiber (tcpip.sys) gestartet wird, erzwingt die Kernelmodus-Filter-Engine zur Startzeit die Sicherheitsrichtlinie des Systems durch Startzeitfilter.

Sobald die Basisfilterungs-Engine (Base Filtering Engine, BFE) im Benutzermodus gestartet wird, werden der Plattform persistente Filter hinzugefügt, Startzeitfilter deaktiviert, und Benachrichtigungen werden an die Callouttreiber gesendet, die [mit FwpmBfeStateSubscribeChanges0 abonniert haben.](/windows-hardware/drivers/ddi/fwpmk/nf-fwpmk-fwpmbfestatesubscribechanges0) Die Benachrichtigungen werden unmittelbar nach Abschluss der BFE-Initialisierung gesendet. Die Plattform ist jetzt bereit für die Registrierung von Rückrufen und das Hinzugefügt von Laufzeitobjekten.

Der Übergang von der Startzeit zu permanenten Filtern kann auf einem langsamen Computer mehrere Sekunden oder sogar länger dauern. Dies ist atomar. Wenn ein Anbieter sowohl über einen Startzeit- als auch über einen permanenten Filter verfügt, wird es also nie ein Fenster geben, wenn keines von beiden wirksam ist.

Nach dem Start von BFE können Laufzeitfilter von Firewall-Agents oder von benutzerdefinierten Firewalllösungen hinzugefügt werden. BFE verarbeitet diese Filter und sendet sie zur Erzwingung an die entsprechende Filtermodulebene. BFE akzeptiert auch Authentifizierungseinstellungen und sendet diese Einstellungen an die IPsec-Schlüsselmodulen (IKE/AuthIP). Weitere [Informationen finden Sie unter IPsec-Konfiguration.](ipsec-configuration.md)

Filter und Authentifizierungseinstellungen können jederzeit über die VOM BFE verfügbar gemachte RPC-Schnittstelle im System hinzugefügt, entfernt oder geändert werden. Untergeordnete Ebenen und Calloutmodule können ebenfalls hinzugefügt oder entfernt werden.

Datenfluss:

1.  Ein Paket wird in den Netzwerkstapel übertragen.
2.  Der Netzwerkstapel sucht einen Shim und ruft ihn auf.
3.  Der Shim ruft den Klassifizierungsprozess auf einer bestimmten Ebene auf.
4.  Während der Klassifizierung werden Filter übereinstimmen, und die resultierende Aktion wird ergriffen. (Weitere Informationen [finden Sie unter Filtern von Vermittlungen.)](filter-arbitration.md)
5.  Wenn während des Klassifizierungsprozesses Eine Übereinstimmung mit Rückruffiltern vor sich geht, werden die entsprechenden Aufrufe aufgerufen.
6.  Der Shim bezieht sich auf die endgültige Filterungsentscheidung (z. B. das Ablegen des Pakets).

Der ausgehende Datenfluss folgt einem ähnlichen Muster.

In den folgenden Themen wird der Betrieb des WFP weiter beschrieben.

-   [TCP-Paketflüsse](tcp-packet-flows.md)
-   [UDP-Paketflüsse](udp-packet-flows.md)
-   [Filtern der Vermittlung](filter-arbitration.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Objektmodell](object-model.md)
</dt> <dt>

[Objektverwaltung](object-management.md)
</dt> </dl>

 

 