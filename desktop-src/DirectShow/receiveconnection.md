---
description: ReceiveConnection
ms.assetid: 90a6a09a-95e1-4adf-8e0b-269f971aaa67
title: ReceiveConnection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55a8a91cbf9870d6c53592ff823f710eb5875fa939592309425df0a0bca6f0e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072764"
---
# <a name="receiveconnection"></a>ReceiveConnection

Mit diesem Mechanismus kann ein Ausgabepin eine Formatänderung an seinen Downstream-Peer vorschlagen, wenn das neue Format einen größeren Puffer erfordert. Der Ausgabepin führt Folgendes aus:

1.  Ruft [**IPin::ReceiveConnection für**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) den Downstreameingabepin auf.
2.  Wenn `ReceiveConnection` erfolgreich ist, ruft [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) auf dem Eingabepin auf.

Darüber hinaus muss der Ausgabepin möglicherweise [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) aufrufen und dann denCommit für die Zuweisung decommitieren und erneut zuweisen, um die Puffergrößen zu ändern. Stellen Sie sicher, dass Alle ausstehenden Stichproben im alten Format vorliegen, bevor Sie die Puffergröße ändern.

Einige MPEG-2-Decoder verwenden diesen Mechanismus, um zwischen DER MPEG-1- und MPEG-2-Ausgabe zu wechseln oder wenn sich die Videogröße ändert.

 

 



