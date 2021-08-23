---
title: Implementieren von IMediaObject FreeStreamingResources
description: Implementieren von IMediaObject FreeStreamingResources
ms.assetid: 970dd10b-a7a0-4ba0-97e3-725d5c914500
keywords:
- Windows Media Player-Plug-Ins, Echo-Beispielstreamingressourcen
- Plug-Ins, Echo-Beispielstreamingressourcen
- Digitale Signalverarbeitungs-Plug-Ins, Echo-Beispielstreamingressourcen
- DSP-Plug-Ins, Echo-Beispielstreamingressourcen
- Echo-DSP-Plug-In-Beispiel, Streamingressourcen
- Echo-DSP-Plug-In-Beispiel, Freigeben von Arbeitsspeicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30da5f92ec8420ccc90f74256003aae02664a57a8ffad3470901f672cf37aa73
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119617320"
---
# <a name="implementing-imediaobjectfreestreamingresources"></a>Implementieren von IMediaObject::FreeStreamingResources

Es ist wichtig, dass Ihr Code jeglichen zugeordneten Arbeitsspeicher freigibt, bevor das Plug-In-Objekt zerstört wird. Windows Media Player ruft **FreeStreamingResources** auf, um dies zu ermöglichen. Aus Sicherheitsgründen enthält das vom Plug-In-Assistenten erstellte Beispiel einen Aufruf von **FreeStreamingResources** in der **FinalRelease-Methode,** um sicherzustellen, dass der Arbeitsspeicher freigegeben wird. Sie müssen **freeStreamingResources** den folgenden Code für das Echo-Beispiel hinzufügen:


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

 

 




