---
description: In diesem Beispiel wird veranschaulicht, wie ein Array von Sicherheits Puffern initialisiert wird.
ms.assetid: f8196a9c-786a-49a3-85a4-1bd5f414a653
title: Beispiel Code für secbuffer und secbufferdesc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee7d28e885d6eec65c209caeda299b2f7e5f2ad3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358427"
---
# <a name="secbuffer-and-secbufferdesc-example-code"></a>Beispiel Code für secbuffer und secbufferdesc

In diesem Beispiel wird veranschaulicht, wie ein Array von Sicherheits Puffern initialisiert wird. Es werden Eingabe Sicherheitspuffer angezeigt, die von der Serverseite einer Verbindung initialisiert wurden, um einen [**calltsecuritycontext (allgemein)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)aufzurufen. Beachten Sie, dass der letzte Puffer das nicht transparente Sicherheits Token enthält, das vom Client empfangen wurde, und dass das Flag "Schreib geschützter Schlüssel für secbuffer" \_ für [**secbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)festgelegt ist


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



 

 
