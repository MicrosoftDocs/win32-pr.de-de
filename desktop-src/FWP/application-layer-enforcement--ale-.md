---
title: Durchsetzung der Anwendungsschicht (ALE)
description: ALE ist ein Satz von Windows Filtering Platform (WFP)-kernelmodusschichten, die für die Zustands behaftete Filterung verwendet werden.
ms.assetid: ffebd312-9220-476c-a4ba-28e2e8ac8879
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f4cab1b2583d221c59d83c513c451077c806129
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390269"
---
# <a name="application-layer-enforcement-ale"></a>Durchsetzung der Anwendungsschicht (ALE)

ALE ist ein Satz von Windows Filtering Platform (WFP)-kernelmodusschichten, die für die Zustands behaftete Filterung verwendet werden.

Durch die Zustands behaftete Filterung wird der Status von Netzwerkverbindungen nachverfolgt, und nur Pakete, die einem bekannten Verbindungsstatus entsprechen, werden zugelassen. Beispielsweise kann eine Zustands behaftete Filterung für eine TCP-Verbindung, die von hinter einer Firewall initiiert wurde, nur eingehende Pakete zulassen, die mit vorherigen ausgehenden Paketen, die von der Partei geschützt

Filter in den ALE-Ebenen autorisieren die Erstellung von eingehenden und ausgehenden Verbindungen, Port Zuweisungen, Socketvorgänge wie " [**lauschen ()**](/windows/desktop/api/winsock2/nf-winsock2-listen)", die Erstellung von Rohdaten Socket und den Empfangsmodus.

Der Datenverkehr auf der ALE Ebene wird entweder pro Verbindung oder pro Socket klassifiziert. Bei nicht-ALE Ebenen kann der Datenverkehr nur auf Paketbasis von Filtern klassifiziert werden.

ALE Ebenen sind die einzigen WFP-Schichten, bei denen Netzwerk Datenverkehr basierend auf der Anwendungs Identität – mithilfe eines normalisierten Datei namens – und basierend auf der Benutzeridentität – mithilfe einer Sicherheits Beschreibung gefiltert werden kann. (Siehe "f \_ " Datei \_ Namen \_ Informationen in der Dokumentation zum Windows-Treiberkit (WDK), um weitere Informationen zu normalisierten Dateinamen zu erhalten.)

Wenn IPSec zum Schutz der Verbindung verwendet wird, kann darüber hinaus auch die Filterung auf der Ebene der Remote Computer und die Identität des Remote Benutzers durchgeführt werden. Der Remote Computer und die Benutzer Identitäten werden aus den Anmelde Informationen abgerufen, die beim Erstellen einer IPSec-Sitzung verwendet werden.

Aus diesem Grund werden Richtlinien, die erzwingen, dass (z. b. "Administrator") und/oder welche Anwendung (z. b. "Internet Explorer") die oben erwähnten Netzwerk Vorgänge ausführen dürfen, auf der ALE Ebene erstellt.

ALE bietet die Erzwingung von Richtlinien wie z. b. "Windows Messenger allen Zugriff auf das Netzwerk gestatten, während alle anderen Anwendungen blockiert werden". Wenn z. b. die Anwendung "Messenger" über das Netzwerk eine Verbindung herstellt, fängt ALE das Ereignis ab, stellt fest, dass es von Messenger initiiert wurde, und fragt die WFP-Filter-Engine ab, um zu bestimmen, ob der Socket fortgesetzt werden darf.

> [!Note]  
> Aufgrund der Art von echten Dual-IP-Sockets treten möglicherweise keine Klassifizierungen auf der IPv4-ALE-Ebene auf. Dies ist Entwurfs bedingt, da der Socket für alle Intents und Zwecke ein IPv6-Socket ist. Um den V4-Datenverkehr für einen solchen Socket anzuzeigen, erstellen Sie mithilfe der IPv6-zugeordneten Adresse Filter auf der v6-Schicht.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ALE Ebenen](ale-layers.md)
</dt> <dt>

[Status behaftete ALE Filterung](ale-stateful-filtering.md)
</dt> <dt>

[ALE Multicast-/Broadcast Datenverkehr](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Erneute ALE-Autorisierung](ale-re-authorization.md)
</dt> <dt>

[Anpassung des ALE-Flows](ale-flow-customization.md)
</dt> </dl>

 

 