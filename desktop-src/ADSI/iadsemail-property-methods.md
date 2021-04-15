---
title: Iadenmail-Eigenschaften Methoden (IADs. h)
description: Die-Eigenschaften Methode der iadsemail-Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: 605ba62f-b15a-4411-839b-c4ad8acedd8a
ms.tgt_platform: multiple
keywords:
- Iadlmail-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsEmail Property Methods
- IADsEmail.Type
- IADsEmail.get_Type
- IADsEmail.put_Type
- IADsEmail.Address
- IADsEmail.get_Address
- IADsEmail.put_Address
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1956d5544b36cdaefcdd9d712ae99001d42279d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392117"
---
# <a name="iadsemail-property-methods"></a>Iadlmail-Eigenschaften Methoden

Die-Eigenschaften Methode der [**iadsemail**](/windows/desktop/api/Iads/nn-iads-iadsemail) -Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird. Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**Adresse**
</dt> <dd> <dl>

Die E-Mail-Adresse des Benutzers.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Address(
  [out] BSTR* retval
);
HRESULT put_Address(
  [in] BSTR bstrAddress
);
```


</dt> </dl> </dd> <dt>

**Type**
</dt> <dd> <dl>

Der Typ der e-Mail-Nachricht.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Type(
  [out] LONG* retVal
);
HRESULT put_Type(
  [in] LONG lnType
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ iadlmail ist als 97af011a-478e-11d1-a3b4-00c04tb950 DC definiert.<br/>            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IADsEmail**](/windows/desktop/api/Iads/nn-iads-iadsemail)
</dt> <dt>

[**Werbung \_ per e-Mail**](/windows/win32/api/iads/ns-iads-ads_email)
</dt> </dl>

 

 





