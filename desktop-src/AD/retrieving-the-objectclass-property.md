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
# <a name="retrieving-the-objectclass-attribute"></a><span data-ttu-id="8e092-103">Abrufen des Attributs "objectClass"</span><span class="sxs-lookup"><span data-stu-id="8e092-103">Retrieving the objectClass Attribute</span></span>

<span data-ttu-id="8e092-104">Das **objectClass** -Attribut enthält die Klasse, für die das Objekt eine Instanz ist, sowie alle Klassen, von denen diese Klasse abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="8e092-104">The **objectClass** attribute contains the class of which the object is an instance, as well as all classes from which that class is derived.</span></span> <span data-ttu-id="8e092-105">Die **User** -Klasse erbt z. b. von **Top**, **Person** und **OrganizationalPerson**. Daher enthält das **objectClass** -Attribut die Namen dieser Klassen sowie den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="8e092-105">For example, the **user** class inherits from **top**, **person**, and **organizationalPerson**; therefore, the **objectClass** attribute contains the names of those classes, as well as user.</span></span> <span data-ttu-id="8e092-106">Wie können Sie also herausfinden, in welcher Klasse das Objekt eine Instanz von ist?</span><span class="sxs-lookup"><span data-stu-id="8e092-106">So, how do you find out what class the object is an instance of?</span></span> <span data-ttu-id="8e092-107">Das **objectClass** -Attribut ist das einzige Attribut mit mehreren Werten, das übergeordnete Werte verfügt.</span><span class="sxs-lookup"><span data-stu-id="8e092-107">The **objectClass** attribute is the only attribute with multiple values that has ordered values.</span></span> <span data-ttu-id="8e092-108">Der erste Wert ist der obere Teil der Klassenhierarchie, bei der es sich um die oberste Klasse handelt, und der letzte Wert ist die am meisten abgeleitete Klasse, bei der es sich um die Klasse handelt, von der das Objekt eine Instanz ist.</span><span class="sxs-lookup"><span data-stu-id="8e092-108">The first value is the top of the class hierarchy, which is the top class, and the last value is the most derived class, which is the class that the object is an instance of.</span></span>

<span data-ttu-id="8e092-109">Die folgende Funktion verwendet einen Zeiger auf eine Spalte, die ein **objectClass** -Attribut enthält, und gibt die instanziierte **objectClass** des-Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="8e092-109">The following function takes a pointer to a column containing an **objectClass** attribute and returns the instantiated **objectClass** of the object.</span></span>


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



 

 




