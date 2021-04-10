---
title: IADsContainer-Eigenschaften Methoden (IADs. h)
description: Mit den Eigenschafts Methoden der IADsContainer-Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt. Weitere Informationen und eine allgemeine Erörterung von Eigenschaften Methoden finden Sie unter Interface Property Methods.
ms.assetid: 74d348bf-7b7f-4971-ba03-f77940600674
ms.tgt_platform: multiple
keywords:
- IADsContainer-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsContainer Property Methods
- IADsContainer.Count
- IADsContainer.get_Count
- IADsContainer.Filter
- IADsContainer.get_Filter
- IADsContainer.put_Filter
- IADsContainer.Hints
- IADsContainer.get_Hints
- IADsContainer.put_Hints
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5196addda0d9ff89f8a4976f3197bbeeae07044
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105152"
---
# <a name="iadscontainer-property-methods"></a>IADsContainer-Eigenschaften Methoden

Mit den Eigenschafts Methoden der [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) -Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt. Weitere Informationen und eine allgemeine Erörterung von Eigenschaften Methoden finden Sie unter [Interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**Count**
</dt> <dd> <dl>

Ruft die Anzahl der Elemente im Container ab. Wenn **Filter** festgelegt ist, gibt **count** nur die Anzahl der gefilterten Elemente zurück.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skript Datentyp: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* plCount
);
```


</dt> </dl> </dd> <dt>

**Filter**
</dt> <dd> <dl>

Ruft den Filter ab, mit dem Objektklassen in einer angegebenen Enumeration ausgewählt werden, oder legt diesen fest. Dabei handelt es sich um ein Variant-Array, bei dem es sich bei jedem Element um den Namen einer Schema Klasse handelt. Wenn **Filter** nicht festgelegt oder auf leer festgelegt ist, werden alle Objekte aller Klassen vom Enumerator abgerufen.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Filter(
  [out] VARIANT* pvFilter
);
HRESULT put_Filter(
  [in] VARIANT vFilter
);
```


</dt> </dl> </dd> <dt>

**Hinweise**
</dt> <dd> <dl>

Ein Variant-Array von **BSTR** -Zeichen folgen. Jedes Element identifiziert den Namen einer Eigenschaft, die in der Schema Definition gefunden wurde. Der *vhints* -Parameter ermöglicht es dem Client, anzugeben, welche Attribute für jedes Enumerationsobjekt geladen werden sollen. Diese Daten können verwendet werden, um den Netzwerk Zugriff zu optimieren. Die genaue Implementierung ist jedoch Anbieter spezifisch und wird zurzeit nicht vom WinNT-Anbieter verwendet.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Hints(
  [out] VARIANT* pvHints
);
HRESULT put_Hints(
  [in] VARIANT vHints
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Bemerkungen

Die enumerationsprozesse unter [**IADsContainer:: get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) und **IADsContainer:: get \_ count** werden für die enthaltenen Objekte im Cache ausgeführt. Wenn ein Container eine große Anzahl von Objekten enthält, wirkt sich dies möglicherweise negativ auf die Leistung aus. Um die Leistung zu verbessern, deaktivieren Sie den Cache, richten Sie eine geeignete Seitengröße ein, und verwenden Sie die [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle. Aus diesem Grund wird die Eigenschaft **get \_ count** im Microsoft LDAP-Anbieter nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden Visual Basic Codebeispiel wird gezeigt, wie Eigenschafts Methoden von [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) verwendet werden können.


```VB
Dim cont As IADsContainer
Dim usr As IADsUser

On Error GoTo Cleanup
 
Set cont = GetObject("LDAP://OU=Sales, DC=Fabrikam, DC=COM")
cont.Hints = Array("adminDescription") ' Load this attribute. Optional.
Debug.Print cont.Get("adminDescription")

' Filter users.
cont.Filter = Array("user")

For Each usr In cont
  Debug.Print usr.Name
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cont = Nothing
    Set usr = Nothing
```



Im folgenden C++-Codebeispiel wird gezeigt, wie die-Eigenschaften Methoden von [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) verwendet werden können. Aus Gründen der Übersichtlichkeit wird die Fehlerüberprüfung ausgelassen.


```C++
IADsContainer *pCont;
IADs *pChild;
IADs *pADs;
 
HRESULT hr = ADsGetObject(L"LDAP://OU=Sales,DC=Fabrikam,DC=COM",
                          IID_IADsContainer, 
                          (void**)&pCont);

if(FAILED(hr)){goto Cleanup;}

LPWSTR pszArray[] = { L"adminDescription" };
DWORD dwNumber = sizeof(pszArray)/sizeof(LPWSTR);
hr = ADsBuildVarArrayStr( pszArray, dwNumber, &var);
if(FAILED(hr)){goto Cleanup;}

hr = pCont->put_Hints( var );
if(FAILED(hr)){goto Cleanup;}

VariantClear(&var);
 
hr = pCont->QueryInterface(IID_IADs, (void**)pADs);
if(FAILED(hr)){goto Cleanup;}
 
hr = pADs->Get(CComBSTR("adminDescription"), var);
 
LPWSTR pszUsers = {L"user"};
dwNumber = sizeof(pszUsers)/sizeof(LPWSTR);
hr = ADsBuildVarArrayStr(pszUsers, dwNumber, &var);
hr = pCont->put_Filter( var );
VariantClear(&var);
 
// Enumerate user objects in the container.
IEnumVARIANT *pEnum = NULL;
hr = ADsBuildEnumerator(pCont, &pEnum);
pCont->Release();    // Not required when users are enumerated.
 
ULONG lFetch;
VariantClear(&var);
while (SUCCEEDED(ADsEnumerateNext(pEnum, 1, &var, &lFetch)) && 
                      lFetch==1) {
    hr = V_DISPATCH(&var)->QueryInterface(IID_IADs, (void**)&pChild)
    if(SUCCEEDED(hr)) {
        BSTR bstrName;
        pChild->get_Name(&bstrName);
        printf("  %S\n", bstrName);
        SysFreeString(bstrName);
        pChild->Release();
    }
    VariantClear(&var);
}
Cleanup:
    if(pADs)
        pADs->Release();

    if(pCont)
        pCont->Release();

    if(pChild)
        pChild->Release();

    VariantClear(&var);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsContainer ist definiert als 001677d0-SD16-11CE-abc4-02608c9e7553<br/>        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> <dt>

[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)
</dt> </dl>

 

 





