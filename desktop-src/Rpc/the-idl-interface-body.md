---
title: Der IDL-Schnittstellen Text
description: Der IDL-Schnittstellen Text enthält Datentypen, die in Remote Prozedur aufrufen und den Funktionsprototypen für die Remote Prozeduren verwendet werden.
ms.assetid: b07524a7-b27e-4ea2-ae34-068c07d9a444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 565cbe6493bd865030b77b5e9ef6275b444ca451
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728672"
---
# <a name="the-idl-interface-body"></a>Der IDL-Schnittstellen Text

Der IDL-Schnittstellen Text enthält Datentypen, die in Remote Prozedur aufrufen und den Funktionsprototypen für die Remote Prozeduren verwendet werden. Der Schnittstellen Text kann auch Importe, Pragmas, Konstante Deklarationen und Typdeklarationen enthalten. Im Microsoft-Erweiterungs Modus lässt der mittellose Compiler auch implizite Deklarationen in Form von Variablen Definitionen zu.

Das folgende Beispiel zeigt eine IDL-Datei, die die Definition einer Schnittstelle enthält. Der Text der Schnittstellen Definition, der zwischen den geschweiften Klammern liegt, enthält die Definition einer Konstante (**bubosize**), einen Typ (**pContext- \_ \_ Handlertyp**) und einige Remote Prozeduren (**remoteopen**, **RemoteRead**, **remoteclose** und **Shutdown**).

``` syntax
[ 
  uuid (ba209999-0c6c-11d2-97cf-00c04f8eea45), 
  version(1.0), 
  pointer_default(unique) 
] 
interface cxhndl 
{ 
 
  const short BUFSIZE = 1024;  
 
  typedef [context_handle] void *PCONTEXT_HANDLE_TYPE; 
 
  short RemoteOpen( 
      [out] PCONTEXT_HANDLE_TYPE *pphContext, 
      [in, string] unsigned char *pszFile 
  ); 
 
   short RemoteRead( 
      [in]  PCONTEXT_HANDLE_TYPE phContext, 
      [out] unsigned char achBuf[BUFSIZE], 
      [out] short *pcbBuf 
  ); 
 
  short RemoteClose( [in, out] PCONTEXT_HANDLE_TYPE *pphContext ); 
 
  void Shutdown(void); 
 
}
```

Weitere Informationen finden Sie in der [Referenz zur Mittel l-Sprache](/windows/desktop/Midl/midl-language-reference).

 

 