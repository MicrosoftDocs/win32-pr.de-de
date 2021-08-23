---
title: ALE Flow Anpassung
description: Die Netzwerkfilterung auf den ALE-Ebenen (Application Layer Enforcement) der Windows Filtering Platform (WFP) kann angepasst werden, indem Filter mit bestimmten Klassifizierungsoptionen hinzugefügt werden.
ms.assetid: 123af237-cf42-410b-8a2f-c011cb5f4f19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbe42a6df32bc69ba454226eb113cb43756224daaf752c3925f1f2d3bacd7650
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951369"
---
# <a name="ale-flow-customization"></a>ALE Flow Anpassung

Die Netzwerkfilterung auf den ALE-Ebenen (Application Layer Enforcement) der Windows Filtering Platform (WFP) kann angepasst werden, indem Filter mit bestimmten Klassifizierungsoptionen hinzugefügt werden.

## <a name="multicastbroadcast-traffic"></a>Multicast-/Broadcastdatenverkehr

Um eingehenden Datenverkehr basierend auf ausgehenden Multicast- oder Broadcastzuständen zu blockieren, fügen Sie einen Filter hinzu, der ausgehenden Multicast- und Broadcastdatenverkehr autorisiert und für den die [**Option FWP \_ CLASSIFY OPTION \_ \_ MULTICAST \_ STATE**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) auf **FWP OPTION VALUE \_ \_ \_ DENY \_ MULTICAST \_ STATE** festgelegt ist.

## <a name="remote-peers"></a>Remote-Peers

Um Antwortpakete von verschiedenen Peers demselben ALE-Flow hinzuzufügen, fügen Sie einen Filter hinzu, bei dem die [**Option FWP \_ CLASSIFY OPTION LOOSE SOURCE \_ \_ \_ \_ MAPPING**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) auf FWP OPTION VALUE ENABLE LOOSE SOURCE MAPPING festgelegt **\_ \_ \_ \_ \_ \_ ist.**

Ein [Codebeispiel finden Sie unter](using-classify-options.md) Verwenden von Klassifizieren von Optionen.

## <a name="ale-flow-lifetime"></a>ALE Flow Lebensdauer

Um die Leerlauf-Timeoutwerte für einen ALE-Flow zu ändern, fügen Sie einen Filter hinzu, bei dem die [**Option FWP \_ CLASSIFY OPTION \_ \_ MCAST \_ BCAST \_ LIFETIME**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) und/oder **die Option FWP CLASSIFY OPTION \_ \_ \_ UNICAST \_ LIFETIME** auf den gewünschten Leerlauf-Timeoutwert festgelegt ist.

Ein [Codebeispiel finden Sie unter](using-classify-options.md) Verwenden von Klassifizieren von Optionen.

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

[Erneute ALE-Autorisierung](ale-re-authorization.md)
</dt> <dt>

[Verwenden von Klassifizieren von Optionen](using-classify-options.md)
</dt> </dl>

 

 




