---
title: IADsGroup-Eigenschaftenmethoden (Iads.h)
description: Eigenschaftsmethoden der IADsGroup-Schnittstelle.
ms.assetid: a8aa88d4-4695-47bc-bf7f-a17236a5671c
ms.tgt_platform: multiple
keywords:
- IADsGroup-Eigenschaftenmethoden ADSI
topic_type:
- apiref
api_name:
- IADsGroup Property Methods
- IADsGroup.Description
- IADsGroup.get_Description
- IADsGroup.put_Description
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f15a55765a10afef10087e7b28d04304ab0cc2668915a6e6ffa71fc770eb54a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082404"
---
# <a name="iadsgroup-property-methods"></a>IADsGroup-Eigenschaftenmethoden

Die Eigenschaftenmethoden der [**IADsGroup-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadsgroup) lesen und schreiben die folgenden Eigenschaften. Weitere Informationen finden Sie unter [Schnittstelleneigenschaftsmethoden.](interface-property-methods.md)

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**Beschreibung**
</dt> <dd> <dl>

Gibt die Textbeschreibung der Gruppenmitgliedschaft an.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Hinweise

### <a name="using-iadsgroup-to-retrieve-descriptions-of-built-in-groups"></a>Verwenden von IADsGroup zum Abrufen von Beschreibungen integrierter Gruppen

In den folgenden Beispielen wird gezeigt, wie Sie Informationen zu Windows Nach Namen gruppieren. In einer mehrsprachigen Umgebung sind integrierte Gruppen manchmal durch verschiedene lokalisierte Namen bekannt, was bedeutet, dass sie nicht direkt mithilfe von Zeichenfolgenbezeichnern wie "WinNT://Microsoft/Administrators" abgerufen werden können. In diesem Fall kann der Benutzer eine Bindung an das bekannte SID-Objekt für die Gruppe erstellen, den lokalisierten Gruppennamen abrufen und an die GetObject-Methode angeben. Weitere Informationen finden Sie unter [Bekannte SIDs.](/windows/desktop/SecAuthZ/well-known-sids)

## <a name="examples"></a>Beispiele

Im folgenden Visual Basic wird veranschaulicht, wie eine Bindung an ein Gruppenobjekt erstellt und die Beschreibung der Gruppe angezeigt wird.


```VB
Dim grp As IADsGroup
On Error GoTo Cleanup

Set grp = GetObject("WinNT://Microsoft/Administrators")
Debug.Print grp.Description

Cleanup
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set grp = Nothing
```



Im folgenden C++-Beispiel wird veranschaulicht, wie eine Bindung an ein Gruppenobjekt erstellt und die Beschreibung der Gruppe angezeigt wird.


```C++
IADsGroup *pGroup = NULL;
HRESULT hr = S_OK;
LPWSTR adsPath = L"WinNT://localHost/Administrators";
BSTR bstr;

hr = ADsGetObject(adsPath,IID_IADsGroup,(void**)&pGroup);

if(FAILED(hr)) {goto Cleanup;}

hr = pGroup->get_Description(&bstr);
if(FAILED(hr)) {goto Cleanup;}

printf("Description: %S\n",bstr);

Cleanup:
    SysFreeString(bstr);
    if(pGroup) 
        pGroup->Release();

    return hr;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsGroup ist als 27636B00-410F-11CF-B1FF-02608C9E7553 definiert.<br/>            |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Iads**](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup)
</dt> <dt>

[Schnittstelleneigenschaftsmethoden](interface-property-methods.md)
</dt> </dl>

 

