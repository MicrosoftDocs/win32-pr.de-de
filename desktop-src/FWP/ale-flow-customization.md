---
title: Anpassung des ALE-Flows
description: Die Netzwerk Filterung auf der Ebene (Application Layer Enforcement, ALE) der Windows-Filter Plattform (WFP) kann durch Hinzufügen von Filtern mit bestimmten Klassifikations Optionen angepasst werden.
ms.assetid: 123af237-cf42-410b-8a2f-c011cb5f4f19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9843a60719f424403139885f24f165c0dd936b
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104314368"
---
# <a name="ale-flow-customization"></a>Anpassung des ALE-Flows

Die Netzwerk Filterung auf der Ebene (Application Layer Enforcement, ALE) der Windows-Filter Plattform (WFP) kann durch Hinzufügen von Filtern mit bestimmten Klassifikations Optionen angepasst werden.

## <a name="multicastbroadcast-traffic"></a>Multicast/Broadcast-Datenverkehr

Fügen Sie zum Blockieren von eingehendem Datenverkehr, der auf ausgehenden Multicast-oder Broadcast Zuständen basiert, einen Filter hinzu, der ausgehenden Multicast-und Broadcast Datenverkehr autorisiert, und für die die FWP-Option " [**\_ \_ \_ Multicast- \_ Status**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) " auf **FWP- \_ Option \_ Wert " \_ \_ Multicast \_ Status ablehnen**"

## <a name="remote-peers"></a>Remote Peers

Fügen Sie einen Filter mit der Option FWP-klassifizieren, wenn die Option freie [**\_ \_ \_ \_ Quell \_ Zuordnung**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) **aktivieren auf FWP- \_ Option \_ Wert \_ \_ lose \_ Quell \_ Zuordnung aktivieren** festgelegt ist, um Antwort Pakete von unterschiedlichen Peers dem gleichen Datenfluss hinzuzufügen.

Siehe [Verwenden von klassifizier Optionen](using-classify-options.md) für Codebeispiele.

## <a name="ale-flow-lifetime"></a>ALE Fluss Lebensdauer

Fügen Sie zum Ändern der Leerlauf Timeout Werte für einen ALE-Datenfluss einen Filter mit der Option [**FWP- \_ klassifizieren- \_ Option \_ mcast \_ Bcast \_ Lifetime**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) und/oder der Option **\_ \_ \_ \_ unicastlebensdauer für die FWP-klassifizier Option** auf den gewünschten Leerlauf Timeout Wert fest.

Siehe [Verwenden von klassifizier Optionen](using-classify-options.md) für ein Codebeispiel.

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

[Erneute ALE-Autorisierung](ale-re-authorization.md)
</dt> <dt>

[Verwenden von klassifizier Optionen](using-classify-options.md)
</dt> </dl>

 

 




