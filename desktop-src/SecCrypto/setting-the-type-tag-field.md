---
description: Variant-Typvariablen verfügen über ein Type-Tagfeld VT, das den Datentyp der Daten angibt.
ms.assetid: 3436faf6-2e66-46a1-b1e8-84f513282c16
title: Festlegen des Typs "Tagfeld"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e443fae33b14bd4270e63188ff96a042a91c8e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214371"
---
# <a name="setting-the-type-tag-field"></a>Festlegen des Typs "Tagfeld"

**Variant** -Typvariablen verfügen über ein Type-Tagfeld **VT** , das den Datentyp der Daten angibt. Rückgabewerte von **Variant** -Typen werden von Methoden zurückgegeben, bei denen das Type-Tagfeld auf den Datentyp des Rückgabewerts festgelegt ist. Für die Eingabeparameter des **Variant** -Typs in einem Methodenaufrufe muss das Type-Tagfeld von der Anwendung auf einen der unterstützten Werte festgelegt sein. Die Entsprechung von Parametertypen zu Datentypen lautet wie folgt.



| Parametertyp              | Datentyp                                      |
|-----------------------------|------------------------------------------------|
| propType \_ Long<br/>   | VT \_ I2 oder VT \_ I4<br/>                    |
| propType- \_ Datum<br/>   | VT- \_ Datum<br/>                            |
| propType- \_ Binärdatei<br/> | VT \_ BSTR oder (VT \_ BSTR \| VT \_ ByRef)<br/> |
| propType- \_ Zeichenfolge<br/> | VT \_ BSTR oder (VT \_ BSTR \| VT \_ ByRef)<br/> |



 

Im folgenden Beispiel wird gezeigt, wie die oben aufgeführten Variant-Datentypen initialisiert werden.


```C++
HRESULT hr;
VARIANT vEMail;
VARIANT vNotBefore;
VARIANT vCount;
VARIANT vByRef;
BSTR bstr = NULL;
SYSTEMTIME st;

//Set the BSTR variant data type.
VariantInit(&vEMail);
vEMail.vt = VT_BSTR;   
vEMail.bstrVal = SysAllocString(L"someone@example.com");
if (NULL == vEMail.bstrVal)
{
    hr = E_OUTOFMEMORY;
    //Handle error.   
}
//Use the variant.
VariantClear(&vEMail);  //when done


//Set the BSTR|BYREF variant data type.
VariantInit(&vByRef);
vByRef.vt = VT_BSTR | VT_BYREF;   
vByRef.pbstrVal = &bstr;
//Use the variant.
VariantClear(&vByRef);  //when done
SysFreeString(bstr);


//Set the DATE variant data type.
memset(&st, 0, sizeof(SYSTEMTIME));
st.wYear = 2000;
st.wMonth = 1;
st.wDay = 1;
st.wHour = 12;

VariantInit(&vNotBefore);
vNotBefore.vt = VT_DATE;
if (!SystemTimeToVariantTime(&st, &vNotBefore.date))
{
    hr = E_FAIL;
    //Handle error.
}
//Use the variant.
VariantClear(&vNotBefore);  //when done


//Set the LONG variant data type.
VariantInit(&vCount);
vCount.vt = VT_I4;
vCount.long = 123456;
//Use the variant.
VariantClear(&vCount);  //when done
```



 

 




