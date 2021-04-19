---
description: Einige der LSA-Richtlinien Funktionen verwenden die LSA- \_ Unicode- \_ Zeichen folgen Struktur zum Speichern von Zeichen folgen Informationen. In dieser Struktur werden die Zeichenfolge und ihre Längen Informationen gespeichert.
ms.assetid: 8a02cbb4-0b59-4c1e-9831-592a2005905e
title: Verwenden von LSA Unicode-Zeichen folgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc00e5b98bf2e287f32934b4ea093570ba3359ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353037"
---
# <a name="using-lsa-unicode-strings"></a><span data-ttu-id="9f8ed-104">Verwenden von LSA Unicode-Zeichen folgen</span><span class="sxs-lookup"><span data-stu-id="9f8ed-104">Using LSA Unicode Strings</span></span>

<span data-ttu-id="9f8ed-105">Einige der LSA-Richtlinien Funktionen verwenden die [**LSA- \_ Unicode- \_ Zeichen**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) folgen Struktur zum Speichern von Zeichen folgen Informationen.</span><span class="sxs-lookup"><span data-stu-id="9f8ed-105">Several of the LSA Policy functions use the [**LSA\_UNICODE\_STRING**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) structure to store string information.</span></span> <span data-ttu-id="9f8ed-106">In dieser Struktur werden die Zeichenfolge und ihre Längen Informationen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9f8ed-106">This structure stores the string and its length information.</span></span>

<span data-ttu-id="9f8ed-107">Der folgende Code implementiert eine Funktion, die **LPWSTR** -Daten in [**LSA- \_ Unicode- \_ Zeichen**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) folgen Strukturen konvertiert:</span><span class="sxs-lookup"><span data-stu-id="9f8ed-107">The following code implements a function that converts **LPWSTR** data to [**LSA\_UNICODE\_STRING**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) structures:</span></span>


```C++
#include <windows.h>

bool InitLsaString(
  PLSA_UNICODE_STRING pLsaString,
  LPCWSTR pwszString
)
{
  DWORD dwLen = 0;

  if (NULL == pLsaString)
      return FALSE;

  if (NULL != pwszString) 
  {
      dwLen = wcslen(pwszString);
      if (dwLen > 0x7ffe)   // String is too large
          return FALSE;
  }

  // Store the string.
  pLsaString->Buffer = (WCHAR *)pwszString;
  pLsaString->Length =  (USHORT)dwLen * sizeof(WCHAR);
  pLsaString->MaximumLength= (USHORT)(dwLen+1) * sizeof(WCHAR);

  return TRUE;
}
```



 

 



