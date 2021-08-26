---
description: Die folgende Headerdatei sollte sowohl im Client als auch in den SSPI-Beispielen des Servers als SspiExample.h enthalten sein. Sie deklariert Funktionen, die die Kommunikation mit dem Sicherheitspaket verarbeiten.
ms.assetid: 358c2cd6-674b-4d70-9657-800b0d1b2fe7
title: Headerdatei für SSPI-Client und -Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ba76283b2686ecde8a6e453c5c376f8589a78dccf9e740b381f89fc5ef4db21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101280"
---
# <a name="header-file-for-sspi-client-and-server"></a>Headerdatei für SSPI-Client und -Server

Die folgende Headerdatei sollte sowohl im Client als auch in den SSPI-Beispielen des Servers als SspiExample.h enthalten sein. Sie deklariert Funktionen, die die Kommunikation mit dem Sicherheitspaket verarbeiten.


```C++
//  SspiExample.h
#include <sspi.h>
#include <windows.h>

BOOL SendMsg (SOCKET s, PBYTE pBuf, DWORD cbBuf);
BOOL ReceiveMsg (SOCKET s, PBYTE pBuf, DWORD cbBuf, DWORD *pcbRead);
BOOL SendBytes (SOCKET s, PBYTE pBuf, DWORD cbBuf);
BOOL ReceiveBytes (SOCKET s, PBYTE pBuf, DWORD cbBuf, DWORD *pcbRead);
void cleanup();

BOOL GenClientContext (
    BYTE *pIn,
    DWORD cbIn,
    BYTE *pOut,
    DWORD *pcbOut,
    BOOL *pfDone,
    CHAR *pszTarget,
    CredHandle *hCred,
    struct _SecHandle *hcText
);

BOOL GenServerContext (
   BYTE *pIn,
   DWORD cbIn,
   BYTE *pOut,
   DWORD *pcbOut,
   BOOL *pfDone,
   BOOL  fNewCredential
);

BOOL EncryptThis (
         PBYTE pMessage, 
         ULONG cbMessage,
         BYTE ** ppOutput,
         LPDWORD pcbOutput,
         ULONG securityTrailer
    );

PBYTE DecryptThis(
         PBYTE achData, 
         LPDWORD pcbMessage,
         struct _SecHandle *hCtxt,
         ULONG   cbSecurityTrailer
);

BOOL 
SignThis (
         PBYTE pMessage, 
         ULONG cbMessage,
         BYTE ** ppOutput,
         LPDWORD pcbOutput
);

PBYTE VerifyThis(
          PBYTE pBuffer, 
          LPDWORD pcbMessage,
          struct _SecHandle *hCtxt,
          ULONG   cbMaxSignature
);

void PrintHexDump(DWORD length, PBYTE buffer);

BOOL ConnectAuthSocket (
   SOCKET *s, 
   CredHandle *hCred, 
   struct _SecHandle *hcText
);

BOOL CloseAuthSocket (SOCKET s);

BOOL DoAuthentication (SOCKET s);

void MyHandleError(char *s);

```



 

 



