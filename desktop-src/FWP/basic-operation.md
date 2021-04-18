---
title: WFP-Vorgang
description: Die Windows-Filter Plattform (WFP) führt ihre Aufgaben durch die Integration der folgenden grundlegenden Entitäts Ebenen, Filter, Shims und Callouts durch.
ms.assetid: bf88ace7-1160-434b-9be0-3f9db6aa2e87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e7a7d38bd0de5b1f549e2187c414644bf68442
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106338261"
---
# <a name="wfp-operation"></a>WFP-Vorgang

Die Windows-Filter Plattform (WFP) führt ihre Aufgaben durch die Integration der folgenden grundlegenden Entitäten durch: *Ebenen*, *Filter*, *Shims* und *Legenden.*

## <a name="layers"></a>Ebenen

Eine *Ebene* ist ein Container, der von der Filter-Engine verwaltet wird, deren Funktion das Organisieren von Filtern in Sets vorsieht. Eine Ebene ist kein Modul im Netzwerk Stapel. Jede Ebene verfügt über ein Schema, das den Typ der Filter definiert, die dieser hinzugefügt werden können. Weitere Informationen finden Sie [unter Filterbedingungen, die auf jeder Filter Ebene verfügbar sind](filtering-conditions-available-at-each-filtering-layer.md) .

Ebenen können Unterebenen enthalten, um widersprüchliche Filteranforderungen zu verwalten, z. b. "Blockieren von TCP-Ports über 1024" und "Open Port 1080". Die Regeln zum Verwalten von Filter Konflikten werden durch [Filter-Schiedsgerichtsbarkeit](filter-arbitration.md)bestimmt.

WFP enthält eine Reihe [integrierter Unterebenen](management-filtering-sublayer-identifiers.md). Jede Ebene erbt alle integrierten Unterebenen. Benutzer können auch eigene untergeordnete Ebenen hinzufügen.

Die Liste der Filter-Engine-Schichten finden Sie im Referenz Abschnitt [**Filtern von ebenenbezeichern**](management-filtering-layer-identifiers-.md).

## <a name="filters"></a>Filter

Ein *Filter* ist eine Regel, die mit eingehenden oder ausgehenden Paketen übereinstimmt. Die Regel teilt der Filter-Engine mit, was mit dem Paket zu tun ist, einschließlich des aufrufungsmoduls für eine Tiefe Paket-oder Datenstrom Untersuchung. Ein Filter kann z. b. "Blockieren von Datenverkehr mit einem TCP-Port größer als 1024" oder "Aufrufe an IDs für nicht gesicherten Datenverkehr" angeben.

Ein Filter für die Start Zeit ist ein Filter, der zum Zeitpunkt der Startzeit erzwungen wird, sobald der TCP/IP-stapeltreiber (tcpip.sys) gestartet wird. Ein Start Zeitfilter ist deaktiviert, wenn BFE gestartet wird. Ein Filter wird als Start Zeit gekennzeichnet, indem das Flag "Boottime" für das [**fwpm- \_ \_ \_ filterflag**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0) festgelegt wird, wenn [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0) aufgerufen wird.

Ein Lauf Zeitfilter ist ein Filter, der nach dem Start von BFE erzwungen wird. Ein Lauf Zeitfilter kann abhängig von der Art der Erstellung statisch, dynamisch oder permanent sein. Weitere Informationen zu den verschiedenen Typen von Lauf Zeit Filtern und deren Lebensdauer finden Sie unter [Objekt Verwaltung](object-management.md) .

## <a name="shims"></a>Shims

Ein *Shim* ist eine Kernelmoduskomponente, die Filter Entscheidungen durch die Klassifizierung der Filter-Engine-Ebenen ermöglicht. Jedes Shim klassifiziert eine oder mehrere Ebenen. Beispielsweise klassifiziert das transportebenenmodul-Shim die eingehende Transportschicht, die ausgehende Transportschicht und die ALE Connect-und Receive-Accept Ebenen für das erste Paket eines Flows.

Da Pakete, Streams und Ereignisse den Netzwerk Stapel durchlaufen, analysieren die Shims diese, um die klassifizierbaren Bedingungen und Werte zu extrahieren, und dann die Filter-Engine aufzurufen, um Sie anhand der Filter in einer bestimmten Ebene auszuwerten. Die Filter-Engine kann eine oder mehrere Legenden als Teil der Klassifizierung aufrufen. Die Shims führen das eigentliche Löschen von Paketen, Streams und Ereignissen basierend auf dem Ergebnis der Klassifizierung durch, die von der Filter-Engine ausgeführt wird.

## <a name="callouts"></a>Aufrufe

Eine Legende ist eine Reihe von Funktionen *,* die von einem Treiber verfügbar gemacht und für die spezielle Filterung verwendet werden. Sie werden verwendet, um die Pakete zu analysieren und zu manipulieren, wie z. b. Viren Überprüfung, Überprüfung auf ungeeignete Inhalte durch die Überprüfung auf ungeeignete Inhalte, Paketdaten Analyse für Überwachungstools. Einige Legenden, wie z. b. der Network Address Translation (NAT)-Treiber, sind in das Betriebssystem integriert. Andere, wie z. b. eine HTTP-Steuerelement Legende oder das Angriffs Erkennungs System (ID), können von unabhängigen Softwareanbietern (ISVs) bereitgestellt werden. Die Legenden Funktionen werden von der Filter-Engine aufgerufen, wenn ein entsprechender Legenden Filter auf einer bestimmten Ebene übereinstimmt.

Callouts können in jeder der Kernel Modus-WFP-Ebenen registriert werden. Callouts können eine Aktion ("blockieren", "zulassen") zurückgeben und beim Durchführen der streamüberprüfung "verzögern", "Weitere Daten benötigen", "Verbindung löschen") und den eingehenden und ausgehenden Netzwerk Datenverkehr ändern und sichern.

Sobald eine Legende bei der Filter-Engine registriert ist, kann Sie zu verarbeitende Netzwerk Datenverkehr empfangen. Der Datenverkehr kann abhängig von der Ebene Pakete, Streams oder Ereignisse sein. Eine Anwendung oder ein Firewall-Agent bewirkt, dass Datenverkehr an eine Legende übermittelt wird, indem ein Filter hinzugefügt wird, dessen Aktion "Legenden" ist und dessen Legenden-ID der Bezeichner der Legende ist. Callouts können das Filtermodul anweisen, "Block" oder "zulassen" an das Shim zurückzugeben. Aufrufe können auch "Continue" zurückgeben, damit andere Filter das Paket verarbeiten können.

Mehrere Aufrufe können von einem Legenden Treiber verfügbar gemacht werden.

Eine Legende muss hinzugefügt werden (mit [**FwpmCalloutAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutadd0)) und (mit [fwpscallumgiester](/windows-hardware/drivers/ddi/_netvista/)) registriert werden, bevor Sie verwendet werden kann. Vor der Erstellung von Filtern, die auf die Legende verweisen, ist ein Aufruf von **FwpmCalloutAdd0** erforderlich. Ein Aufruf von fwpscallmysqgiester ist erforderlich, bevor WFP die Legende aufrufen kann, wenn die Legenden Filter abgeglichen werden. Standardmäßig werden Filter, die auf Aufrufe verweisen, die hinzugefügt, aber noch nicht bei der Filter-Engine registriert wurden, als "Block Filter" behandelt. Die Reihenfolge, in der **FwpmCalloutAdd0** und fwpscallumgisteraufgerufen werden, spielt keine Rolle. Eine permanente Legende muss nur einmal hinzugefügt werden und muss jedes Mal registriert werden, wenn der Treiber, der die Legende implementiert, gestartet wird (z. b. nach einem Neustart).

## <a name="classification"></a>Klassifizierung

Klassifizierung ist der Prozess, bei dem Filter auf den Netzwerk Datenverkehr (Paket, Stream oder Ereignis) angewendet werden, um das Ergebnis "zulassen" oder "blockieren" für diesen Datenverkehr zu ermitteln. Bei einem Paket, einem Stream oder einem Ereignis gibt es einen Klassifizierungs aufruppe pro Schicht.

Während der Klassifizierung werden die Eigenschaften (z. b. Quelladresse) des Pakets, Streams oder Ereignisses mit Filterbedingungen verglichen, die für Filter auf der Ebene festgelegt sind, auf der die Klassifizierung aufgerufen wird. Wenn Übereinstimmungen gefunden werden, wird der [Filter-Schiedsgerichts](filter-arbitration.md) ungsalgorithmus verwendet, um das Ergebnis des Klassifizierungs Vorgangs zu bestimmen.

Eine Klassifizierungs Anforderung wird von einem Shim ausgelöst.

Klassifizierungs Aktionen können wie folgt lauten:

-   Zulassen
-   Blockieren
-   Legende
    -   Zulassen
    -   Blockieren
    -   Weiter
    -   Wickeln
    -   Weitere Daten benötigen
    -   Verbindung löschen

## <a name="wfp-operation"></a>WFP-Vorgang

Sobald der TCP/IP-stapeltreiber (tcpip.sys) gestartet wird, erzwingt die kernelmodusfilter-Engine die Sicherheitsrichtlinie des Systems über Start Zeitfilter, sobald der TCP/IP-stapeltreiber () gestartet wird.

Nachdem die Basis Filter-Engine (BFE) im Benutzermodus gestartet wurde, werden der Plattform persistente Filter hinzugefügt, die Start Zeitfilter sind deaktiviert, und Benachrichtigungen werden an die Legenden Treiber gesendet, die mithilfe von [FwpmBfeStateSubscribeChanges0](/windows-hardware/drivers/ddi/fwpmk/nf-fwpmk-fwpmbfestatesubscribechanges0)abonniert wurden. Die Benachrichtigungen werden unmittelbar nach Abschluss der Initialisierung von BFE versendet. Die Plattform ist nun bereit für die Registrierung und das Hinzufügen von Lauf Zeit Objekten.

Die Umstellung von der Start Zeit auf persistente Filter kann auf einem langsamen Computer mehrere Sekunden oder sogar länger dauern. Er ist atomarisch. Wenn ein Anbieter also sowohl über einen Startzeit als auch über einen persistenten Filter verfügt, wird nie ein Fenster angezeigt, wenn keines der beiden Optionen wirksam ist.

Nach dem Start von BFE können Lauf Zeitfilter durch Firewall-Agents oder durch benutzerdefinierte Firewalllösungen hinzugefügt werden. BFE verarbeitet diese Filter und sendet Sie zur Erzwingung an die entsprechende Filter-Engine-Schicht. BFE akzeptiert auch Authentifizierungs Einstellungen und sendet diese Einstellungen an die IPSec-Schlüssel für die Schlüssel Erstellung (IKE/AuthIP). Weitere Informationen finden Sie unter [IPSec-Konfiguration](ipsec-configuration.md) .

Filter und Authentifizierungs Einstellungen können jederzeit über die RPC-Schnittstelle, die von den BFE verfügbar gemacht wird, im System hinzugefügt, entfernt oder geändert werden. Unterebenen und Legenden Module können ebenfalls hinzugefügt oder entfernt werden.

Datenfluss:

1.  Ein Paket wird in den Netzwerk Stapel integriert.
2.  Der Netzwerk Stapel findet und Ruft einen Shim auf.
3.  Der Shim ruft den Klassifizierungsprozess auf einer bestimmten Ebene auf.
4.  Während der Klassifizierung werden Filter abgeglichen, und die resultierende Aktion wird durchgeführt. (Siehe [Filter-Schiedsgerichtsbarkeit](filter-arbitration.md).)
5.  Wenn beim Klassifizierungsprozess alle Legenden Filter abgeglichen werden, werden die entsprechenden Legenden aufgerufen.
6.  Der Shim agiert bei der abschließenden Filter Entscheidung (z. b. beim Ablegen des Pakets).

Der ausgehende Datenfluss folgt einem ähnlichen Muster.

In den folgenden Themen wird der WFP-Vorgang ausführlicher beschrieben.

-   [TCP-paketflows](tcp-packet-flows.md)
-   [UDP-paketflows](udp-packet-flows.md)
-   [Filterung Filtern](filter-arbitration.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Objektmodell](object-model.md)
</dt> <dt>

[Objekt Verwaltung](object-management.md)
</dt> </dl>

 

 