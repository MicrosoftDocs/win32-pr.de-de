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
# <a name="handling-unknown-errors"></a><span data-ttu-id="121d0-103">Behandeln von unbekannten Fehlern</span><span class="sxs-lookup"><span data-stu-id="121d0-103">Handling Unknown Errors</span></span>

<span data-ttu-id="121d0-104">Es ist zulässig, einen Statuscode nur von der Implementierung einer Schnittstellen Methode zurückzugeben, die als legal Returnable sanktioniert ist.</span><span class="sxs-lookup"><span data-stu-id="121d0-104">It is legal to return a status code only from the implementation of an interface method sanctioned as legally returnable.</span></span> <span data-ttu-id="121d0-105">Wenn diese Regel nicht beachtet wird, wird die Möglichkeit eines Konflikts zwischen zurückgegebenen Fehlercode Werten und denjenigen, die von der Anwendung sanktioniert werden, angezeigt.</span><span class="sxs-lookup"><span data-stu-id="121d0-105">Failure to observe this rule invites the possibility of conflict between returned error-code values and those sanctioned by the application.</span></span> <span data-ttu-id="121d0-106">Achten Sie besonders auf dieses potenzielle Problem, wenn Sie Fehlercodes aus Funktionen weitergeben, die intern aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="121d0-106">Pay particular attention to this potential problem when propagating error codes from functions that are called internally.</span></span>

<span data-ttu-id="121d0-107">Anwendungen, die-Schnittstellen aufzurufen, sollten jeden unbekannten zurückgegebenen Fehlercode behandeln (im Gegensatz zu einem Erfolgs Code), der nicht \_ unerwartet ist.</span><span class="sxs-lookup"><span data-stu-id="121d0-107">Applications that call interfaces should treat any unknown returned error code (as opposed to a success code) as synonymous with E\_UNEXPECTED.</span></span> <span data-ttu-id="121d0-108">Diese Vorgehensweise zur Behandlung unbekannter Fehlercodes ist für Clients der com-definierten Schnittstellen und Funktionen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="121d0-108">This practice of handling unknown error codes is required by clients of the COM-defined interfaces and functions.</span></span> <span data-ttu-id="121d0-109">Die typische Programmierpraxis besteht darin, einige bestimmte Fehlercodes ausführlich zu behandeln und den Rest generisch zu behandeln. diese Anforderung zur Behandlung unerwarteter oder unbekannter Fehlercodes ist problemlos zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="121d0-109">Because typical programming practice is to handle a few specific error codes in detail and treat the rest generically, this requirement of handling unexpected or unknown error codes is easily met.</span></span>

<span data-ttu-id="121d0-110">Es ist wichtig, alle möglichen Fehler zu behandeln, wenn eine Schnittstellen Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="121d0-110">It is important to handle all possible errors when calling an interface method.</span></span> <span data-ttu-id="121d0-111">Wenn dies nicht der Fall ist, kann es zu einem Absturz ihrer Anwendung oder zu beschädigten Daten kommen, oder es kann anfällig für Sicherheits Exploits werden.</span><span class="sxs-lookup"><span data-stu-id="121d0-111">Failure to do so could cause your application to crash, to corrupt data, or to become vulnerable to security exploits.</span></span> <span data-ttu-id="121d0-112">Das folgende Codebeispiel zeigt die empfohlene Vorgehensweise für die Behandlung unbekannter Fehler:</span><span class="sxs-lookup"><span data-stu-id="121d0-112">The following code sample shows the recommended way of handling unknown errors:</span></span>


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



<span data-ttu-id="121d0-113">Die folgende Fehlerüberprüfung wird häufig bei den Routinen verwendet, die keine besonderen Elemente zurückgeben (außer S \_ OK oder ein unerwarteter Fehler):</span><span class="sxs-lookup"><span data-stu-id="121d0-113">The following error check is often used with those routines that do not return anything special (other than S\_OK or some unexpected error):</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="121d0-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="121d0-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="121d0-115">Fehlerbehandlung in com</span><span class="sxs-lookup"><span data-stu-id="121d0-115">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

 




