---
title: Erzwingung der Anwendungsschicht (Application Layer Enforcement, ALE)
description: ALE ist eine Reihe von Windows WFP-Kernelmodusebenen (Filtering Platform), die für die zustandsbasierte Filterung verwendet werden.
ms.assetid: ffebd312-9220-476c-a4ba-28e2e8ac8879
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d74db5fdc231569f65c3b25cb630b306111aa5d6a7e3eb7faad743a5f74db8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069470"
---
# <a name="application-layer-enforcement-ale"></a>Erzwingung der Anwendungsschicht (Application Layer Enforcement, ALE)

ALE ist eine Reihe von Windows WFP-Kernelmodusebenen (Filtering Platform), die für die zustandsbasierte Filterung verwendet werden.

Die zustandshafte Filterung verfolgt den Status von Netzwerkverbindungen nach und lässt nur Pakete zu, die mit einem bekannten Verbindungsstatus übereinstimmen. Beispielsweise kann die zustandshafte Filterung für eine TCP-Verbindung, die hinter einer Firewall initiiert wurde, nur eingehende Pakete zulassen, die mit vorherigen ausgehenden Paketen übereinstimmen, die von der geschützten Partei gesendet wurden.

Filter in den ALE-Ebenen autorisieren die Erstellung eingehender und ausgehender Verbindungen, Portzuweisungen, Socketvorgänge wie [**listen()**](/windows/desktop/api/winsock2/nf-winsock2-listen), die Erstellung von Unformatierungssocket und den Empfang im promiscuous-Modus.

Der Datenverkehr auf den ALE-Ebenen wird entweder pro Verbindung oder pro Socket klassifiziert. Auf Nicht-ALE-Ebenen können Filter Datenverkehr nur pro Paket klassifizieren.

ALE-Ebenen sind die einzigen WFP-Ebenen, bei denen Netzwerkdatenverkehr basierend auf der Anwendungsidentität – mithilfe eines normalisierten Dateinamens – und basierend auf der Benutzeridentität mithilfe eines Sicherheitsdeskriptors gefiltert werden kann. (Siehe FLT \_ \_ \_ DATEINAMENINFORMATIONEN in der WDK-Dokumentation (Windows Driver Kit), um weitere Informationen zu normalisierten Dateinamen zu erhalten.)

Wenn IPsec zum Sichern der Verbindung verwendet wird, kann das Filtern auf ALE-Ebenen auch für die Identität des Remotecomputers und für die Remotebenutzeridentität durchgeführt werden. Der Remotecomputer und die Benutzeridentitäten werden aus den Anmeldeinformationen ermittelt, die bei der Erstellung einer IPsec-Sitzung verwendet wurden.

Aus diesem Grund werden Richtlinien, die erzwingen, wer (z. B. "Administrator") und/oder welche Anwendung (z. B. "Internet Explorer") die oben genannten Netzwerkvorgänge ausführen darf, auf den ALE-Ebenen verfasst.

ALE bietet Erzwingung für Richtlinien wie "Windows Messenger den zugriff auf das Netzwerk erlauben und gleichzeitig alle anderen Anwendungen blockieren". Wenn die Anwendung "Messenger" in einem solchen Beispiel eine Verbindung über das Netzwerk herstellt, fängt ALE das Ereignis ab, ermittelt, dass es von Messenger initiiert wurde, und fragt die WFP-Filter-Engine ab, um zu bestimmen, ob der Socket fortgesetzt werden darf.

> [!Note]  
> Aufgrund der Natur echter Dual-IP-Sockets werden Klassifizierungen auf der IPv4-ALE-Schicht möglicherweise nicht verwendet. Dies ist beabsichtigt, da der Socket für alle Absichten und Zwecke ein IPv6-Socket ist. Um den V4-Datenverkehr für einen solchen Socket zu sehen, erstellen Sie Filter auf der V6-Ebene mithilfe der IPv6-zugeordneten Adresse.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ALE-Ebenen](ale-layers.md)
</dt> <dt>

[Zustands behaftete ALE-Filterung](ale-stateful-filtering.md)
</dt> <dt>

[ALE-Multicast-/Broadcastdatenverkehr](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Erneute ALE-Autorisierung](ale-re-authorization.md)
</dt> <dt>

[ALE Flow Anpassung](ale-flow-customization.md)
</dt> </dl>

 

 