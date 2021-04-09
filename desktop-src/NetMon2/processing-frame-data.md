---
description: Im folgenden Beispielcode legt der Monitor einen Aufzeichnungs Filter fest, der nur die IP-Adresse und die angeforderten Protokolldaten angibt.
ms.assetid: 0945bceb-b5fe-4f07-866b-4e0468227610
title: Verarbeiten von Frame-Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41c49de62d630033aa7d3ed3e8e115fd1a02f7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959489"
---
# <a name="processing-frame-data"></a><span data-ttu-id="b314f-103">Verarbeiten von Frame-Daten</span><span class="sxs-lookup"><span data-stu-id="b314f-103">Processing Frame Data</span></span>

<span data-ttu-id="b314f-104">Im folgenden Beispielcode legt der Monitor einen Aufzeichnungs Filter fest, der **nur die IP-Adresse** und die angeforderten Protokolldaten angibt.</span><span class="sxs-lookup"><span data-stu-id="b314f-104">In the following example code, the monitor sets a capture filter that specifies **IP only** and requested protocol data.</span></span>


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



 

 



