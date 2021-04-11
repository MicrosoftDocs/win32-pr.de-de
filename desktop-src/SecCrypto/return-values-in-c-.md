---
description: In C++ ist der Rückgabewert in der Regel vom Typ HRESULT.
ms.assetid: 7abf1b3e-b94b-4846-a813-5eab5b34324c
title: Rückgabewerte in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7a5417019468945054f24701636fcece1d3d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215995"
---
# <a name="return-values-in-c"></a><span data-ttu-id="07ab2-103">Rückgabewerte in C++</span><span class="sxs-lookup"><span data-stu-id="07ab2-103">Return Values in C++</span></span>

<span data-ttu-id="07ab2-104">In C++ ist der Rückgabewert in der Regel vom Typ **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="07ab2-104">In C++, the return value is typically of type **HRESULT**.</span></span> <span data-ttu-id="07ab2-105">Es stammt von diesem Rückgabewert, dass ermittelt werden kann, ob die Methode erfolgreich war, und falls nicht, was der Fehler war.</span><span class="sxs-lookup"><span data-stu-id="07ab2-105">It is from this return value that it can be determined whether the method succeeded or not, and if not, what the error was.</span></span> <span data-ttu-id="07ab2-106">Zertifikat Dienste werden in \_ der Regel für das **HRESULT** zurückgegeben, wenn die-Methode erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="07ab2-106">Certificate Services typically returns S\_OK for the **HRESULT** when the method has completed successfully.</span></span> <span data-ttu-id="07ab2-107">Programmgesteuerte Werte, die zurückgegeben werden müssen, werden durch "out"-Parameter in der-Methode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="07ab2-107">Programmatic values that need to be returned are returned through "out" parameters in the method.</span></span> <span data-ttu-id="07ab2-108">Das folgende Beispiel zeigt einen C++-Methoden Aufrufzum Abrufen einer Anforderungs Eigenschaft:</span><span class="sxs-lookup"><span data-stu-id="07ab2-108">The following example shows a C++ method call to retrieve a request property:</span></span>


```C++
BSTR      bstrPropName = NULL;
VARIANT   varProp;
HRESULT   hr;

VariantInit(&varProp);

bstrPropName = SysAllocString(L"RequestID");
if (NULL == bstrPropName)
{
    printf("Failed SysAllocString\n");
    // Take application-specific error action.
    exit(1);
}

// Retrieve the request property.
// pCertServerPolicy is a pointer to a previously
// instantiated ICertServerPolicy object.
hr = pCertServerPolicy->GetRequestProperty(bstrPropName,
                                           PROPTYPE_LONG,
                                           &varProp);
if (S_OK != hr)
{
    printf("Failed GetRequestProperty [%x]\n", hr);
    // Take application-specific error action.
    // ...
}
else
{
    // Successfully retrieved property; use varProp as needed.
    // ...
}

// Done processing.
VariantClear(&varProp);
if (NULL != bstrPropName)
    SysFreeString(bstrPropName);
```



<span data-ttu-id="07ab2-109">Im vorangehenden Code Fragment wird "Erfolg" oder "Fehler" an die **HRESULT** -Variable " *HR*" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="07ab2-109">In the preceding code fragment, success or failure is returned to the **HRESULT** variable, *hr*.</span></span> <span data-ttu-id="07ab2-110">Es ist zwingend erforderlich, die **HRESULT** -Variable zu überprüfen, um \[ im Code erfolgreich durch die Bedingung (en \_ OK! = HR) verarbeitet zu werden \] .</span><span class="sxs-lookup"><span data-stu-id="07ab2-110">It is imperative to check the **HRESULT** variable for success \[handled in the code by the condition (S\_OK != hr)\].</span></span> <span data-ttu-id="07ab2-111">Wenn die Methode erfolgreich abgeschlossen wurde, wird der Wert der Anforderungs Eigenschaft im **Variablen** - *varprop* -Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="07ab2-111">If the method completed successfully, the request property value is returned in the **VARIANT** *varProp* parameter.</span></span>

 

 



