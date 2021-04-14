---
title: Beispiel Code für die Überprüfung der Rechte zum Erstellen von Schema Objekten
description: Im folgenden C/C++-Codebeispiel wird eine Funktion veranschaulicht, die das Attribut "attribuwedchildclasseseffective" im Schema Container (IADs-Zeiger auf Schema Container wird als Parameter übergeben) für die attributeSchema-Klasse und die classSchema-Klasse überprüft.
ms.assetid: 3abc2351-a3cf-4a6c-9a13-15dd51723883
ms.tgt_platform: multiple
keywords:
- Beispiel Code für die Überprüfung der Rechte zum Erstellen von Schema Objekten AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bef0d4958313a189a0a50c0b4233fdb4a30aaf75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470908"
---
# <a name="example-code-for-checking-for-rights-to-create-schema-objects"></a><span data-ttu-id="8dfb5-104">Beispiel Code für die Überprüfung der Rechte zum Erstellen von Schema Objekten</span><span class="sxs-lookup"><span data-stu-id="8dfb5-104">Example Code for Checking for Rights to Create Schema Objects</span></span>

<span data-ttu-id="8dfb5-105">Im folgenden C/C++-Codebeispiel wird eine Funktion veranschaulicht, die das Attribut " **attribuwedchildclasseseffective** " im Schema Container (IADs-Zeiger auf Schema Container wird als Parameter übergeben) für die **attributeSchema** -Klasse und die **classSchema** -Klasse überprüft.</span><span class="sxs-lookup"><span data-stu-id="8dfb5-105">The following C/C++ code example shows a function that checks the **allowedChildClassesEffective** attribute on the schema container (IADs pointer to schema container is passed as a parameter) for the **attributeSchema** and **classSchema** classes.</span></span> <span data-ttu-id="8dfb5-106">Er gibt **" \_ OK** " zurück, wenn beide Klassen in " **Zuordnungs** Klasse" aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="8dfb5-106">It returns **S\_OK** if both classes are listed in **allowedChildClassesEffective**.</span></span> <span data-ttu-id="8dfb5-107">Wenn beides nicht der Fall ist, wird **S \_ false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8dfb5-107">If both are not, it returns **S\_FALSE**.</span></span>


```C++

// Function takes an IADs pointer to schema container as a parameter.
 
HRESULT HasSchemaAdditionRights(IADs *pSchema)
{
if (!pSchema)
  return E_POINTER;
HRESULT hr = E_FAIL;
VARIANT var;
VARIANT *pVar;
// Check access rights.
BOOL bIsAddAttributeAllowed = FALSE;
BOOL bIsAddClassAllowed = FALSE;
// Get AllowedChildClassesEffective. It is constructed;
// therefore, you must use GetInfoEx to explicitly 
// get it into the cache.
LPOLESTR pwszArray[] = {L"allowedChildClassesEffective"};
DWORD dwArrayItems = sizeof(pwszArray)/sizeof(LPOLESTR);
VARIANT vArray;
VariantInit(&vArray);
// Build a Variant of array type, using the specified string array.
hr = ADsBuildVarArrayStr(pwszArray, dwArrayItems, &vArray);
if (SUCCEEDED(hr))
{
  hr = pSchema->GetInfoEx(vArray,0L);
  if (SUCCEEDED(hr))
  {
    hr = pSchema->GetEx(CComBSTR("allowedChildClassesEffective"), 
                        &var);
    if (SUCCEEDED(hr))
    {
       hr = SafeArrayAccessData((SAFEARRAY*)(var.pparray), 
                                (void HUGEP* FAR*)&pVar);
       long lLBound, lUBound;
       // One-dimensional array. Get the bounds for the array.
       hr = SafeArrayGetLBound((SAFEARRAY*)(var.pparray), 
                               1,
                               &lLBound);
       hr = SafeArrayGetUBound((SAFEARRAY*)(var.pparray), 
                               1, 
                               &lUBound);
       // Get the count of elements
       long cElements = lUBound-lLBound + 1;
       // Get the elements of the array.
       if (SUCCEEDED(hr))
       {
        for (int i = 0; i < cElements; i++ ) 
        {
          // Check each element to verify that attributeSchema 
          // or classSchema is there.
          if (VT_BSTR == pVar[i].vt)
          {
            if (0==_wcsicmp(L"attributeSchema", pVar[i].bstrVal))
              bIsAddAttributeAllowed = TRUE;
            else if (0==_wcsicmp(L"classSchema", pVar[i].bstrVal))
              bIsAddClassAllowed = TRUE;
          }
        }
        if (bIsAddAttributeAllowed && bIsAddClassAllowed)
          hr = S_OK;
        else
          hr = S_FALSE;
       }
    }
    VariantClear(&var);
  }
}
 
return hr;
 
};
```



 

 




