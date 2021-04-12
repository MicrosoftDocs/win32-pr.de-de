---
title: Iadsbacklink-Eigenschaften Methoden (IADs. h)
description: Die-Eigenschaften Methode der iadsbacklink-Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: 0a66fa6d-1bf5-4ff0-8bbd-625a69cf9594
ms.tgt_platform: multiple
keywords:
- Iadsbacklink-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsBackLink Property Methods
- IADsBackLink.RemoteID
- IADsBackLink.get_RemoteID
- IADsBackLink.put_RemoteID
- IADsBackLink.ObjectName
- IADsBackLink.get_ObjectName
- IADsBackLink.put_ObjectName
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c2220fff3a18b0822c0167b387ec10c324d95aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105158"
---
# <a name="iadsbacklink-property-methods"></a>Iadsbacklink-Eigenschaften Methoden

Die-Eigenschaften Methode der [**iadsbacklink**](/windows/desktop/api/Iads/nn-iads-iadsbacklink) -Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird. Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**ObjectName**
</dt> <dd> <dl>

Der Name eines Objekts, an das das **Backlinkattribut** angefügt ist.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ObjectName(
  [out] BSTR* retval
);
HRESULT put_ObjectName(
  [in] BSTR bstrSubjectName
);
```


</dt> </dl> </dd> <dt>

**RemoteID**
</dt> <dd> <dl>

Der Bezeichner des Remote Servers, der einen externen Verweis auf das durch **objectName** angegebene Objekt erfordert.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_RemoteID(
  [out] LONG* retVal
);
HRESULT put_RemoteID(
  [in] LONG bstrProtectedAttrName
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
| IID<br/>                      | IID \_ iadsbacklink ist als FD1302BD-4080-11d1-A3AC-00C04FB950DC definiert.<br/>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IADsBackLink**](/windows/desktop/api/Iads/nn-iads-iadsbacklink)
</dt> <dt>

[**anzeigen ( \_ Backlink)**](/windows/win32/api/iads/ns-iads-ads_backlink)
</dt> </dl>

 

 





