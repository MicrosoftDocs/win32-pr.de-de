---
title: Iadsfileservice-Eigenschaften Methoden (IADs. h)
description: Mit den Eigenschafts Methoden der iadsfileservice-Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: 1455df61-9218-450b-b956-1cf127364f24
ms.tgt_platform: multiple
keywords:
- Iadsfileservice-Eigenschaften Methoden ADSI
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
ms.openlocfilehash: e1f3a46b37522bbdce6e99b969811e2909c8ecc9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518461"
---
# <a name="iadsfileservice-property-methods"></a>Iadsfileservice-Eigenschaften Methoden

Mit den Eigenschafts Methoden der [**iadsfileservice**](/windows/desktop/api/Iads/nn-iads-iadsfileservice) -Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt. Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**Beschreibung**
</dt> <dd> <dl>

Die Beschreibung des Datei Dienstanbieter.

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


</dt> </dl> </dd> <dt>

**MaxUserCount**
</dt> <dd> <dl>

Die maximal zulässige Anzahl von Benutzern, die für den Dienst zulässig sind.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
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

 

## <a name="remarks"></a>Bemerkungen

Sie müssen den Datei Dienst durchlaufen, um auf Dateifreigaben, Sitzungen und Ressourcen auf einem Computer zuzugreifen.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird eine Beschreibung für geschrieben und das Benutzerlimit des Datei Dienstanbieter überprüft.


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



Im folgenden Codebeispiel wird eine Beschreibung für geschrieben und das Benutzerlimit für ein Datei Dienst Objekt überprüft.


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
| Header<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ iadsfileservice ist als A89D1900-31CA-11CF-A98A-00AA006BC149 definiert.<br/>      |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iadsservice**](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[**Iadsfileservice**](/windows/desktop/api/Iads/nn-iads-iadsfileservice)
</dt> <dt>

[**Iadsfileserviceoperations**](/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations)
</dt> <dt>

[**Iadsserviceoperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)
</dt> <dt>

[Schnittstelleneigenschaften Methoden](interface-property-methods.md)
</dt> </dl>

 

 





