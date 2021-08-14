---
description: In diesem Beispiel wird veranschaulicht, wie ein Array von Sicherheitspuffern initialisiert wird.
ms.assetid: f8196a9c-786a-49a3-85a4-1bd5f414a653
title: SecBuffer- und SecBufferDesc-Beispielcode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b60b776dd85e29c3f91d2840849d18e48d100dada6037bff556074b1041bdb8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918447"
---
# <a name="secbuffer-and-secbufferdesc-example-code"></a>SecBuffer- und SecBufferDesc-Beispielcode

In diesem Beispiel wird veranschaulicht, wie ein Array von Sicherheitspuffern initialisiert wird. Es zeigt Eingabesicherheitspuffer an, die von der Serverseite einer Verbindung initialisiert wurden, um sich auf einen Aufruf von [**AcceptSecurityContext (Allgemein)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)vorzubereiten. Beachten Sie, dass der letzte Puffer das nicht transparente Sicherheitstoken enthält, das vom Client empfangen wurde, und dass das SECBUFFER \_ READONLY-Flag für [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)festgelegt ist.


```C++
SecBuffer  Buffers[3];
SecBufferDesc BufferDesc;
BYTE *pHeader;
BYTE *pMessage;
BYTE *pTrailer;

//--------------------------------------------------------------------
// pHeader, pMessage, and pTrailer are BYTE strings.
// In a working program, they would be assigned string values.

BufferDesc.ulVersion = SECBUFFER_VERSION;
BufferDesc.cBuffers = 3;
BufferDesc.pBuffers = Buffers;

Buffers[0].cbBuffer = sizeof(pHeader);
Buffers[0].BufferType = SECBUFFER_READONLY | SECBUFFER_DATA;
Buffers[0].pvBuffer = pHeader;

Buffers[1].cbBuffer = sizeof(pMessage);
Buffers[1].BufferType = SECBUFFER_DATA;
Buffers[1].pvBuffer = pMessage;

Buffers[2].cbBuffer = sizeof(pTrailer);
Buffers[2].BufferType = SECBUFFER_READONLY | SECBUFFER_TOKEN;
Buffers[2].pvBuffer = pTrailer;
```



 

 
