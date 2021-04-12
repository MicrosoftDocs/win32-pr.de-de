---
title: Iadsfileshare-Eigenschaften Methoden (IADs. h)
description: Mit den Eigenschafts Methoden der iadsfileshare-Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: c5a81c42-507f-4a68-b6f4-83097bd0fa01
ms.tgt_platform: multiple
keywords:
- Iadsfileshare-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsFileShare Property Methods
- IADsFileShare.CurrentUserCount
- IADsFileShare.get_CurrentUserCount
- IADsFileShare.Description
- IADsFileShare.get_Description
- IADsFileShare.put_Description
- IADsFileShare.HostComputer
- IADsFileShare.get_HostComputer
- IADsFileShare.put_HostComputer
- IADsFileShare.MaxUserCount
- IADsFileShare.get_MaxUserCount
- IADsFileShare.Path
- IADsFileShare.get_Path
- IADsFileShare.put_Path
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f38369a4054f1848d5e35ff8bdb2dda9e9423a87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105140"
---
# <a name="iadsfileshare-property-methods"></a>Iadsfileshare-Eigenschaften Methoden

Mit den Eigenschafts Methoden der [**iadsfileshare**](/windows/desktop/api/Iads/nn-iads-iadsfileshare) -Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt. Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**Currentusercount**
</dt> <dd> <dl>

Die Anzahl der Benutzer, die mit der Freigabe verbunden sind.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skript Datentyp: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CurrentUserCount(
  [out] LONG* plCurrentUserCount
);
```


</dt> </dl> </dd> <dt>

**Beschreibung**
</dt> <dd> <dl>

Die Beschreibung der Dateifreigabe.

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

**Host Computer**
</dt> <dd> <dl>

Ein ADsPath-Verweis auf den Host Computer.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HostComputer(
  [out] BSTR* pbstrHostComputer
);
HRESULT put_HostComputer(
  [in] BSTR bstrHostComputer
);
```


</dt> </dl> </dd> <dt>

**MaxUserCount**
</dt> <dd> <dl>

Die maximale Anzahl von Benutzern, die gleichzeitig auf die Freigabe zugreifen dürfen.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skript Datentyp: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxUserCount(
  [out] LONG* plMaxUserCount
);
```


</dt> </dl> </dd> <dt>

**Pfad**
</dt> <dd> <dl>

Der Dateisystempfad zum freigegebenen Verzeichnis.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* pbstrPath
);
HRESULT put_Path(
  [in] BSTR bstrPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Beispiele

Wenn Sie auf die Eigenschaften von Dateifreigaben auf einem Computer zugreifen möchten, müssen Sie zunächst eine Bindung an den "LanManServer" auf dem Computer herstellen. Im folgenden Codebeispiel wird gezeigt, wie Sie die Beschreibung und die maximale Anzahl zulässiger Benutzer für alle öffentlichen Dateifreigaben auf dem Computer (mit dem Namen "MyMachine") in der Standard Domäne einrichten.


```VB
Dim fs As IADsFileService
Dim share As IADsFileShare
On Error GoTo Cleanup

Set fs = GetObject("WinNT://myMachine/LanmanServer")
If (fs.class = "FileService") Then
    For Each share In fs
        share.description = share.name & " is my working folder."
        share.MaxUserCount =  10
        share.SetInfo
    Next share
End if

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fs = Nothing
    Set share = Nothing
```



Im folgenden Codebeispiel wird gezeigt, wie das vorhandene Verzeichnis "C: \\ MyFolder" als öffentliche Dateifreigabe erstellt wird.


```VB
Dim fs As IADsFileShare
Dim cont As IADsContainer
On Error GoTo Cleanup
 
Set cont = GetObject("WinNT://yourDomain/yourMachineName/LanmanServer")
 
Set fs = cont.Create("FileShare", "Public")
Debug.Print fs.Class
fs.Path = "C:\MyFolder"
fs.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cont = Nothing
    Set fs = Nothing
```



Im folgenden Codebeispiel wird das vorhandene Verzeichnis C: \\ MyFolder zu einer öffentlichen Dateifreigabe.


```C++
IADsFileShare *pShare = NULL;
IADsContainer *pCont = NULL;
LPWSTR adsPath = L"WinNT://yourMachineName/LanmanServer";
HRESULT hr = S_OK;

hr = ADsGetObject(adsPath, IID_IADsContainer,(void**)&pCont);
if(FAILED(hr)) {goto Cleanup;}

hr = pCont->Create(CComBSTR("FileShare"), CComBSTR("Public"), (IDispatch**)&pShare);

if(FAILED(hr)) {goto Cleanup;}

hr = pShare->put_Path(CComBSTR("c:\\public"));

if(FAILED(hr)) {goto Cleanup;}

hr = pShare->SetInfo();

Cleanup:
    if(pCont) pCont->Release();
    if(pShare) pShare->Release();
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ iadsfileshare ist als EB6DCAF0-4B83-11CF-A995-00AA006BC149 definiert.<br/>        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iadsservice**](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[**Iadsfileshare**](/windows/desktop/api/Iads/nn-iads-iadsfileshare)
</dt> <dt>

[Schnittstelleneigenschaften Methoden](interface-property-methods.md)
</dt> </dl>

 

 





