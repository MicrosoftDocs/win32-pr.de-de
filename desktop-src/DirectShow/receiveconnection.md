---
description: Receiveconnection
ms.assetid: 90a6a09a-95e1-4adf-8e0b-269f971aaa67
title: Receiveconnection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80fd9fe31f87a34dc3bfdfc4ecfb532255138b9c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124670"
---
# <a name="receiveconnection"></a>Receiveconnection

Dieser Mechanismus ermöglicht es einer Ausgabepin, eine Formatänderung an den downstreampeer vorzuschlagen, wenn das neue Format einen größeren Puffer erfordert. Die Ausgabe-PIN führt folgende Aktionen aus:

1.  Ruft [**IPin:: receiveconnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) für die downstreameingabepin auf.
2.  Wenn `ReceiveConnection` erfolgreich ist, wird [**IMemInputPin:: notifyzuweisung**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) für die Eingabe-PIN aufgerufen.

Außerdem muss die Ausgabepin möglicherweise [**imemzucator:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) aufrufen und dann die Zuweisung Decommit und erneut ausführen, um die Puffergrößen zu ändern. Stellen Sie sicher, dass Sie alle ausstehenden Beispiele im alten Format bereitstellen, bevor Sie die Puffergröße ändern.

Einige MPEG-2-Decoder verwenden diesen Mechanismus, um zwischen MPEG-1-und MPEG-2-Ausgabe zu wechseln oder die Videogröße zu ändern.

 

 



