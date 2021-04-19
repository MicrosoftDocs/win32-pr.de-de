---
title: Iadstypedname-Eigenschafts Methoden (IADs. h)
description: Die-Eigenschaften Methode der iadstypedname-Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: 0097c7c0-91f9-4874-93f2-c24900054a49
ms.tgt_platform: multiple
keywords:
- Iadstypedname-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsTypedName Property Methods
- IADsTypedName.ObjectName
- IADsTypedName.get_ObjectName
- IADsTypedName.put_ObjectName
- IADsTypedName.Level
- IADsTypedName.get_Level
- IADsTypedName.put_Level
- IADsTypedName.Interval
- IADsTypedName.get_Interval
- IADsTypedName.put_Interval
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1a90e3c3950fb3912e2fe206048053bec6322be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339963"
---
# <a name="iadstypedname-property-methods"></a>Iadstypedname-Eigenschaften Methoden

Die-Eigenschaften Methode der [**iadstypedname**](/windows/desktop/api/Iads/nn-iads-iadstypedname) -Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird. Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**Intervall**
</dt> <dd> <dl>

Die Frequenz des Verweises des Objekts.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Interval(
  [out] LONG* retval
);
HRESULT put_Interval(
  [in] LONG lnInterval
);
```


</dt> </dl> </dd> <dt>

**Level**
</dt> <dd> <dl>

Die dem-Objekt zugeordnete Prioritätsstufe.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Level(
  [out] LONG* retval
);
HRESULT put_Level(
  [in] LONG lnLevel
);
```


</dt> </dl> </dd> <dt>

**ObjectName**
</dt> <dd> <dl>

Der Name eines Objekts.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ObjectName(
  [out] BSTR* retVal
);
HRESULT put_ObjectName(
  [in] BSTR bstrObjectName
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
| IID<br/>                      | IID \_ iadstypedname ist als B371A349-4080-11d1-A3AC-00C04FB950DC definiert.<br/>        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IADsTypedName**](/windows/desktop/api/Iads/nn-iads-iadstypedname)
</dt> <dt>

[**ADS \_ typedName**](/windows/win32/api/iads/ns-iads-ads_typedname)
</dt> </dl>

 

 





