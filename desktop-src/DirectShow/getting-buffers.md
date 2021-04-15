---
description: Puffer werden erhalten.
ms.assetid: be61aee9-41d5-42bc-b905-d0216d301faf
title: Puffer werden erhalten.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf516096397eca1fce3a023ee4987d8e8feaa4b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520539"
---
# <a name="getting-buffers"></a>Puffer werden erhalten.

Wenn der Filter über eine benutzerdefinierte Zuweisung verfügt, die Filter Ressourcen verwendet, sollte die [**imemzuzuordcator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) -Methode des zuordcators die streamingsperre wie andere Streamingmethoden enthalten:


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

 

 



