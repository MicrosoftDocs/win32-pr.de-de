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
# <a name="return-values-in-c"></a>Rückgabewerte in C++

In C++ ist der Rückgabewert in der Regel vom Typ **HRESULT**. Es stammt von diesem Rückgabewert, dass ermittelt werden kann, ob die Methode erfolgreich war, und falls nicht, was der Fehler war. Zertifikat Dienste werden in \_ der Regel für das **HRESULT** zurückgegeben, wenn die-Methode erfolgreich abgeschlossen wurde. Programmgesteuerte Werte, die zurückgegeben werden müssen, werden durch "out"-Parameter in der-Methode zurückgegeben. Das folgende Beispiel zeigt einen C++-Methoden Aufrufzum Abrufen einer Anforderungs Eigenschaft:


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



Im vorangehenden Code Fragment wird "Erfolg" oder "Fehler" an die **HRESULT** -Variable " *HR*" zurückgegeben. Es ist zwingend erforderlich, die **HRESULT** -Variable zu überprüfen, um \[ im Code erfolgreich durch die Bedingung (en \_ OK! = HR) verarbeitet zu werden \] . Wenn die Methode erfolgreich abgeschlossen wurde, wird der Wert der Anforderungs Eigenschaft im **Variablen** - *varprop* -Parameter zurückgegeben.

 

 



