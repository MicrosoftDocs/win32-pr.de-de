---
description: Im folgenden Beispiel wird die verifyversioninfo-Funktion verwendet, um zu bestimmen, ob die angegebene Produktsuite (s) auf dem lokalen Computer installiert ist.
ms.assetid: 9f405e99-28f5-4415-a274-682b87ae6842
title: Erkennen einer Produkt Suite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 594acbe22283e1c2a3be3ce60116076b2de6f3fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369904"
---
# <a name="detecting-a-product-suite"></a><span data-ttu-id="1e089-103">Erkennen einer Produkt Suite</span><span class="sxs-lookup"><span data-stu-id="1e089-103">Detecting a Product Suite</span></span>

<span data-ttu-id="1e089-104">Im folgenden Beispiel wird die [**verifyversioninfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) -Funktion verwendet, um zu bestimmen, ob die angegebene Produktsuite (s) auf dem lokalen Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="1e089-104">The following example uses the [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) function to determine whether the specified product suite(s) are installed on the local computer.</span></span>

<span data-ttu-id="1e089-105">In diesem Beispiel werden der Ver \_ und das Flag verwendet.</span><span class="sxs-lookup"><span data-stu-id="1e089-105">This example uses the VER\_AND flag.</span></span> <span data-ttu-id="1e089-106">Wenn zwei Flags in der Suite mask angegeben sind, gibt die Funktion nur **dann true** zurück, wenn beide Produkt Sammlungen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="1e089-106">If two flags are specified in the suite mask, the function returns **TRUE** only if both product suites are present.</span></span> <span data-ttu-id="1e089-107">Wenn das Beispiel so geändert wurde, dass das Ver- \_ oder-Flag verwendet wird, gibt [**verifyversioninfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) **true** zurück, wenn eine der Produkt Sammlungen vorhanden wäre.</span><span class="sxs-lookup"><span data-stu-id="1e089-107">If the example were changed to use the VER\_OR flag, [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) would return **TRUE** if either product suite were present.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

BOOL CheckProductSuite ( WORD wSuite ) 
{
  OSVERSIONINFOEX osvi;
  DWORDLONG dwlConditionMask = 0;

  // Initialize the OSVERSIONINFOEX structure.

  ZeroMemory(&osvi, sizeof(OSVERSIONINFOEX));
  osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFOEX);
  osvi.wSuiteMask = wSuite;

  // Set up the condition mask.

  VER_SET_CONDITION( dwlConditionMask, 
          VER_SUITENAME, VER_AND );

  // Perform the test.

  return VerifyVersionInfo(
          &osvi, 
          VER_SUITENAME,
          dwlConditionMask);
}

void main()
{
    if( CheckProductSuite(VER_SUITE_ENTERPRISE) )
        printf( "The system meets the requirements.\n" );
    else printf( "The system does not meet the requirements.\n");
}
```



 

 



