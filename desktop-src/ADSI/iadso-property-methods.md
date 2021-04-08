---
title: Iadso-Eigenschaften Methoden (IADs. h)
description: Mit den Eigenschafts Methoden der iadso-Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: d4bc1d29-98de-462d-b59c-2bc2641c25a0
ms.tgt_platform: multiple
keywords:
- Iadso-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsO Property Methods
- IADsO.Description
- IADsO.get_Description
- IADsO.put_Description
- IADsO.FaxNumber
- IADsO.get_FaxNumber
- IADsO.put_FaxNumber
- IADsO.LocalityName
- IADsO.get_LocalityName
- IADsO.put_LocalityName
- IADsO.PostalAddress
- IADsO.get_PostalAddress
- IADsO.put_PostalAddress
- IADsO.TelephoneNumber
- IADsO.get_TelephoneNumber
- IADsO.put_TelephoneNumber
- IADsO.SeeAlso
- IADsO.get_SeeAlso
- IADsO.put_SeeAlso
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09840cf62d6883eb4f5ca326998b697a34698c90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742688"
---
# <a name="iadso-property-methods"></a>Iadso-Eigenschaften Methoden

Mit den Eigenschafts Methoden der [**iadso**](/windows/desktop/api/Iads/nn-iads-iadso) -Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt. Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**Beschreibung**
</dt> <dd> <dl>

Die Beschreibung der Organisation.

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

**Faxnummer**
</dt> <dd> <dl>

Die Faxnummer (Fax) der Organisation.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_FaxNumber(
  [out] BSTR* pbstrFaxNumber
);
HRESULT put_FaxNumber(
  [in] BSTR bstrFaxNumber
);
```


</dt> </dl> </dd> <dt>

**Localityname**
</dt> <dd> <dl>

Der Name des Orts, an dem sich die Organisation befindet.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LocalityName(
  [out] BSTR* pbstrLocalityName
);
HRESULT put_LocalityName(
  [in] BSTR bstrLocalityName
);
```


</dt> </dl> </dd> <dt>

**PostalAddress**
</dt> <dd> <dl>

Die Postanschrift der Organisation.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PostalAddress(
  [out] BSTR* pbstrPostalAddress
);
HRESULT put_PostalAddress(
  [in] BSTR bstrPostalAddress
);
```


</dt> </dl> </dd> <dt>

**SeeAlso**
</dt> <dd> <dl>

Ein Array von ADsPath-Namen anderer ADSI-Objekte, die für dieses Objekt relevant sein können.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SeeAlso(
  [out] VARIANT* pvSeeAlso
);
HRESULT put_SeeAlso(
  [in] VARIANT vSeeAlso
);
```


</dt> </dl> </dd> <dt>

**TelephoneNumber**
</dt> <dd> <dl>

Die Telefonnummer der Organisation.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TelephoneNumber(
  [out] BSTR* pbstrTelephoneNumber
);
HRESULT put_TelephoneNumber(
  [in] BSTR bstrTelephoneNumber
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird die Beschreibung einer bestimmten Organisation angezeigt. Dabei wird davon ausgegangen, dass der zugrunde liegende Verzeichnisdienst das Gruppieren von Verzeichnis Objekten nach Organisation unter


```VB
Dim dom As IADsContainer
Dim dso As IADsOpenDSObject
Dim szUsername As String
Dim szPassword As String
On Error GoTo Cleanup

' Insert code to securely retrieve the user name and password
 
Set dso = GetObject("LDAP:")
Set dom = dso.OpenDSObject("LDAP://adsrv1/dc=Fabrikam, dc=Com", _
                           szUsername, szPassword,1)
dom.Filter = Array("organization")
For Each o In dom
    MsgBox "Fax number of " & o.Name & " : " & o.Description
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set dom = Nothing
    Set dso = Nothing
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ iadso ist als A1CD2DC6-Effe-11CF-8ABC-00C04FD8D503 definiert.<br/>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iadso**](/windows/desktop/api/Iads/nn-iads-iadso)
</dt> <dt>

[Schnittstelleneigenschaften Methoden](interface-property-methods.md)
</dt> </dl>

 

 





