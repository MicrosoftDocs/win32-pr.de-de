---
title: IADsOU-Eigenschaftenmethoden (Iads.h)
description: Die Eigenschaftenmethoden der IADsOU-Schnittstelle erhalten oder legen die in der folgenden Tabelle aufgeführten Eigenschaften fest. Weitere Informationen finden Sie unter Schnittstelleneigenschaftsmethoden.
ms.assetid: 8cb84972-733b-47ca-8647-1b7a85c97021
ms.tgt_platform: multiple
keywords:
- IADsOU-Eigenschaftenmethoden ADSI
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
ms.openlocfilehash: 019fb93575bc8b8b419797c7efdf41c15a6375172a834f48626befd3526b3b2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179529"
---
# <a name="iadsou-property-methods"></a>IADsOU-Eigenschaftenmethoden

Die Eigenschaftenmethoden der [**IADsOU-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadsou) erhalten oder legen die in der folgenden Tabelle aufgeführten Eigenschaften fest. Weitere Informationen finden Sie unter [Schnittstelleneigenschaftsmethoden.](interface-property-methods.md)

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**BusinessCategory**
</dt> <dd> <dl>

Eine Zeichenfolge, die die allgemeine Geschäftsfunktion oder die funktionen enthält, die von der Organisationseinheit ausgeführt werden, z. B. "Buchhaltung".

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **BSTR**
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

**FaxNumber**
</dt> <dd> <dl>

Eine Zeichenfolge, die die Faksimilenummer der Organisationseinheit enthält.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **BSTR**
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

**LocalityName**
</dt> <dd> <dl>

Eine Zeichenfolge, die den Namen der geografischen Region der Organisationseinheit enthält.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **BSTR**
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

Eine Zeichenfolge, die die Postadresse der Organisationseinheit enthält.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **BSTR**
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

Ein Array von Zeichenfolgen, das die Distinguished Names anderer Verzeichnisobjekte enthält, die für dieses Objekt relevant sein können.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **VARIANT**
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

Skriptdatentyp: **BSTR**
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

Im folgenden Codebeispiel werden **businessCategory** und **Description aller** Organisationseinheiten in einem Container angezeigt. Es wird davon ausgegangen, dass der zugrunde liegende Verzeichnisdienst das Gruppieren von Verzeichnisobjekten nach Organisationseinheit unterstützt.


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
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsOU ist als A2F733B8-KVE-11CF-8ABC-00C04FD8D503 definiert.<br/>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IADsOU**](/windows/desktop/api/Iads/nn-iads-iadsou)
</dt> <dt>

[Schnittstelleneigenschaftsmethoden](interface-property-methods.md)
</dt> </dl>

 

 





