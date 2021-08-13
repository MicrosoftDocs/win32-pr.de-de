---
description: Initialisieren Media Foundation
ms.assetid: e4db81d3-7a9e-47d7-8611-6dac8026259c
title: Initialisieren Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 202ab57db5821b252001a723eb8765493eb86362111da5c54e5e16e9fca4219a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119268920"
---
# <a name="initializing-media-foundation"></a>Initialisieren Media Foundation

Vor der Verwendung Microsoft Media Foundation Objekte oder Schnittstellen müssen Sie die [**MFStartup-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) aufrufen. Übergeben Sie die konstante **\_ MF-VERSION**.


```C++
    hr = MFStartup(MF_VERSION);
```



Die [**MFStartup-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) initialisiert die Media Foundation Plattform. Wenn **MFStartup** MF E BAD STARTUP VERSION zurückgibt, bedeutet dies, dass Ihre Anwendung mit einer Version der Media Foundation-Header kompiliert wurde, die nicht mit den \_ \_ \_ Media Foundation-DLLs auf Ihrem System \_ übereinstimmen.

Für jeden Aufruf von [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup)muss Ihre Anwendung [**MFShutdown aufrufen.**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown)


```C++
MFShutdown();
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-Architektur](media-foundation-architecture.md)
</dt> <dt>

[Media Foundation-Plattform-APIs](media-foundation-platform-apis.md)
</dt> </dl>

 

 



