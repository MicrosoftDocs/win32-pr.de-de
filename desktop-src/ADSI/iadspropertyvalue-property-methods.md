---
title: IADsPropertyValue-Eigenschaftsmethoden (Iads.h)
description: Die Eigenschaftenmethoden der IADsPropertyValue-Schnittstelle bieten Zugriff auf die in der folgenden Tabelle beschriebenen Eigenschaften. Weitere Informationen finden Sie unter Schnittstelleneigenschaftsmethoden.
ms.assetid: 1039d4a9-bef8-457d-9a32-3743c14adef1
ms.tgt_platform: multiple
keywords:
- IADsPropertyValue-Eigenschaftsmethoden ADSI
topic_type:
- apiref
api_name:
- IADsPropertyValue Property Methods
- IADsPropertyValue.ADsType
- IADsPropertyValue.get_ADsType
- IADsPropertyValue.put_ADsType
- IADsPropertyValue.DNString
- IADsPropertyValue.get_DNString
- IADsPropertyValue.put_DNString
- IADsPropertyValue.CaseExactString
- IADsPropertyValue.get_CaseExactString
- IADsPropertyValue.put_CaseExactString
- IADsPropertyValue.CaseIgnoreString
- IADsPropertyValue.get_CaseIgnoreString
- IADsPropertyValue.put_CaseIgnoreString
- IADsPropertyValue.PrintableString
- IADsPropertyValue.get_PrintableString
- IADsPropertyValue.put_PrintableString
- IADsPropertyValue.NumericString
- IADsPropertyValue.get_NumericString
- IADsPropertyValue.put_NumericString
- IADsPropertyValue.Boolean
- IADsPropertyValue.get_Boolean
- IADsPropertyValue.put_Boolean
- IADsPropertyValue.Integer
- IADsPropertyValue.get_Integer
- IADsPropertyValue.put_Integer
- IADsPropertyValue.OctetString
- IADsPropertyValue.get_OctetString
- IADsPropertyValue.put_OctetString
- IADsPropertyValue.SecurityDescriptor
- IADsPropertyValue.get_SecurityDescriptor
- IADsPropertyValue.put_SecurityDescriptor
- IADsPropertyValue.LargeInteger
- IADsPropertyValue.get_LargeInteger
- IADsPropertyValue.put_LargeInteger
- IADsPropertyValue.UTCTime
- IADsPropertyValue.get_UTCTime
- IADsPropertyValue.put_UTCTime
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaa64ef7d7802306902060a9eb0e2423f3155ba032115c831212403cda658784
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118427616"
---
# <a name="iadspropertyvalue-property-methods"></a>IADsPropertyValue-Eigenschaftsmethoden

Die Eigenschaftenmethoden der [**IADsPropertyValue-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) bieten Zugriff auf die in der folgenden Tabelle beschriebenen Eigenschaften. Weitere Informationen finden Sie unter [Schnittstelleneigenschaftsmethoden.](interface-property-methods.md)

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**ADsType**
</dt> <dd> <dl>

Der Datentyp des Werts der Eigenschaft, der aus der [**ADSTYPEENUM-Enumeration**](/windows/win32/api/iads/ne-iads-adstypeenum) der value-Eigenschaft übernommen wurde.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ADsType(
  [out] LONG* ADsType
);
HRESULT put_ADsType(
  [in] LONG ADsType
);
```


</dt> </dl> </dd> <dt>

**Boolean**
</dt> <dd> <dl>

Boolescher Wert.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Boolean(
  [out] LONG* lnBoolean
);
HRESULT put_Boolean(
  [in] LONG lnBoolean
);
```


</dt> </dl> </dd> <dt>

**CaseExactString**
</dt> <dd> <dl>

Zu interpretierende Zeichenfolge. Groß-/Kleinschreibung wird beachtet,

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CaseExactString(
  [out] BSTR* bstrCaseExactString
);
HRESULT put_CaseExactString(
  [in] BSTR bstrCaseExactString
);
```


</dt> </dl> </dd> <dt>

**CaseIgnoreString**
</dt> <dd> <dl>

Zu interpretierende Zeichenfolge. Diese Klasse berücksichtigt keine Groß-/Kleinschreibung.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CaseIgnoreString(
  [out] BSTR* bstrCaseIgnoreString
);
HRESULT put_CaseIgnoreString(
  [in] BSTR bstrCaseIgnoreString
);
```


</dt> </dl> </dd> <dt>

**DNString**
</dt> <dd> <dl>

Eine Zeichenfolge, die den Distinguished Name (Pfad) eines Verzeichnisdienstwertobjekts identifiziert.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DNString(
  [out] BSTR* bstrDNString
);
HRESULT put_DNString(
  [in] BSTR bstrDNString
);
```


</dt> </dl> </dd> <dt>

**Integer**
</dt> <dd> <dl>

Wert für ganze Zahl.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Integer(
  [out] LONG* lnInteger
);
HRESULT put_Integer(
  [in] LONG lnInteger
);
```


</dt> </dl> </dd> <dt>

**LargeInteger**
</dt> <dd> <dl>

Zeiger auf die [**IDispatch-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-idispatch) des Objekts, das [**IADsLargeInteger für diesen**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) Wert implementiert.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **IDispatch**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LargeInteger(
  [out] IDispatch** ppLargeInteger
);
HRESULT put_LargeInteger(
  [in] IDispatch* pLargeInteger
);
```


</dt> </dl> </dd> <dt>

**NumericString**
</dt> <dd> <dl>

Zu interpretierenden Text. Numerischer Typ.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NumericString(
  [out] BSTR* bstrNumericString
);
HRESULT put_NumericString(
  [in] BSTR bstrNumericString
);
```


</dt> </dl> </dd> <dt>

**OctetString**
</dt> <dd> <dl>

Variant-Array von Ein-Byte-Zeichen.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OctetString(
  [in] VARIANT* vOctetString
);
HRESULT put_OctetString(
  [in] VARIANT* vOctetString
);
```


</dt> </dl> </dd> <dt>

**PrintableString**
</dt> <dd> <dl>

Anzeigen oder Drucken einer Zeichenfolge.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrintableString(
  [out] BSTR* bstrPrintableString
);
HRESULT put_PrintableString(
  [in] BSTR bstrPrintableString
);
```


</dt> </dl> </dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl>

Zeiger auf die [**IDispatch-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-idispatch) des Objekts, das [**IADsSecurityDescriptor für**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) diesen Wert implementiert.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **IDispatch**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SecurityDescriptor(
  [out] IDispatch** ppSecurityDescriptor
);
HRESULT put_SecurityDescriptor(
  [in] IDispatch* pSecurityDescriptor
);
```


</dt> </dl> </dd> <dt>

**UTCTime**
</dt> <dd> <dl>

Ein Datum des **VT \_ DATE-Typs,** ausgedrückt koordinierte Weltzeit UTC-Format.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **DATE**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UTCTime(
  [out] DATE* daUTCTime
);
HRESULT put_UTCTime(
  [in] DATE daUTCTime
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Hinweise

Die [**IADsPropertyValue-Eigenschaften**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) legen nur einen Eigenschaftswert des angegebenen Typs fest oder rufen diesen ab. Beispielsweise führt die **CaseIgnoreString-Eigenschaft** für ein Attribut vom Typ **ADSTYPE \_ DN \_ STRING** wie das **distinguishedName-Attribut** zu einem Fehler. Die **CaseIgnoreString-Eigenschaft** funktioniert nur für Attribute vom Typ **ADS CASE IGNORE \_ \_ \_ STRING**. Die folgende Tabelle ordnet den [**ADSTYPEENUM-Wert**](/windows/win32/api/iads/ne-iads-adstypeenum) der entsprechenden **IADsPropertyValue-Eigenschaft** zu, die für den Zugriff auf diesen Attributtyp verwendet werden kann. Wenn ein **ADSTYPEENUM-Wert** in dieser Tabelle nicht aufgeführt ist, ist er nicht über die **IADsPropertyValue-Schnittstelle** verfügbar. Die [**IADsPropertyValue2-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2) sollte verwendet werden, um Daten in den anderen Formaten zu erhalten.



| [**ADSTYPEENUM-Wert**](/windows/win32/api/iads/ne-iads-adstypeenum) | [**IADsPropertyValue-Eigenschaft**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) |
|------------------------------------------|---------------------------------------------------------|
| **ADSTYPE \_ DN \_ STRING**                  | **DNString**                                            |
| **ADSTYPE \_ CASE \_ EXACT \_ STRING**         | **CaseExactString**                                     |
| **ADSTYPE \_ CASE \_ IGNORE \_ STRING**        | **CaseIgnoreString**                                    |
| **DRUCKBARE \_ \_ ADSTYPE-ZEICHENFOLGE**           | **PrintableString**                                     |
| **NUMERISCHE \_ \_ ADSTYPE-ZEICHENFOLGE**             | **NumericString**                                       |
| **ADSTYPE \_ BOOLEAN**                     | **Boolean**                                             |
| **ADSTYPE \_ INTEGER**                     | **Integer**                                             |
| **ADSTYPE \_ OCTET \_ STRING**               | **OctetString**                                         |
| **ADSTYPE \_ UTC \_ TIME**                   | **UTCTime**                                             |
| **ADSTYPE \_ LARGE \_ INTEGER**              | **LargeInteger**                                        |
| **ADSTYPE \_ NT \_ SECURITY \_ DESCRIPTOR**    | **SecurityDescriptor**                                  |



 

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel zeigt, wie eine Eigenschaft aus der Eigenschaftenliste abgerufen wird.


```VB
Dim propList As IADsPropertyList
Dim propEntry As IADsPropertyEntry
Dim propVal As IADsPropertyValue

On Error GoTo Cleanup
 
' Retrieve the property list.
Set propList = GetObject("LDAP://dc01/DC=Fabrikam,DC=com")
propList.GetInfo
 
' Retrieve a property entry. If you are certain of the property type,
' replace ADSTYPE_UNKNOWN with the actual property type.
Set propEntry = propList.GetPropertyItem("description", ADSTYPE_UNKNOWN)
 
' Print the property entry values.
For Each v In propEntry.Values
    Set propVal = v
    Select Case propVal.ADsType
        Case ADSTYPE_CASE_EXACT_STRING
            Debug.Print propVal.CaseExactString
        Case ADSTYPE_CASE_IGNORE_STRING
            Debug.Print propVal.CaseIgnoreString
        Case Else
            Debug.Print "Unable to handle a property of type: " & propVal.ADsType
    End Select
    
Next

Cleanup:
    If (Err.Number<>0) Then
       Debug.Print "An error has occurred. " & Err.Number
    End If
    Set propList = Nothing
    Set propEntry = Nothing
    Set propVal = Nothing
```



Der folgende Code zeigt, wie **IADsPropertyValue::get \_ CaseIgnoreString** verwendet wird, um den Wert der description-Eigenschaft aus einer Eigenschaftenliste abzurufen.


```C++
#include <activeds.h>
#include <stdio.h>
 
IADsPropertyList *pList = NULL;
IADsPropertyEntry *pEntry = NULL;
IADsPropertyValue *pVal = NULL;
IADs *pObj = NULL;
VARIANT var, varItem;
BSTR valStr;
IEnumVARIANT *pEnum = NULL;
LONG lstart = 0;
LONG lend = 0;
LONG lADsType = ADSTYPE_UNKNOWN;
 
VariantInit(&var);
VariantInit(&varItem);
 
// Bind to the directory object.
HRESULT hr = ADsGetObject(L"LDAP://dc01/DC=Fabrikam,DC=com",
                          IID_IADsPropertyList,
                          (void**)&pList);

if(FAILED(hr)){goto Cleanup;}

// Initialize the property cache.
hr = pList->QueryInterface(IID_IADs,(void**)&pObj);
if(FAILED(hr)){goto Cleanup;}

pObj->GetInfo();
pObj->Release();
 
// Retrieve the property entry.
hr = pList->GetPropertyItem(CComBSTR("description"), ADSTYPE_CASE_IGNORE_STRING, &var);
pList->Release();
if(FAILED(hr)){goto Cleanup;}

hr = V_DISPATCH(&var)->QueryInterface(IID_IADsPropertyEntry,
                                      (void**)&pEntry);
VariantClear(&var);
if(FAILED(hr)){goto Cleanup;}
 
// Retrieve the value array of the property entry.
hr = pEntry->get_Values(&var);
if(FAILED(hr)){goto Cleanup;}

SAFEARRAY *sa = V_ARRAY( &var );
 
// Retrieve the lower and upper bound. Iterate and print the values.
hr = SafeArrayGetLBound( sa, 1, &lstart );
hr = SafeArrayGetUBound( sa, 1, &lend );
printf(" Property value(s) = ");
for ( long idx=lstart; idx < lend+1; idx++ )    {
    hr = SafeArrayGetElement( sa, &idx, &varItem );
    hr = V_DISPATCH(&varItem)->QueryInterface(IID_IADsPropertyValue,
                                              (void**)&pVal);
    if(FAILED(hr)){goto Cleanup;}

    pVal->get_ADsType(&lADsType);

    switch(lADsType)
    {
        case ADSTYPE_CASE_IGNORE_STRING:
        {
            hr = pVal->get_CaseIgnoreString(&valStr);
            break;
        }
        case ADSTYPE_CASE_EXACT_STRING:
        {
            hr = pVal->get_CaseExactString(&valStr);
            break;
        }
        default:
        {
            valStr = SysAllocString(L"Unable to handle a property of this type");
            break;
        }
    }

    if(FAILED(hr)){goto Cleanup;}
    printf(" %S ", valStr);
    SysFreeString(valStr);
    VariantClear(&varItem);
}
printf("\n");

Cleanup:
    if(pList)
        pList = NULL;

    if(pEntry)
        pEntry = NULL;

    if(pVal)
        pVal = NULL;

    if(pObj)
        pObj = NULL;

    if(pEnum)
        pEnum = NULL;

    SysFreeString(valStr);
    VariantClear(&varItem);
    VariantClear(&var);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsPropertyValue ist als 79FA9AD0-A97C-11D0-8534-00C04FD8D503 definiert.<br/>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)
</dt> <dt>

[**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum)
</dt> <dt>

[**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)
</dt> <dt>

[**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)
</dt> <dt>

[**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)
</dt> <dt>

[**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> </dl>

 

