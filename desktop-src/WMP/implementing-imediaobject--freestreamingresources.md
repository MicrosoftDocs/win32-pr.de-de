---
title: Implementieren von imediaobject-freestreamingresources
description: Implementieren von imediaobject-freestreamingresources
ms.assetid: 970dd10b-a7a0-4ba0-97e3-725d5c914500
keywords:
- Windows Media Player-Plug-ins, Echo Sample Streaming Resources
- Plug-ins, Echo Sample Streaming-Ressourcen
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample Streaming-Ressourcen
- DSP-Plug-ins, Echo Sample Streaming-Ressourcen
- Echo DSP-Plug-in-Beispiel, Streamingressourcen
- Echo DSP-Plug-in-Beispiel, Freigeben von Arbeitsspeicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a31a293cfc68caf43496d031426de2441c9c1d05
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855803"
---
# <a name="implementing-imediaobjectfreestreamingresources"></a>Implementieren von imediaobject:: freestreamingresources

Es ist wichtig, dass Ihr Code jeden zugeordneten Arbeitsspeicher freigibt, bevor das Plug-in-Objekt zerstört wird. Windows Media Player ruft **freestreamingresources** auf, um dies zu ermöglichen. Aus Sicherheitsgründen enthält das Beispiel **, das vom** Plug-in-Assistenten erstellt wurde, einen aufzurufenden **freestreamingresources** -Befehl, um sicherzustellen, dass der Arbeitsspeicher freigegeben wird. Sie müssen den folgenden Code für das Echo-Beispiel zu " **freestreamingresources** " hinzufügen:


```
// Test whether a buffer exists.
if (m_pbDelayBuffer)
{
    delete m_pbDelayBuffer;
    m_pbDelayBuffer = NULL;
    m_pbDelayPointer = NULL;
    m_cbDelayBuffer = 0;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Arbeiten mit Streamingressourcen**](working-with-streaming-resources.md)
</dt> </dl>

 

 




