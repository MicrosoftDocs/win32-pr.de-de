---
title: Behandeln von unbekannten Fehlern
description: Behandeln von unbekannten Fehlern
ms.assetid: d6a4cc60-8320-4b67-9f2e-7c4bea6c37fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8c3d9e70b89a9a78be62d2940ad8a69ac34c8f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037525"
---
# <a name="handling-unknown-errors"></a>Behandeln von unbekannten Fehlern

Es ist zulässig, einen Statuscode nur von der Implementierung einer Schnittstellen Methode zurückzugeben, die als legal Returnable sanktioniert ist. Wenn diese Regel nicht beachtet wird, wird die Möglichkeit eines Konflikts zwischen zurückgegebenen Fehlercode Werten und denjenigen, die von der Anwendung sanktioniert werden, angezeigt. Achten Sie besonders auf dieses potenzielle Problem, wenn Sie Fehlercodes aus Funktionen weitergeben, die intern aufgerufen werden.

Anwendungen, die-Schnittstellen aufzurufen, sollten jeden unbekannten zurückgegebenen Fehlercode behandeln (im Gegensatz zu einem Erfolgs Code), der nicht \_ unerwartet ist. Diese Vorgehensweise zur Behandlung unbekannter Fehlercodes ist für Clients der com-definierten Schnittstellen und Funktionen erforderlich. Die typische Programmierpraxis besteht darin, einige bestimmte Fehlercodes ausführlich zu behandeln und den Rest generisch zu behandeln. diese Anforderung zur Behandlung unerwarteter oder unbekannter Fehlercodes ist problemlos zu erfüllen.

Es ist wichtig, alle möglichen Fehler zu behandeln, wenn eine Schnittstellen Methode aufgerufen wird. Wenn dies nicht der Fall ist, kann es zu einem Absturz ihrer Anwendung oder zu beschädigten Daten kommen, oder es kann anfällig für Sicherheits Exploits werden. Das folgende Codebeispiel zeigt die empfohlene Vorgehensweise für die Behandlung unbekannter Fehler:


```C++
HRESULT hr; 
hr = xxMethod(); 
 
switch (GetScode(hr))  
{ 
    case NOERROR: 
      // Method returned success. 
      break; 
 
    case x1: 
      // Handle error x1 here.
      break; 
 
    case x2: 
      // Handle error x2 here.
      break; 
 
    case E_UNEXPECTED: 
    default: 
      // Handle unexpected errors here. 
      break; 
} 
 
```



Die folgende Fehlerüberprüfung wird häufig bei den Routinen verwendet, die keine besonderen Elemente zurückgeben (außer S \_ OK oder ein unerwarteter Fehler):


```C++
if (xxMethod() == NOERROR) 
{
    // Handle success here.
} 
else 
{
    // Handle failure here.
} 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Fehlerbehandlung in com](error-handling-in-com.md)
</dt> </dl>

 

 




