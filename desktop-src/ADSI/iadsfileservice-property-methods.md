---
title: IADsFileService-Eigenschaftsmethoden (Iads.h)
description: Die Eigenschaftenmethoden der IADsFileService-Schnittstelle erhalten oder legen die in der folgenden Tabelle beschriebenen Eigenschaften fest. Weitere Informationen finden Sie unter Schnittstelleneigenschaftsmethoden.
ms.assetid: 1455df61-9218-450b-b956-1cf127364f24
ms.tgt_platform: multiple
keywords:
- IADsFileService-Eigenschaftsmethoden ADSI
topic_type:
- apiref
api_name:
- IADsFileService Property Methods
- IADsFileService.Description
- IADsFileService.get_Description
- IADsFileService.put_Description
- IADsFileService.MaxUserCount
- IADsFileService.get_MaxUserCount
- IADsFileService.put_MaxUserCount
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd12e1f9c52606f76cf6c0828767819e318874c323b22f5e1a91b70d71965465
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082444"
---
# <a name="iadsfileservice-property-methods"></a>IADsFileService-Eigenschaftsmethoden

Die Eigenschaftenmethoden der [**IADsFileService-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadsfileservice) erhalten oder legen die in der folgenden Tabelle beschriebenen Eigenschaften fest. Weitere Informationen finden Sie unter [Schnittstelleneigenschaftsmethoden.](interface-property-methods.md)

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**Beschreibung**
</dt> <dd> <dl>

Die Beschreibung des Dateidiensts.

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


</dt> </dl> </dd> <dt>

**MaxUserCount**
</dt> <dd> <dl>

Die maximale Anzahl von Benutzern, die für den Dienst zu einem beliebigen Zeitpunkt zulässig sind.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxUserCount(
  [out] LONG* plMaxUserCount
);
HRESULT put_MaxUserCount(
  [in] LONG lMaxUserCount
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Hinweise

Sie müssen den Dateidienst durchgehen, um auf Dateifreigaben, Sitzungen und Ressourcen auf einem Computer zu zugreifen.

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel schreibt eine Beschreibung für den Dateidienst und überprüft den Benutzergrenzwert.


```VB
Dim fs As IADsFileService
On Error GoTo Cleanup

' Bind to a file service object on "myComputer" in the local domain.
Set fs = GetObject("WinNT://myComputer/LanmanServer")

fs.Description = "WinNT file service."
n = fs.MaxUserCount
If n = -1 Then
   MsgBox "No limit has been imposed on number of users allowed."
Else
   MsgBox n & " users are allowed."
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fs = Nothing
```



Das folgende Codebeispiel schreibt eine Beschreibung für und überprüft das Benutzerlimit für ein Dateidienstobjekt.


```C++
HRESULT CheckFileService()
{
    IADsFileService *pFs = NULL;
    LPWSTR adsPath = L"WinNT://myComputer/LanmanServer";
    HRESULT hr = S_OK;
    long count = 0;

    hr = ADsGetObject(adsPath, IID_IADsFileService, (void**)&pFs)
    if(FAILED(hr)) {goto Cleanup;}

    hr = pFs->put_Description(CComBSTR("WinNT File Service"));
    if(FAILED(hr)) {goto Cleanup;}

    hr = pFs->SetInfo();
    if(FAILED(hr)) {goto Cleanup;}

    hr = pFs->get_MaxUserCount(&count);
    if(FAILED(hr)) {goto Cleanup;}

    if(count == -1) {
        printf("No limit has been imposed on the number of users.\n");
    } 
    else {
        printf("Number of allowed users are %d\n",count);
    }

Cleanup:
    if(pFs) pFs->Release();
    return S_OK;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsFileService ist als A89D1900-31CA-11CF-A98A-00AA006BC149 definiert.<br/>      |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[**IADsFileService**](/windows/desktop/api/Iads/nn-iads-iadsfileservice)
</dt> <dt>

[**IADsFileServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations)
</dt> <dt>

[**IADsServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)
</dt> <dt>

[Schnittstelleneigenschaftsmethoden](interface-property-methods.md)
</dt> </dl>

 

 





