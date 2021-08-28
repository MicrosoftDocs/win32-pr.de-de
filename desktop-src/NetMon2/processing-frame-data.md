---
description: Im folgenden Beispielcode legt der Monitor einen Erfassungsfilter fest, der nur IP-Adressen und angeforderte Protokolldaten angibt.
ms.assetid: 0945bceb-b5fe-4f07-866b-4e0468227610
title: Verarbeiten von Framedaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a103dd2fea564eb6eb93ffcb32d5c21acbe991d515b7e75f287786dbce976c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995430"
---
# <a name="processing-frame-data"></a>Verarbeiten von Framedaten

Im folgenden Beispielcode legt der Monitor einen Erfassungsfilter fest, der nur **IP-Adressen** und angeforderte Protokolldaten angibt.


```C++
STDMETHODIMP CTestMon::OnFrames(UPDATE_EVENT Event)
{
    DWORD i;
    LPFRAMETABLE lpFrameTable = Event.lpFrameTable;

    // The frame table can wrap the indexes.
    for (
      i = lpFrameTable->StartIndex; 
      i != lpFrameTable->EndIndex; 
     (i == lpFrameTable->FrameTableLength ) ? i=0: i ++ )
    {
        LPFRAME_DESCRIPTOR lpFrameDesc = &lpFrameTable->Frames[i];
        
        // Cast the frame data to an unaligned pointer to an IP  
        // structure. A try/catch block could be a workaround, but
        // if the capture filter is set correctly, this is the
        // verifiable IP.
        ULPIP ulpIP = (ULPIP)(&lpFrameDesc->FramePointer[lpFrameDesc->LowProtocolOffset]);
        // Now examine the IP frame.
    }
    return NOERROR;
}
```



 

 



