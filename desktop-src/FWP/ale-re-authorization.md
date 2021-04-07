---
title: Erneute ALE-Autorisierung
description: Der Netzwerk Datenverkehr auf der Ebene (Application Layer Enforcement, ALE) der Windows-Filter Plattform (WFP) wird nach ALE Flows gefiltert.
ms.assetid: 3cc7f78e-3f9d-4a91-8ea0-9b64c299068a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed05c4c0767d449ec128250f852c365455bd0dc7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727009"
---
# <a name="ale-reauthorization"></a>Erneute ALE-Autorisierung

Der Netzwerk Datenverkehr auf der Ebene (Application Layer Enforcement, ALE) der Windows-Filter Plattform (WFP) wird nach [ALE Flows](ale-stateful-filtering.md)gefiltert. Sobald ein ALE Datenfluss zulässig ist, wird der gesamte Datenverkehr zugelassen, der Teil des ALE-Flows ist. Die erneute Autorisierung ist eine Anforderung zur Validierung der Berechtigungen des ALE-Datenflusses, in der Regel aufgrund einer Änderung der Netzwerk Richtlinie.

Bei Alen Flows wird eine Richtung, ein-und ausgehenden Datenverkehr basierend auf der Richtung des ersten Pakets zugewiesen, das die Erstellung und Autorisierung des Flows ausgelöst hat. Eingehende Datenflüsse werden auf der Ebene der Ebene der Ebene der Ebene der Ebene der Ebene der Ebene der Ebene der Ebene " [**\_ \_ \_ \_ \_ \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) " auf der Ebene der Ausgehende ALE-Datenflüsse werden auf der Ebene der Ebene der Ebene "f" der **Ebene "f \_ \_ \_ \_ \_ {4 \| 6}** " erstellt und autorisiert. Die Richtung des ALE-Flows schränkt die Richtung von Paketen, die zum Flow gehören, nicht ein. ALE Flows enthalten sowohl eingehende als auch ausgehende Pakete, unabhängig von der Richtung des ALE-Flows.

Die erneute Autorisierung eines ALE-Flows wird durch Folgendes ausgelöst:

-   Eine Richtlinien Änderung auf der Ebene, an der der ALE Flow ursprünglich autorisiert oder erstellt wurde.
-   Eine Ankunfts Schnittstelle unterscheidet sich von der Schnittstelle, an der der ALE Flow ursprünglich autorisiert oder erstellt wurde.
-   Eine ausstehende Verbindung.

Die erneute Autorisierung unterscheidet sich von der anfänglichen Autorisierung durch das vorhanden sein des Flag " [**\_ \_ \_ \_ Reauthorization**](filtering-condition-flags-.md) " der Sdn-Bedingung.

Eine erneute Autorisierung kann nur auf der Ebene der Authentifizierungs Stufen der Ebene der Authentifizierungs Stufe " [**\_ \_ \_ \_ \_ \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) " und der Ebene "f" der **Ebene " \_ \_ \_ \_ \_ v {4 \| 6}** " durchgeführt werden.

### <a name="policy-change-reauthorization"></a>Neuautorisierung von Richtlinien ändern

Eine Richtlinien Änderung wird als hinzufügen oder Entfernen von Filtern auf der Ebene "ALE" implementiert. Sobald eine Richtlinien Änderung erkannt wird, wird das erste Paket, das einen auf der betroffenen Ebene erstellten ALE-Datenfluss durchsucht, für die erneute Autorisierung der Ebene angegeben. Aus diesem Grund ist es für eine erneute Autorisierung durchaus möglich, dass ein Ausgeh Endes Paket auf der Ebene der Ebene [**\_ \_ \_ auth \_ recv \_ Accept \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) auf der Ebene der Ebene der vollständigen Ebene klassifiziert wird und dass ein eingehender Paket auf der Ebene der Ebene der Ebene der Ebene der Ebene der Ebene " **f \_ \_ \_ \_ \_ {4 \| 6}** " der Ebene

Ein Grund für diese Klassifizierung mit gemischter Richtung ist, dass es möglicherweise keinen weiteren Netzwerk Datenverkehr aus der ursprünglichen Richtung gibt (z. b. eingehender Paket für eingehenden Datenfluss). Ein Beispiel hierfür ist ein unidirektionales UDP-Streaming nach einem anfänglichen bidirektionalen Hand Shake. In diesem Fall ist es wünschenswert, das Streaming so bald wie möglich zu beenden.

### <a name="arrival-interface-reauthorization"></a>Erneute Autorisierung der Ankunfts Schnittstelle

Die erneute Autorisierung der Ankunfts Schnittstelle ist ab Windows Server 2008 und Windows Vista mit Service Pack 1 (SP1) verfügbar.

Pakete, die dem gleichen ALE Datenfluss angehören, können von mehreren Schnittstellen eintreffen. Das erste Paket, das über eine Schnittstelle übertragen wird, die sich von der ursprünglichen Schnittstelle des ALE-Flows unterscheidet, wird erneut autorisiert

Bei einem starken Host Modell, bei dem es sich um das Standard Sicherheitsmodell für den TCP/IP-Stapel handelt, werden bei einer Verbindung an einer Netzwerkschnittstelle nur Pakete akzeptiert, die in derselben Schnittstelle enthalten sind. Daher wird die erneute Autorisierung der Ankunfts Schnittstelle auf einem starken Host Computer nicht verwendet.

Bei einem schwachen Host Modell ermöglicht eine Verbindung mit einer Netzwerkschnittstelle das eingehen von Paketen an einer beliebigen anderen Netzwerkschnittstelle. Die erneute Autorisierung der Ankunfts Schnittstelle wird auf einem schwachen Host Computer verwendet, um Schnittstellen spezifische Richtlinien zu implementieren. Weitere Informationen finden Sie unter ["The Cable Guy: strong and Weak Host Models".](/previous-versions/technet-magazine/cc137807(v=msdn.10))

Bei der erneuten Autorisierung sind möglicherweise einige [klassifizierbare Felder](filtering-conditions.md) unbekannt. Wenn z. b. ein ausgehendes Paket auf der fwpm-Schicht der Ebene-Authentifizierung für die [**\_ Ebene " \_ \_ \_ \_ Accept \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) " erneut autorisiert wird, sind alle Felder in Bezug auf die Ankunfts Schnittstelle unbekannt. In diesem Fall werden die Werte der unbekannten Felder als [**FWP \_ empty**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)angegeben.

Felder vom Typ " [**f" \_ leer**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) können mit der [**Übereinstimmung mit der \_ Übereinstimmung \_**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type)von "f. Aus diesem Grund kann eine Richtlinie festgelegt werden, um reautorisierungen zu blockieren und einen ALE-Datenfluss zu beenden, wenn Anforderungen zur erneuten Autorisierung für den ALE-Flow eintreffen.

## <a name="pending-connection-reauthorization"></a>Erneute Autorisierung der Verbindung steht aus

Ein Legenden-Treiber kann einen klassifizier Vorgang auf ALE Ebenen verschieben und ihn zu einem späteren Zeitpunkt vervollständigen, wenn die Filter Entscheidung sicher getroffen werden kann. Die Funktionen zum Verschieben/vervollständigen von ALE werden über die kernelmodusfunktionen [FwpsPendOperation0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpspendoperation0) und [FwpsCompleteOperation0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpscompleteoperation0)unterstützt.

Die erneute Autorisierung wird unmittelbar nach dem Aufruf von FwpsCompleteOperation0 ausgelöst und ermöglicht es dem Legenden Treiber, den Flow zuzulassen oder zu blockieren.

Nur eine anfängliche Autorisierung kann verschoben werden. Ein FwpsPendOperation0-Aufrufe schlägt fehl, wenn das FWP-Bedingungs Kennzeichen [**\_ \_ \_ \_ reautorisierungsflag ist**](filtering-condition-flags-.md) festgelegt ist.

Weitere Informationen finden Sie in der Dokumentation zum [Windows-Treiberkit](/windows-hardware/drivers/ddi/_netvista/) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Durchsetzung der Anwendungsschicht (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[ALE Ebenen](ale-layers.md)
</dt> <dt>

[Status behaftete ALE Filterung](ale-stateful-filtering.md)
</dt> <dt>

[ALE Multicast-/Broadcast Datenverkehr](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Anpassung des ALE-Flows](ale-flow-customization.md)
</dt> </dl>

 

 