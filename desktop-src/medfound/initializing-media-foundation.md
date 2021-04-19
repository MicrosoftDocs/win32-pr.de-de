---
description: Media Foundation wird initialisiert.
ms.assetid: e4db81d3-7a9e-47d7-8611-6dac8026259c
title: Media Foundation wird initialisiert.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb876ec3493d6c4fac1c2f6d6757ef647c511a98
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106363892"
---
# <a name="initializing-media-foundation"></a>Media Foundation wird initialisiert.

Vor der Verwendung von Microsoft Media Foundation-Objekten oder-Schnittstellen müssen Sie die [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) -Funktion aufruft. Übergeben Sie die Konstante **MF- \_ Version**.


```C++
    hr = MFStartup(MF_VERSION);
```



Die [**MF Startup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) -Funktion initialisiert die Media Foundation Plattform. Wenn **MF Startup** eine Fehler \_ hafte \_ Start Version von MF E zurückgibt \_ \_ , bedeutet dies, dass Ihre Anwendung mit einer Version der Media Foundation-Header kompiliert wurde, die nicht mit den Media Foundation DLLs auf dem System identisch ist.

Für jeden [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup)-Rückruf muss Ihre Anwendung [**mfshutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown)aufgerufen werden.


```C++
MFShutdown();
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-Architektur](media-foundation-architecture.md)
</dt> <dt>

[Media Foundation Plattform-APIs](media-foundation-platform-apis.md)
</dt> </dl>

 

 



