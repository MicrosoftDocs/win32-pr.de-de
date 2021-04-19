---
title: Iadsou-Eigenschaften Methoden (IADs. h)
description: Mit den Eigenschafts Methoden der iadsou-Schnittstelle werden die in der folgenden Tabelle aufgeführten Eigenschaften angezeigt oder festgelegt. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: 8cb84972-733b-47ca-8647-1b7a85c97021
ms.tgt_platform: multiple
keywords:
- Iadsou-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsOU Property Methods
- IADsOU.BusinessCategory
- IADsOU.get_BusinessCategory
- IADsOU.put_BusinessCategory
- IADsOU.Description
- IADsOU.get_Description
- IADsOU.put_Description
- IADsOU.FaxNumber
- IADsOU.get_FaxNumber
- IADsOU.put_FaxNumber
- IADsOU.LocalityName
- IADsOU.get_LocalityName
- IADsOU.put_LocalityName
- IADsOU.PostalAddress
- IADsOU.get_PostalAddress
- IADsOU.put_PostalAddress
- IADsOU.TelephoneNumber
- IADsOU.get_TelephoneNumber
- IADsOU.put_TelephoneNumber
- IADsOU.SeeAlso
- IADsOU.get_SeeAlso
- IADsOU.put_SeeAlso
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0ce30fad6a690a26a8e16b817b77b129dee25f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342854"
---
# <a name="iadsou-property-methods"></a>Iadsou-Eigenschaften Methoden

Mit den Eigenschafts Methoden der [**iadsou**](/windows/desktop/api/Iads/nn-iads-iadsou) -Schnittstelle werden die in der folgenden Tabelle aufgeführten Eigenschaften angezeigt oder festgelegt. Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**Businesscategory**
</dt> <dd> <dl>

Eine Zeichenfolge, die die allgemeine Geschäftsfunktion oder die von der Organisationseinheit ausgeführten Funktionen enthält, z. b. "Accounting".

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_BusinessCategory(
  [out] BSTR* pbstrBusinessCategory
);
HRESULT put_BusinessCategory(
  [in] BSTR bstrBusinessCategory
);
```


</dt> </dl> </dd> <dt>

**Beschreibung**
</dt> <dd> <dl>

Eine Zeichenfolge, die eine Textbeschreibung der Organisationseinheit enthält.

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

Eine Zeichenfolge, die die Faxnummer der Organisationseinheit enthält.

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

Eine Zeichenfolge, die den Namen des geografischen Bereichs der Organisationseinheit enthält.

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

Eine Zeichenfolge, die die Postanschrift der Organisationseinheit enthält.

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

Ein Array von Zeichen folgen, das die Distinguished Names von anderen Verzeichnis Objekten enthält, die für dieses Objekt relevant sein können.

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

Eine Zeichenfolge, die die Telefonnummer der Organisationseinheit enthält.

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

Im folgenden Codebeispiel werden die **businesscategory** und die **Beschreibung** aller Organisationseinheiten in einem Container angezeigt. Dabei wird davon ausgegangen, dass der zugrunde liegende Verzeichnisdienst das Gruppieren von Verzeichnis Objekten nach Organisationseinheit unterstützt.


```VB
Dim dom As IADsContainer
Dim ou As IADsOU

' Bind to the container.
Set dom = GetObject("LDAP://server1/domain1")

' Filter out all objects that are not of class "organizationalUnit".
dom.filter = Array("organizationalUnit")

' Enumerate the organizational units in the container and display  
' the BusinessCategory and Description properties of each OU.
For Each ou In dom
    MsgBox ou.BusinessCategory & ": " & ou.Description
Next
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ iadsou ist als A2F733B8-Effe-11CF-8ABC-00C04FD8D503 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iadsou**](/windows/desktop/api/Iads/nn-iads-iadsou)
</dt> <dt>

[Schnittstelleneigenschaften Methoden](interface-property-methods.md)
</dt> </dl>

 

 





