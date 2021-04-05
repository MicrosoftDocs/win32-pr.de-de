---
title: Abrufen des Attributs "objectClass"
description: Das objectClass-Attribut enthält die Klasse, für die das Objekt eine Instanz ist, sowie alle Klassen, von denen diese Klasse abgeleitet ist.
ms.assetid: 6066d9c3-f97b-482a-88c7-0fde1dc2f4c4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f237efff1e13c7f3498a51f38588c9885fbab76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707565"
---
# <a name="retrieving-the-objectclass-attribute"></a>Abrufen des Attributs "objectClass"

Das **objectClass** -Attribut enthält die Klasse, für die das Objekt eine Instanz ist, sowie alle Klassen, von denen diese Klasse abgeleitet ist. Die **User** -Klasse erbt z. b. von **Top**, **Person** und **OrganizationalPerson**. Daher enthält das **objectClass** -Attribut die Namen dieser Klassen sowie den Benutzer. Wie können Sie also herausfinden, in welcher Klasse das Objekt eine Instanz von ist? Das **objectClass** -Attribut ist das einzige Attribut mit mehreren Werten, das übergeordnete Werte verfügt. Der erste Wert ist der obere Teil der Klassenhierarchie, bei der es sich um die oberste Klasse handelt, und der letzte Wert ist die am meisten abgeleitete Klasse, bei der es sich um die Klasse handelt, von der das Objekt eine Instanz ist.

Die folgende Funktion verwendet einen Zeiger auf eine Spalte, die ein **objectClass** -Attribut enthält, und gibt die instanziierte **objectClass** des-Objekts zurück.


```C++
HRESULT GetClass(ADS_SEARCH_COLUMN *pcol, LPOLESTR *ppClass)
{
  if (!pcol)
    return E_POINTER;
 
  HRESULT hr = E_FAIL;
  if (ppClass)
  {
    LPOLESTR szClass = new OLECHAR[MAX_PATH];
    wcscpy_s(szClass, L"");
    if ( _wcsicmp(pcol->pszAttrName,L"objectClass") == 0 )
    {
      for (DWORD x = 0; x< pcol->dwNumValues; x++)
      {
        wcscpy_s(szClass, pcol->pADsValues[x].CaseIgnoreString);
      }
    }
    if (0==wcscmp(L"", szClass))
    {
      hr = E_FAIL;
    }
    else
    {
      //Allocate memory for string.
      //Caller must free using CoTaskMemFree.
      *ppClass = (OLECHAR *)CoTaskMemAlloc (
                             sizeof(OLECHAR)*(wcslen(szClass)+1));
      if (*ppClass)
      {
        wcscpy_s(*ppClass, szClass);
        hr = S_OK;
      }
      else
      hr=E_FAIL;
    }
  }
  return hr;
}
```



 

 




