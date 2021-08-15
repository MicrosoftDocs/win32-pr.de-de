---
title: IADsSyntax-Eigenschaftsmethoden (Iads.h)
description: Die Eigenschaftenmethoden der IADsSyntax-Schnittstelle erhalten oder legen die in der folgenden Tabelle aufgeführten Eigenschaften fest. Weitere Informationen zu Eigenschaftsmethoden finden Sie unter Schnittstelleneigenschaftenmethoden.
ms.assetid: a216a55d-63eb-4fdf-a67f-8d4b5eb74262
ms.tgt_platform: multiple
keywords:
- IADsSyntax-Eigenschaftsmethoden ADSI
topic_type:
- apiref
api_name:
- IADsSyntax Property Methods
- IADsSyntax.OleAutoDataType
- IADsSyntax.get_OleAutoDataType
- IADsSyntax.put_OleAutoDataType
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c193bba78bfe215d37bdfdedf5d45bd73f1a85606b3dab6e5a3c233cece8db18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961899"
---
# <a name="iadssyntax-property-methods"></a>IADsSyntax-Eigenschaftsmethoden

Die Eigenschaftenmethoden der [**IADsSyntax-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadssyntax) erhalten oder legen die in der folgenden Tabelle aufgeführten Eigenschaften fest. Weitere Informationen zu Eigenschaftsmethoden finden Sie unter [Schnittstelleneigenschaftsmethoden.](interface-property-methods.md)

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**OleAutoDataType**
</dt> <dd> <dl>

Ruft einen **LONG-Wert** ab, der den Wert der **VT \_ xxx-Konstante** für den Automation-Datentyp enthält, der diese Syntax darstellt, und legt diesen fest.

Active Directory unterstützt die folgenden **VT \_ xxx-Konstanten** für den Automation-Datentyp, der diese Syntax darstellt:

-   **VT \_ BOOL** BOOL
-   **VT \_ BSTR** BSTR
-   **VT \_ BSTRT** BSTRT
-   **VT \_ CY** CURRENCY
-   **VT \_ DATE** Date
-   **VT \_ EMPTY** **NULL**
-   **VT \_ ERROR** Ungültig
-   **VT \_ I2** short
-   **VT \_ I4** long
-   **VT \_ R4** real
-   **VT \_ R8** double
-   **VT \_ UI1** BYTE

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OleAutoDataType(
  [out] LONG* plAutoDataType
);
HRESULT put_OleAutoDataType(
  [in] LONG lAutoDataType
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Hinweise

Ein Array von nicht signierten Bytes, **VT \_ UI1** \| **VT \_ ARRAY,** kann bedeuten, dass der Anbieter eine Syntax zugeordnet hat, die keinem virtuellen Automation-Typ zugeordnet werden kann.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird die Syntax des **OperatingSystemVersion-Attributs** eines Computers in einem Netzwerk über den WinNT-Anbieter untersucht. Die Ergebnissyntax ist eine Zeichenfolge.


```VB
Dim obj As IADs
Dim cl As IADsClass
Dim pr As IADsProperty
Dim sy As IADsSyntax
Dim sc As IADsContainer
On Error GoTo Cleanup

Set obj = GetObject("WinNT://myMachine,computer")
Set cl = GetObject(obj.Schema)
Set sc = GetObject(cl.Parent)
Set pr = sc.GetObject("Property","OperatingSystemVersion")
Set sy = GetObject(sc.ADsPath & "/" & pr.Syntax)
 
MsgBox "Automation data types: " & sy.OleAutoDataType

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set obj = Nothing
    Set cl = Nothing
    Set pr = Nothing
    Set sy = Nothing
    Set sc = Nothing
```



Im folgenden Codebeispiel wird die Syntax des **OperatingSystemVersion-Attributs** eines Computers in einem Netzwerk über den WinNT-Anbieter untersucht. Die Ergebnissyntax ist eine Zeichenfolge. Aus Gründen der Kürze wird die Fehlerüberprüfung ausgelassen.


```C++
#include <stdio.h>
#include <activeds.h>
#include <atlbase.h>
 
IADs *pObj = NULL;
IADsClass *pCls = NULL;
IADsProperty *pProp = NULL;
IADsSyntax *pSyn = NULL;
IADsContainer *pCont = NULL;
 
HRESULT hr = ADsGetObject(L"WinNT://myMachine,computer",
                          IID_IADs,
                          (void**)&pObj);
if(FAILED(hr)){goto Cleanup;}
VARIANT var;
VariantInit(&var);
CComBSTR sbstr;
 
pObj->get_Schema(&sbstr);
printf("Object schema: %S\n",sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsClass,(void**)&pCls);
if(FAILED(hr)){goto Cleanup;}

pCls->get_Parent(&sbstr);
printf("Object class's container:  %S\n", sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsContainer, (void**)&pCont);
if(FAILED(hr)){goto Cleanup;}
pCont->QueryInterface(IID_IADs,(void**)&pObj);
pObj->get_ADsPath(&sbstr);
printf("Container's AdsPath:  %S\n",sbstr);
 
IDispatch *pDisp;
hr = pCont->GetObject(CComBSTR("Property"),
                      CComBSTR("OperatingSystemVersion"),
                      (IDispatch**)&pDisp);
if(FAILED(hr)){goto Cleanup;}
 
hr = pDisp->QueryInterface(IID_IADsProperty, (void**)&pProp);
if(FAILED(hr)){goto Cleanup;}
 
hr = pProp->get_Syntax(&sbstr);
if(FAILED(hr)){goto Cleanup;}
printf("Property Syntax:  %S\n",sbstr);
 
printf("ADsPath of the syntax object %S\n",sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsSyntax, (void**)&pSyn);
if(FAILED(hr)){goto Cleanup;}

long lType;
pSyn->get_OleAutoDataType(&lType);
printf("Property syntax's OleAutoDataType: %d\n", lType);

Cleanup:
    if(pObj)
        pObj->Release();

    if(pProp)
        pProp->Release();

    if(pCls)
        pCls->Release();

    if(pSyn)
        pSyn->Release();

    if(pCont)
        pCont->Release();
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | \_IID-IADsSyntax ist als C8F93DD2-4AE0-11CF-9E73-00AA004A5691 definiert.<br/>           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)
</dt> <dt>

[**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax)
</dt> </dl>

 

 





