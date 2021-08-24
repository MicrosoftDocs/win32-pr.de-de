---
description: Abrufen von Puffern
ms.assetid: be61aee9-41d5-42bc-b905-d0216d301faf
title: Abrufen von Puffern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f727045142b9432da93511ecea1f3238aa24ad213fdc7715f5e2e45a91ab19a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536900"
---
# <a name="getting-buffers"></a>Abrufen von Puffern

Wenn Ihr Filter über eine benutzerdefinierte Zuweisung verfügt, die Filterressourcen verwendet, sollte die [**IMemAllocator::GetBuffer-Methode**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) der Zuweisung die Streamingsperre wie bei anderen Streamingmethoden halten:


```C++
HRESULT CMyInputAllocator::GetBuffer(
    IMediaSample **ppBuffer,
    REFERENCE_TIME *pStartTime, 
    REFERENCE_TIME *pEndTime,
    DWORD dwFlags)
{
    CAutoLock cObjectLock(&m_csReceive);

    /* Use resources. */

    return CMemAllocator::GetBuffer(ppBuffer, pStartTime, pEndTime, dwFlags);    
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Threads und kritische Abschnitte](threads-and-critical-sections.md)
</dt> </dl>

 

 



