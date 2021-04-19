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
# <a name="using-lsa-unicode-strings"></a>Verwenden von LSA Unicode-Zeichen folgen

Einige der LSA-Richtlinien Funktionen verwenden die [**LSA- \_ Unicode- \_ Zeichen**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) folgen Struktur zum Speichern von Zeichen folgen Informationen. In dieser Struktur werden die Zeichenfolge und ihre Längen Informationen gespeichert.

Der folgende Code implementiert eine Funktion, die **LPWSTR** -Daten in [**LSA- \_ Unicode- \_ Zeichen**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) folgen Strukturen konvertiert:


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



 

 



