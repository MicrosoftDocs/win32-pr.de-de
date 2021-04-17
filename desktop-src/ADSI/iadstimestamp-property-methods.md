---
title: Iadstimestamp-Eigenschaften Methoden (IADs. h)
description: Die Property-Methode der iadstimestamp-Schnittstelle legt die in der folgenden Tabelle beschriebene Eigenschaft fest. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: 0f00d270-3c11-4c60-95b3-178130e31caa
ms.tgt_platform: multiple
keywords:
- Iadstimestamp-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsTimestamp Property Methods
- IADsTimestamp.WholeSeconds
- IADsTimestamp.get_WholeSeconds
- IADsTimestamp.put_WholeSeconds
- IADsTimestamp.EventID
- IADsTimestamp.get_EventID
- IADsTimestamp.put_EventID
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77db7a6a3b3814cd10beca5da5e3166ab1b61a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476347"
---
# <a name="iadstimestamp-property-methods"></a>Iadstimestamp-Eigenschaften Methoden

Die Property-Methode der [**iadstimestamp**](/windows/desktop/api/Iads/nn-iads-iadstimestamp) -Schnittstelle legt die in der folgenden Tabelle beschriebene Eigenschaft fest. Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**EventID**
</dt> <dd> <dl>

Ein Ereignisbezeichner.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_EventID(
  [out] LONG* retval
);
HRESULT put_EventID(
  [in] LONG lnEventID
);
```


</dt> </dl> </dd> <dt>

**Großhandels-econds**
</dt> <dd> <dl>

Anzahl von Sekunden, wobei der Wert 0 (null) 12:00 Uhr, Januar 1970, UTC ist.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_WholeSeconds(
  [out] LONG* retVal
);
HRESULT put_WholeSeconds(
  [in] LONG lnWholeSeconds
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
| IID<br/>                      | IID \_ iadstimestamp ist als B2F5A901-4080-11d1-A3AC-00C04FB950DC definiert.<br/>        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IADsTimestamp**](/windows/desktop/api/Iads/nn-iads-iadstimestamp)
</dt> <dt>

[**Werbe \_ Zeitstempel**](/windows/win32/api/iads/ns-iads-ads_timestamp)
</dt> </dl>

 

 





