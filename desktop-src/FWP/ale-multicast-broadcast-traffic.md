---
title: ALE Multicast-/Broadcast Datenverkehr
description: Alle eingehenden Multicast-und Broadcast Datenverkehr auf der Ebene (Application Layer Enforcement) werden einem globalen ALE-Datenfluss zugeordnet.
ms.assetid: b10b9758-8fce-4256-a25d-917e01336456
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30b56a6e2a27a209baf66d34948b704ae321644
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309895"
---
# <a name="ale-multicastbroadcast-traffic"></a>ALE Multicast-/Broadcast Datenverkehr

Alle eingehenden Multicast-und Broadcast Datenverkehr auf der Ebene (Application Layer Enforcement) werden einem globalen [ALE](ale-stateful-filtering.md)-Datenfluss zugeordnet. Der Antwort Datenverkehr für eingehende Multicast-und Broadcast Pakete wird auf der Ebene der Ebene der Ebene der swpm-Layer-Authentifizierung (x [**\_ \_ \_ \_ \_ {4 \| 6}**](management-filtering-layer-identifiers-.md) ) klassifiziert, und für jede Antwort werden separate ALE-Flows erstellt.

Ausgehender Multicast-und Broadcast Datenverkehr auf der ALE-Ebene erstellt einen 4-Sekunden-ALE Datenfluss. Standardmäßig lässt die Autorisierung eines ausgehenden Multicast-oder Broadcast-ALE-Pakets eingehenden Datenverkehr, ob Unicast, Multicast oder Broadcast, von einer beliebigen Remote Adresse bis zu 4 Sekunden zu. Ein solcher ALE Datenfluss kann nur durch nachfolgenden ausgehenden Datenverkehr, der mit dem Datenfluss übereinstimmt, aktualisiert oder aufrechterhalten werden.

> [!Note]  
> Die 4-Sekunden-Lebensdauer wird durch die integrierte Legenden-Legenden Optionen zum Festlegen der abrufsschout- [**\_ \_ \_ Optionen \_ auth \_ Connect \_ Layer \_ V {4 \| 6}**](built-in-callout-identifiers.md)festgelegt. Um die Standard Lebensdauer von 4 Sekunden zu ändern, fügen Sie einen Filter hinzu, der auf die **fwpm-Legenden \_ Set- \_ \_ Optionen \_ auth \_ Connect \_ Layer \_ V {4 \| 6}** Legende verweist. Weitere Informationen finden Sie unter [ALE Fluss Anpassung](ale-flow-customization.md) .

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Durchsetzung der Anwendungsschicht (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[ALE Ebenen](ale-layers.md)
</dt> <dt>

[Status behaftete ALE Filterung](ale-stateful-filtering.md)
</dt> <dt>

[Erneute ALE-Autorisierung](ale-re-authorization.md)
</dt> <dt>

[Anpassung des ALE-Flows](ale-flow-customization.md)
</dt> </dl>

 

 




