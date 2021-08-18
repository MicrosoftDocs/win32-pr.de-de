---
title: Erneute ALE-Autorisierung
description: Der Netzwerkdatenverkehr auf den ALE-Ebenen (Application Layer Enforcement) der Windows Filtering Platform (WFP) wird nach ALE-Datenflüssen gefiltert.
ms.assetid: 3cc7f78e-3f9d-4a91-8ea0-9b64c299068a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 850cd7f789c1fb1222a0d6820e84a42cf41763dac4e57b96667e7feda364374c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582690"
---
# <a name="ale-reauthorization"></a>Erneute ALE-Autorisierung

Der Netzwerkdatenverkehr auf den ALE-Ebenen (Application Layer Enforcement) der Windows Filtering Platform (WFP) wird nach [ALE-Datenflüssen gefiltert.](ale-stateful-filtering.md) Sobald ein ALE-Flow zugelassen wurde, wird der sämtliche Datenverkehr zugelassen, der Teil des ALE-Flusses ist. Die erneute Authentifizierung ist eine Anforderung zum Überprüfen der Berechtigungen des ALE-Flusses, in der Regel aufgrund einer Änderung der Netzwerkrichtlinie.

ALE-Datenflüssen wird basierend auf der Richtung des ersten Pakets, das die Erstellung und Autorisierung des Flows ausgelöst hat, eine Eingehende oder ausgehende Richtung zugewiesen. Eingehende ALE-Flows werden auf der [**Ebene FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) erstellt und autorisiert. Ausgehende ALE-Flows werden auf der **Ebene FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}** erstellt und autorisiert. Die Richtung des ALE-Flusses schränkt die Richtung der Pakete, die zum Flow gehören, nicht ein. ALE-Flows enthalten sowohl ein- als auch ausgehende Pakete, unabhängig von der Richtung des ALE-Flows selbst.

Die erneute Authentifizierung eines ALE-Flusses wird ausgelöst durch:

-   Eine Richtlinienänderung auf der Ebene, auf der der ALE-Flow ursprünglich autorisiert oder erstellt wurde.
-   Eine Schnittstelle für die Ankunft, die sich von der Schnittstelle abt, in der der ALE-Flow ursprünglich autorisiert oder erstellt wurde.
-   Eine ausstehende Verbindung.

Die erneute Autorisierung unterscheidet sich von der anfänglichen Autorisierung durch das Vorhandensein des [**Flags FWP \_ CONDITION FLAG IS \_ \_ \_ REAUTHORIZE.**](filtering-condition-flags-.md)

Die erneute Authentifizierung kann nur auf den [**Ebenen FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) und **FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}** ausgeführt werden.

### <a name="policy-change-reauthorization"></a>Erneute Authentifizierung von Richtlinienänderung

Eine Richtlinienänderung wird als Hinzufügen oder Entfernen von Filtern auf einer ALE-Ebene implementiert. Sobald eine Richtlinienänderung erkannt wird, wird das erste Paket, das einen ALE-Fluss durchläuft, der auf der betroffenen Ebene erstellt wurde, für die erneute Authentifizierung in der Ebene angegeben. Daher ist es für die erneute Authentifizierung möglich, dass ein ausgehendes Paket auf der [**Ebene FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) klassifiziert wird und dass ein eingehendes Paket auf der **Ebene FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}** klassifiziert ist.

Ein Grund für diese Klassifizierung in gemischter Richtung ist, dass möglicherweise kein weiterer Netzwerkdatenverkehr aus der ursprünglichen Richtung (z. B. eingehendes Paket für eingehenden ALE-Fluss) vorhanden ist. Ein Beispiel hierfür ist das one-way UDP streaming after an initial two-way handshake (UDP-Streaming in einer richtungsbasierten Richtung nach einem ersten zweigefässlichen Handshake). In diesem Fall ist es wünschenswerter, das Streaming so schnell wie möglich zu beenden.

### <a name="arrival-interface-reauthorization"></a>Arrival Interface Reauthorization

Die erneute Authentifizierung der Arrival-Schnittstelle ist ab Windows Server 2008 und Windows Vista mit Service Pack 1 (SP1) verfügbar.

Pakete, die zum gleichen ALE-Fluss gehören, können von mehreren Schnittstellen empfangen werden. Das erste Paket, das über eine andere Schnittstelle als die ursprüngliche Schnittstelle des ALE-Flusses einfing, wird erneut autorisiert.

In einem starken Hostmodell, bei dem es sich um das Standardsicherheitsmodell für den TCP/IP-Stapel handelt, akzeptiert eine Verbindung auf einer Netzwerkschnittstelle nur Pakete, die auf derselben Schnittstelle einfingen. Daher wird die erneute Authentifizierung der Ankunftsschnittstelle nicht auf einem starken Hostcomputer verwendet.

In einem schwachen Hostmodell ermöglicht eine Verbindung auf einer Netzwerkschnittstelle, dass Pakete auf jeder anderen Netzwerkschnittstelle einfingen. Die Neuautorisierung der Ankunftsschnittstelle wird auf einem schwachen Hostcomputer verwendet, um schnittstellenspezifische Richtlinien zu implementieren. Weitere Informationen finden Sie unter ["The Cable Guy: Strong and Weak Host Models".](/previous-versions/technet-magazine/cc137807(v=msdn.10))

Einige [überprüfbare Felder](filtering-conditions.md) sind während der erneuten Authentifizierung möglicherweise unbekannt. Wenn beispielsweise ein ausgehendes Paket auf der [**Ebene FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) erneut autorisiert wird, sind alle Felder für die Eingangsschnittstelle unbekannt. In diesem Fall werden die Werte der unbekannten Felder als [**FWP \_ EMPTY angegeben.**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)

Felder vom Typ [**FWP \_ EMPTY**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) können mit [**FWP \_ MATCH EQUAL \_ übereinstimmen.**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type) Daher kann eine Richtlinie so festgelegt werden, dass erneute Authentifizierungen blockiert und ein ALE-Flow beim Eintreffen von Anforderungen zur erneuten Authentifizierung für den ALE-Flow geschlossen wird.

## <a name="pending-connection-reauthorization"></a>Ausstehende erneute Verbindungsautorisierung

Ein Callouttreiber kann einen Klassifizierungsvorgang auf ALE-Ebenen verschieben und zu einem späteren Zeitpunkt abschließen, wenn die Filterungsentscheidung sicher getroffen werden kann. Die ALE-Funktion zum Verschieben/Abschließen wird über die Kernelmodusfunktionen [FwpsPendOperation0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpspendoperation0) und [FwpsCompleteOperation0 unterstützt.](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpscompleteoperation0)

Die erneute Authentifizierung wird unmittelbar nach dem FwpsCompleteOperation0-Aufruf ausgelöst, und der Callouttreiber kann den Flow zulassen oder blockieren.

Nur eine anfängliche Autorisierung kann zurückgestellt werden. Ein Aufruf von FwpsPendOperation0 kann nicht durchgeführt werden, wenn [**das Flag FWP \_ CONDITION FLAG IS \_ \_ \_ REAUTHORIZE**](filtering-condition-flags-.md) festgelegt ist.

Weitere Informationen finden Sie in der Dokumentation [Windows Driver Kit.](/windows-hardware/drivers/ddi/_netvista/)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erzwingung der Anwendungsschicht (Application Layer Enforcement, ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[ALE-Ebenen](ale-layers.md)
</dt> <dt>

[Zustands behaftete ALE-Filterung](ale-stateful-filtering.md)
</dt> <dt>

[ALE-Multicast-/Broadcastdatenverkehr](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[ALE Flow Anpassung](ale-flow-customization.md)
</dt> </dl>

 

 