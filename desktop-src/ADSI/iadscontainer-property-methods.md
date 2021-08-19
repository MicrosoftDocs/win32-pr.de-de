---
title: IADsContainer-Eigenschaftsmethoden (Iads.h)
description: Die Eigenschaftenmethoden der IADsContainer-Schnittstelle erhalten oder legen die in der folgenden Tabelle beschriebenen Eigenschaften fest. Weitere Informationen und eine allgemeine Erläuterung zu Eigenschaftsmethoden finden Sie unter Schnittstelleneigenschaftenmethoden.
ms.assetid: 74d348bf-7b7f-4971-ba03-f77940600674
ms.tgt_platform: multiple
keywords:
- IADsContainer-Eigenschaftsmethoden ADSI
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
ms.openlocfilehash: 13515bcf90c926db839aad60d49599967ee0d24bedbe0deb4b7d1d21c3c016e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428085"
---
# <a name="iadscontainer-property-methods"></a>IADsContainer-Eigenschaftsmethoden

Die Eigenschaftenmethoden der [**IADsContainer-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadscontainer) erhalten oder legen die in der folgenden Tabelle beschriebenen Eigenschaften fest. Weitere Informationen und eine allgemeine Erläuterung zu Eigenschaftsmethoden finden Sie unter [Schnittstelleneigenschaftenmethoden.](interface-property-methods.md)

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**Count**
</dt> <dd> <dl>

Ruft die Anzahl der Elemente im Container ab. Wenn **Filter** festgelegt ist, gibt **Count** nur die Anzahl der gefilterten Elemente zurück.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skriptdatentyp: **LONG**
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

Ruft den Filter ab, der zum Auswählen von Objektklassen in einer bestimmten Enumeration verwendet wird, oder legt diesen fest. Dies ist ein variant-Array, von dem jedes Element der Name einer Schemaklasse ist. Wenn **Filter** nicht auf leer festgelegt oder festgelegt ist, werden alle Objekte aller Klassen vom Enumerator abgerufen.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **VARIANT**
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

Ein Variantenarray von **BSTR-Zeichenfolgen.** Jedes Element identifiziert den Namen einer Eigenschaft, die sich in der Schemadefinition befindet. Mit dem *vHints-Parameter* kann der Client angeben, welche Attribute für jedes aufzählte Objekt geladen werden sollen. Diese Daten können verwendet werden, um den Netzwerkzugriff zu optimieren. Die genaue Implementierung ist jedoch anbieterspezifisch und wird derzeit nicht vom WinNT-Anbieter verwendet.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **VARIANT**
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

 

## <a name="remarks"></a>Hinweise

Die Enumerationsprozesse unter [**IADsContainer::get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) und **IADsContainer::get \_ Count** werden für die enthaltenen Objekte im Cache ausgeführt. Wenn ein Container eine große Anzahl von -Objekten enthält, kann die Leistung beeinträchtigt werden. Um die Leistung zu verbessern, deaktivieren Sie den Cache, richten Sie eine geeignete Seitengröße ein, und verwenden Sie die [**IDirectorySearch-Schnittstelle.**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) Aus diesem Grund wird die **\_ get Count-Eigenschaft** im Microsoft LDAP-Anbieter nicht unterstützt.

## <a name="examples"></a>Beispiele

Das folgende Visual Basic Codebeispiel zeigt, wie Eigenschaftsmethoden von [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) verwendet werden können.


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



Das folgende C++-Codebeispiel zeigt, wie die Eigenschaftsmethoden von [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) verwendet werden können. Aus Gründen der Kürze wird die Fehlerüberprüfung ausgelassen.


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
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsContainer ist als 001677D0-FD16-11CE-ABC4-02608C9E7553 definiert.<br/>        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> <dt>

[**Idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)
</dt> </dl>

 

 





