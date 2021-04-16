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
# <a name="error-checking-in-c"></a><span data-ttu-id="002d5-104">Fehlerüberprüfung in C++</span><span class="sxs-lookup"><span data-stu-id="002d5-104">Error Checking in C++</span></span>

<span data-ttu-id="002d5-105">In C++ gibt jede Zertifikat Dienst Methode direkt einen **HRESULT** -Wert zurück, der angibt, ob der Methodenaufrufe erfolgreich war oder fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="002d5-105">In C++, every Certificate Services method directly returns an **HRESULT** value that indicates whether the method call succeeded or failed.</span></span> <span data-ttu-id="002d5-106">Wenn der-Befehl fehlgeschlagen ist, gibt der Rückgabewert den Grund für den Fehler an.</span><span class="sxs-lookup"><span data-stu-id="002d5-106">If the call failed, the return value indicates why it failed.</span></span>

<span data-ttu-id="002d5-107">Im folgenden Beispiel wird gezeigt, wie die zurückgegebenen **HRESULT** -Werte für die Fehlerüberprüfung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="002d5-107">The following example shows how the returned **HRESULT** values can be used for error checking.</span></span> <span data-ttu-id="002d5-108">Beispielsweise Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="002d5-108">For example error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>


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



 

 



