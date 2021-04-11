---
description: Medien Erkennung (mediadet)
ms.assetid: 5cdbb6ca-d2c3-4123-b545-198863fed25f
title: Medien Erkennung (mediadet)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f34b1dc267480d3d6ea9efe9b9a743623a917b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104132173"
---
# <a name="media-detector-mediadet"></a>Medien Erkennung (mediadet)

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Das Media Detector-Objekt (mediadet) ruft Formatierungsinformationen ab und gibt weiterhin Frames aus Datei Quellen aus. Der Filter Graph-Manager muss vom Medien Erkennungs Modul nicht funktionieren. Um dieses Objekt zu erstellen, rufen Sie **cokreateinstance** auf. Der Klassen Bezeichner ist CLSID \_ mediadet.

Um Windows Media™-Dateien zu lesen, muss die Anwendung ein Software Zertifikat bereitstellen, das auch als Schlüssel bezeichnet wird. Registrieren Sie die Anwendung als Schlüssel Anbieter über die **IObjectWithSite** -Schnittstelle des Medien Detektors. Weitere Informationen finden Sie unter [Entsperren des Windows Media-Format](unlocking-the-windows-media-format-sdk.md)-SDKs.

Das mediadet-Objekt macht die folgenden Schnittstellen verfügbar:

-   [**Imediadet**](imediadet.md)
-   **IObjectWithSite**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Quellen](working-with-sources.md)
</dt> </dl>

 

 



