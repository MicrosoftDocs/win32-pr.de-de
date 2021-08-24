---
title: ALE Multicast-/Broadcastdatenverkehr
description: Der gesamte eingehende Multicast- und Broadcastdatenverkehr auf den ALE-Ebenen (Application Layer Enforcement) wird einem globalen ALE-Flow zugeordnet.
ms.assetid: b10b9758-8fce-4256-a25d-917e01336456
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2849f7277cc9ada580bca22fa5a4fdf618d959d255b442607963047dd2a37bba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315610"
---
# <a name="ale-multicastbroadcast-traffic"></a>ALE Multicast-/Broadcastdatenverkehr

Der gesamte eingehende Multicast- und Broadcastdatenverkehr auf den ALE-Ebenen (Application Layer Enforcement) wird einem globalen [ALE-Fluss](ale-stateful-filtering.md)zugeordnet. Der Antwortdatenverkehr für eingehende Multicast- und Broadcastpakete wird auf der [**Ebene FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) klassifiziert, und für jede Antwort werden separate ALE-Flows erstellt.

Ausgehender Multicast- und Broadcastdatenverkehr auf den ALE-Ebenen erstellt einen ALE-Fluss von 4 Sekunden. Standardmäßig lässt die Autorisierung eines ausgehenden Multicast- oder Broadcast-ALE-Pakets eingehenden Datenverkehr von einer beliebigen Remoteadresse für bis zu 4 Sekunden zu, egal ob Unicast, Multicast oder Broadcast. Ein solcher ALE-Flow kann nur durch nachfolgenden ausgehenden Datenverkehr aktualisiert oder beibehalten werden, der dem ALE-Flow entspricht.

> [!Note]  
> Die Lebensdauer von 4 Sekunden wird von der integrierten [**FWPM \_ CALLOUT \_ SET OPTIONS \_ \_ AUTH CONNECT LAYER \_ \_ \_ V{4 \| 6}**](built-in-callout-identifiers.md)angegeben. Um die Standardlebensdauer von 4 Sekunden zu ändern, fügen Sie einen Filter hinzu, der auf die **FWPM \_ CALLOUT \_ SET OPTIONS \_ \_ AUTH CONNECT LAYER \_ \_ \_ V{4 \| 6}-Aufrufliste** verweist. Weitere Informationen finden [Sie unter ALE-Flow Anpassung.](ale-flow-customization.md)

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungsschichterzwingung (Application Layer Enforcement, ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[ALE-Ebenen](ale-layers.md)
</dt> <dt>

[Zustandsbehaftete ALE-Filterung](ale-stateful-filtering.md)
</dt> <dt>

[Erneute ALE-Autorisierung](ale-re-authorization.md)
</dt> <dt>

[Anpassung von ALE Flow](ale-flow-customization.md)
</dt> </dl>

 

 




