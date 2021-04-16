---
description: In C++ gibt jede Zertifikat Dienst Methode direkt einen HRESULT-Wert zurück, der angibt, ob der Methodenaufrufe erfolgreich war oder fehlgeschlagen ist. Wenn der-Befehl fehlgeschlagen ist, gibt der Rückgabewert den Grund für den Fehler an.
ms.assetid: 4ab1b5ba-dd19-4802-aa9c-02bd5406681f
title: Fehlerüberprüfung in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f2a56acd41269ece0f9a5c7de4a2dff1960bb10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528718"
---
# <a name="error-checking-in-c"></a>Fehlerüberprüfung in C++

In C++ gibt jede Zertifikat Dienst Methode direkt einen **HRESULT** -Wert zurück, der angibt, ob der Methodenaufrufe erfolgreich war oder fehlgeschlagen ist. Wenn der-Befehl fehlgeschlagen ist, gibt der Rückgabewert den Grund für den Fehler an.

Im folgenden Beispiel wird gezeigt, wie die zurückgegebenen **HRESULT** -Werte für die Fehlerüberprüfung verwendet werden können. Beispielsweise Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).


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



 

 



