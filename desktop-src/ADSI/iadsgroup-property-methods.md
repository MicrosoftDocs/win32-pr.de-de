---
title: IADsGroup-Eigenschaften Methoden (IADs. h)
description: Eigenschaften Methoden der IADsGroup-Schnittstelle.
ms.assetid: a8aa88d4-4695-47bc-bf7f-a17236a5671c
ms.tgt_platform: multiple
keywords:
- IADsGroup-Eigenschaften Methoden ADSI
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
ms.openlocfilehash: 665cb91a55298012e4e906c2972da5371e3960be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346320"
---
# <a name="iadsgroup-property-methods"></a>IADsGroup-Eigenschaften Methoden

Mit den Eigenschafts Methoden der [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) -Schnittstelle werden die folgenden Eigenschaften gelesen und geschrieben. Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**Beschreibung**
</dt> <dd> <dl>

Gibt die Textbeschreibung der Gruppenmitgliedschaft an.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
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

 

## <a name="remarks"></a>Bemerkungen

### <a name="using-iadsgroup-to-retrieve-descriptions-of-built-in-groups"></a>Verwenden von IADsGroup zum Abrufen von Beschreibungen integrierter Gruppen

In den folgenden Beispielen wird gezeigt, wie Informationen zu Windows-Gruppen Objekten nach Namen abgerufen werden. In einer mehrsprachigen Umgebung sind integrierte Gruppen manchmal durch unterschiedliche lokalisierte Namen bekannt. Dies bedeutet, dass Sie nicht direkt mithilfe von Zeichen folgen Bezeichnerzeichen (z. b. "Winnt://Microsoft/Administrators") abgerufen werden können. In diesem Fall kann der Benutzer an das bekannte SID-Objekt für die Gruppe binden, den lokalisierten Gruppennamen abrufen und ihn für die GetObject-Methode bereitstellen. Weitere Informationen finden Sie unter [Bekannte SIDs](/windows/desktop/SecAuthZ/well-known-sids).

## <a name="examples"></a>Beispiele

Im folgenden Visual Basic Beispiel wird gezeigt, wie eine Bindung an ein Gruppen Objekt und die Beschreibung der Gruppe angezeigt wird.


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



Im folgenden C++-Beispiel wird gezeigt, wie eine Bindung an ein Gruppen Objekt erfolgen und die Beschreibung der Gruppe angezeigt wird.


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
| Header<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsGroup ist als 27636b00-410f-11CF-B1FF-02608c9e7553 definiert.<br/>            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup)
</dt> <dt>

[Schnittstelleneigenschaften Methoden](interface-property-methods.md)
</dt> </dl>

 

