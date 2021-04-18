---
title: Iadssyntax-Eigenschaften Methoden (IADs. h)
description: Mit den Eigenschafts Methoden der iadssyntax-Schnittstelle werden die in der folgenden Tabelle aufgeführten Eigenschaften festgelegt oder festgelegt. Weitere Informationen zu Eigenschafts Methoden finden Sie unter Interface Property Methods.
ms.assetid: a216a55d-63eb-4fdf-a67f-8d4b5eb74262
ms.tgt_platform: multiple
keywords:
- Iadssyntax-Eigenschaften Methoden ADSI
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
ms.openlocfilehash: a7a41c84efb4f48171913156823e18a301236290
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517657"
---
# <a name="iadssyntax-property-methods"></a>Iadssyntax-Eigenschaften Methoden

Mit den Eigenschafts Methoden der [**iadssyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) -Schnittstelle werden die in der folgenden Tabelle aufgeführten Eigenschaften festgelegt oder festgelegt. Weitere Informationen zu Eigenschafts Methoden finden Sie unter [Interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**Oleautodatatype**
</dt> <dd> <dl>

Ruft eine **Länge** ab und legt Sie fest, die den Wert der **VT \_ xxx** -Konstante für den Automatisierungs Datentyp enthält, der diese Syntax darstellt.

Active Directory unterstützt die folgenden **VT \_ xxx** -Konstanten für den Automatisierungs Datentyp, der diese Syntax darstellt:

-   **VT \_ Boolescher** bool
-   **VT \_ BSTR** BSTR
-   **VT \_ bstraut** (bstraut)
-   **VT \_ CY** -Währung
-   **VT \_ Datums** Datum
-   **VT \_ leere** **null**
-   **VT \_ Fehler** ist ungültig.
-   **VT \_ I2** Short
-   **VT \_ I4** Long
-   **VT \_ R4** Real
-   **VT \_ R8** Double
-   **VT \_ UI1** Byte

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
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

 

## <a name="remarks"></a>Bemerkungen

Ein Array von Bytes ohne Vorzeichen, **VT \_ UI1** \| **VT \_ Array** , könnte bedeuten, dass der Anbieter eine Syntax zugeordnet hat, die keinem virtuellen Automatisierungs Typ zugeordnet werden kann.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird die Syntax des **operatingsystemversion** -Attributs eines Computers in einem Netzwerk über den WinNT-Anbieter untersucht. Die Ergebnis Syntax ist eine Zeichenfolge.


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



Im folgenden Codebeispiel wird die Syntax des **operatingsystemversion** -Attributs eines Computers in einem Netzwerk über den WinNT-Anbieter untersucht. Die Ergebnis Syntax ist eine Zeichenfolge. Aus Gründen der Übersichtlichkeit wird die Fehlerüberprüfung ausgelassen.


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
| Header<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ iadssyntax ist als C8F93DD2-4AE0-11CF-9E73-00AA004A5691 definiert.<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[**Iadsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)
</dt> <dt>

[**Iadssyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax)
</dt> </dl>

 

 





