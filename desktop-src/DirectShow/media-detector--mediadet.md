---
description: Medienerkennung (MediaDet)
ms.assetid: 5cdbb6ca-d2c3-4123-b545-198863fed25f
title: Medienerkennung (MediaDet)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a072a5d70cf392a1b81fc8387d976bea1db2ddaa5ca2328df914be96a791d19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684970"
---
# <a name="media-detector-mediadet"></a>Medienerkennung (MediaDet)

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Das MediaDet-Objekt (Media Detector) ruft Formatinformationen ab und framest weiterhin aus Dateiquellen. Die Medienerkennung erfordert nicht, dass der Filter Graph Manager funktioniert. Um dieses Objekt zu erstellen, rufen Sie **CoCreateInstance** auf. Der Klassenbezeichner ist CLSID \_ MediaDet.

Zum Lesen Windows Media™-Dateien muss die Anwendung ein Softwarezertifikat bereitstellen, das auch als Schlüssel bezeichnet wird. Registrieren Sie die Anwendung über die **IObjectWithSite-Schnittstelle** von Media Detector als Schlüsselanbieter. Weitere Informationen finden Sie unter [Entsperren des Windows Media Format SDK.](unlocking-the-windows-media-format-sdk.md)

Das MediaDet-Objekt macht die folgenden Schnittstellen verfügbar:

-   [**IMediaDet**](imediadet.md)
-   **Iobjectwithsite**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Quellen](working-with-sources.md)
</dt> </dl>

 

 



