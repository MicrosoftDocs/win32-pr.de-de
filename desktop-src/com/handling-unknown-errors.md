---
title: Behandeln unbekannter Fehler
description: Behandeln unbekannter Fehler
ms.assetid: d6a4cc60-8320-4b67-9f2e-7c4bea6c37fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38fb0e8aaaef8fc3ff4ae9bb76f76a845c325c4b5a5dc4d409dbd0ab35734ce4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048258"
---
# <a name="handling-unknown-errors"></a>Behandeln unbekannter Fehler

Es ist zulässig, einen Statuscode nur aus der Implementierung einer Schnittstellenmethode zurückzugeben, die als rechtlich zulässig sanktioniert ist. Wenn diese Regel nicht beachtet wird, besteht die Möglichkeit eines Konflikts zwischen zurückgegebenen Fehlercodewerten und den von der Anwendung sanktionierten Werten. Achten Sie besonders auf dieses potenzielle Problem, wenn Sie Fehlercodes von Funktionen, die intern aufgerufen werden, weiterverbreiten.

Anwendungen, die Schnittstellen aufrufen, sollten jeden unbekannten zurückgegebenen Fehlercode (im Gegensatz zu einem Erfolgscode) als Synonym für E \_ UNEXPECTED behandeln. Diese Vorgehensweise zur Behandlung unbekannter Fehlercodes ist für Clients der COM-definierten Schnittstellen und Funktionen erforderlich. Da es üblich ist, einige bestimmte Fehlercodes im Detail zu behandeln und den Rest generisch zu behandeln, ist diese Anforderung der Behandlung unerwarteter oder unbekannter Fehlercodes leicht zu erfüllen.

Es ist wichtig, beim Aufrufen einer Schnittstellenmethode alle möglichen Fehler zu behandeln. Andernfalls kann ihre Anwendung abstürzt, Daten beschädigen oder anfällig für Sicherheits exploits werden. Das folgende Codebeispiel zeigt die empfohlene Methode zur Behandlung unbekannter Fehler:


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



Die folgende Fehlerüberprüfung wird häufig mit Routinen verwendet, die keine besonderen Fehler zurückgeben (außer S \_ OK oder unerwartete Fehler):


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

[Fehlerbehandlung in COM](error-handling-in-com.md)
</dt> </dl>

 

 




