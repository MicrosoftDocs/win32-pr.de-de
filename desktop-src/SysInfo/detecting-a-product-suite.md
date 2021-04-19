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
# <a name="detecting-a-product-suite"></a>Erkennen einer Produkt Suite

Im folgenden Beispiel wird die [**verifyversioninfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) -Funktion verwendet, um zu bestimmen, ob die angegebene Produktsuite (s) auf dem lokalen Computer installiert ist.

In diesem Beispiel werden der Ver \_ und das Flag verwendet. Wenn zwei Flags in der Suite mask angegeben sind, gibt die Funktion nur **dann true** zurück, wenn beide Produkt Sammlungen vorhanden sind. Wenn das Beispiel so geändert wurde, dass das Ver- \_ oder-Flag verwendet wird, gibt [**verifyversioninfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) **true** zurück, wenn eine der Produkt Sammlungen vorhanden wäre.


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



 

 



