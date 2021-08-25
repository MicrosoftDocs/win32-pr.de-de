---
description: In C++ gibt jede Certificate Services-Methode direkt einen HRESULT-Wert zurück, der angibt, ob der Methodenaufruf erfolgreich war oder fehlgeschlagen ist. Wenn der Aufruf fehlgeschlagen ist, gibt der Rückgabewert an, warum er fehlgeschlagen ist.
ms.assetid: 4ab1b5ba-dd19-4802-aa9c-02bd5406681f
title: Fehlerüberprüfung in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3e374c6f0bd933c2e4de7a477fea02b4e1538a7a1fa9b4de78e45fd896b192
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874070"
---
# <a name="error-checking-in-c"></a>Fehlerüberprüfung in C++

In C++ gibt jede Certificate Services-Methode direkt einen **HRESULT-Wert** zurück, der angibt, ob der Methodenaufruf erfolgreich war oder fehlgeschlagen ist. Wenn der Aufruf fehlgeschlagen ist, gibt der Rückgabewert an, warum er fehlgeschlagen ist.

Das folgende Beispiel zeigt, wie die zurückgegebenen **HRESULT-Werte** für die Fehlerüberprüfung verwendet werden können. Beispielfehlercodes finden Sie unter [Allgemeine HRESULT-Werte.](common-hresult-values.md)


```C++
HRESULT hr;
BSTR strAttributeName;
BSTR strAttributeValue = NULL;

if(!(strAttributeName = SysAllocString(L"TheAttribute")))
{
     printf("Could not allocate memory for attribute name.\n");
     exit(1);
}

hr = pICertServerPolicy->GetRequestAttribute(
                                strAttributeName,
                                &strAttributeValue);
if(S_OK != hr)          // Check to determine whether method failed
{
    if (E_INVALIDARG == hr)
    {
        //... Do something to recover from errors and so on.
    }
}
// Free BSTRs when finished.
if (NULL != strAttributeName)
    SysFreeString(strAttributeName);
if (NULL != strAttributeValue)
    SysFreeString(strAttributeValue);
```



 

 



