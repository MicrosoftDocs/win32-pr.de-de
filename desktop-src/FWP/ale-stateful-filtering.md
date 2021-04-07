---
title: Status behaftete ALE Filterung
description: Filter, die auf der Ebene (Application Layer Enforcement) der Windows-Filter Plattform (WFP) installiert sind, führen eine Zustands behaftete Netzwerk Filterung durch.
ms.assetid: d5a3fcad-d55e-4a07-af21-cb40e5e9a9ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30cc1b4a5830efd0fef6dc28c88db85cd9c88cca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038987"
---
# <a name="ale-stateful-filtering"></a>Status behaftete ALE Filterung

Filter, die auf der Ebene (Application Layer Enforcement) der Windows-Filter Plattform (WFP) installiert sind, führen eine Zustands behaftete Netzwerk Filterung durch. Ein *ALE Datenfluss* wird als Grundlage für die Zustands behaftete ALE-Filterung verwendet.

Ein ALE Fluss ist eine Möglichkeit zur Klassifizierung von Netzwerk Datenverkehr, indem er basierend auf einer Quell-IP-Adresse, einer Ziel-IP-Adresse, einem Quellport, einem Zielport und einem Protokoll gruppiert wird. Ein ALE-Datenfluss könnte generisch sein, d. h. mindestens einer der Deskriptoren kann alles (oder Platzhalter Zeichen \* ) entsprechen. Beispielsweise würde ein generischer UDP-ALE-Datenfluss als Quell-IP-Adresse = \* , Ziel-IP-Adresse = \* , Quellport = \* , Zielport = \* und Protokoll = UDP beschrieben werden.

Nachdem eine Verbindung autorisiert wurde (eingehende Verbindungen werden auf der Ebene der BPM-Schicht der Ebene [**\_ \_ \_ auth \_ recv \_ akzeptieren \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) ) und ausgehende Verbindungen auf der Ebene der Ebene der Ebene der Ebene der Ebene der Ebene der Ebene der Ebene der Ebene der Ebene der Ebene der Ebene der Ebene der Ebene ein ALE Datenfluss wird so erstellt, dass bei einer Richtlinien Änderung alle Pakete, die ein-und ausgehenden Datenverkehr aufweisen und zum gleichen ALE Datenfluss gehören, automatisch zugelassen werden. **\_ \_ \_ \_ \_ \|** Da eine Richtlinien Änderung möglicherweise die Blockierung zuvor zulässiger Verbindungen erfordert, müssen bei einer Richtlinien Änderung eine [erneute Autorisierung](ale-re-authorization.md) durchgeführt werden.

Die Zustands behaftete ALE-Filterung reduziert die Anzahl der erforderlichen Klassifizierungen drastisch, indem nur das erste Paket klassifiziert wird, das zu einem ALE-Datenfluss gehört. Im Vergleich dazu erfordert eine nicht Zustands behaftete Filterung die Klassifizierung jedes Pakets, das das Netzwerk durchläuft.

Ein ALE-Datenfluss hat eine zugeordnete Richtung, die die Richtung des ersten Pakets des Flows ist. Dies ermöglicht flexiblere Richtlinien, indem es eingehende initiierte Verbindungen zulässt, dass Sie über unterschiedliche Richtlinien von ausgehenden, initiierten Verbindungen verfügen.

## <a name="tcp-ale-flow"></a>TCP-ALE-Fluss

Ein ALE Datenverkehr für TCP-Datenverkehr wird durch das fünf-Tupel von TCP/IP (Quell-IP-Adresse, Ziel-IP-Adresse, Quellport, Zielport und Protokoll) identifiziert.

Ein TCP-ALE-Datenfluss hat die gleiche Lebensdauer wie ein verbundener TCP-Socket. Ein verbundener TCP-Socket kann entweder ein mit [**Connect ()**](/windows/desktop/api/winsock2/nf-winsock2-connect) erstellter Socket oder ein Socket sein, der als Ergebnis eines [**Accept ()**](/windows/desktop/api/winsock2/nf-winsock2-accept) -Aufrufes erstellt wurde.

ALE verwaltet eine 1:1-Beziehung zwischen einem TCP-ALE-Datenfluss und einem TCP-Kontroll Block (TCB).

## <a name="udp-ale-flow"></a>UDP-ALE-Fluss

> [!Note]  
> Protokolle, die nicht TCP oder ICMP lauten, werden wie UDP behandelt.

 

Ein ALE Fluss für UDP-Datenverkehr wird durch das fünf-Tupel von TCP/IP identifiziert (Quell-IP-Adresse, Ziel-IP-Adresse, Quellport, Zielport und Protokoll).

Ein UDP-ALE-Datenfluss wird auf Grundlage eines UDP-Sockets erstellt und stellt den Remotepeer dar, mit dem die Anwendung kommuniziert. Ein Remotepeer wird durch ein Tupel (Ziel-IP-Adresse und Zielport) identifiziert.

Zwischen einem UDP-Socket und den Remote Peers, mit denen er kommuniziert, besteht eine 1: n-Beziehung.

Wenn der lokale UDP-Socket geschlossen wird, werden alle damit verknüpften ALE Flows gelöscht.

Wenn keine socketabschlüsse vorhanden sind, haben UDP-Unicast-ALE-Flows ein [konfigurierbares](ale-flow-customization.md) Leerlauf Timeout, das standardmäßig 60 Sekunden beträgt. Wenn in diesem Fenster keine Pakete gesendet oder empfangen werden, wird der ALE Flow gelöscht. Dieses Standard Timeout wird progressiv verkürzt, wenn die Anzahl der von der systemweiten ALE-Abläufe einen bestimmten Schwellenwert erreicht.

## <a name="icmp-ale-flow"></a>ICMP-ALE-Datenfluss

Ein ALE Fluss für ICMP-Datenverkehr wird durch das sechs-Tupel (Quell-IP-Adresse, Ziel-IP-Adresse, ICMP-Typ, ICMP-Code, Protokoll und ICMP-ID) identifiziert. Die ICMP-ID ist Teil des ALE-Flows nur für ICMP-Echo-/Antwort-Datenverkehr.

Wenn keine socketsperrungen vorhanden sind, haben ICMP-Unicast-ALE-Flows ein [konfigurierbares](ale-flow-customization.md) Leerlauf Timeout, das standardmäßig 60 Sekunden beträgt. Wenn in diesem Fenster keine Pakete gesendet oder empfangen werden, wird der ALE Flow gelöscht. Dieses Standard Timeout wird progressiv verkürzt, wenn die Anzahl der von der systemweiten ALE-Abläufe einen bestimmten Schwellenwert erreicht.

Nur ICMP-Fehlermeldungen, die nicht fehlerhaft sind, werden für ALE Ebenen angezeigt. ICMP-Fehlermeldungen können auf ICMP- \_ Fehler Ebenen überprüft werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Durchsetzung der Anwendungsschicht (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[ALE Ebenen](ale-layers.md)
</dt> <dt>

[ALE Multicast-/Broadcast Datenverkehr](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Erneute ALE-Autorisierung](ale-re-authorization.md)
</dt> <dt>

[Anpassung des ALE-Flows](ale-flow-customization.md)
</dt> <dt>

[TCP-paketflows](tcp-packet-flows.md)
</dt> <dt>

[UDP-paketflows](udp-packet-flows.md)
</dt> <dt>

[Winsock-Funktionen](/windows/desktop/WinSock/winsock-functions)
</dt> </dl>

 

 