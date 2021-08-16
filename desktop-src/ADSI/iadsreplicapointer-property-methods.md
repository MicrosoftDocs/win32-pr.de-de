---
title: IADsReplicaPointer-Eigenschaftsmethoden (Iads.h)
description: Die -Eigenschaftsmethode der IADsReplicaPointer-Schnittstelle legt die in der folgenden Tabelle beschriebene Eigenschaft fest. Weitere Informationen finden Sie unter Schnittstelleneigenschaftsmethoden.
ms.assetid: fc520ea4-b2c2-44c0-8bec-25f8d4a77074
ms.tgt_platform: multiple
keywords:
- IADsReplicaPointer-Eigenschaftsmethoden ADSI
topic_type:
- apiref
api_name:
- IADsReplicaPointer Property Methods
- IADsReplicaPointer.ServerName
- IADsReplicaPointer.get_ServerName
- IADsReplicaPointer.put_ServerName
- IADsReplicaPointer.ReplicaType
- IADsReplicaPointer.get_ReplicaType
- IADsReplicaPointer.put_ReplicaType
- IADsReplicaPointer.ReplicaNumber
- IADsReplicaPointer.get_ReplicaNumber
- IADsReplicaPointer.put_ReplicaNumber
- IADsReplicaPointer.Count
- IADsReplicaPointer.get_Count
- IADsReplicaPointer.put_Count
- IADsReplicaPointer.ReplicaAddressHints
- IADsReplicaPointer.get_ReplicaAddressHints
- IADsReplicaPointer.put_ReplicaAddressHints
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d4e232edf2fb64ec7e560d34d5a6b5c1a498e03c348e601230ced07a585f6dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839720"
---
# <a name="iadsreplicapointer-property-methods"></a>IADsReplicaPointer-Eigenschaftsmethoden

Die -Eigenschaftsmethode der [**IADsReplicaPointer-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadsreplicapointer) legt die in der folgenden Tabelle beschriebene Eigenschaft fest. Weitere Informationen finden Sie unter [Schnittstelleneigenschaftsmethoden.](interface-property-methods.md)

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**Count**
</dt> <dd> <dl>

Die Anzahl der vorhandenen Replikate.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* retval
);
HRESULT put_Count(
  [in] LONG lnCount
);
```


</dt> </dl> </dd> <dt>

**ReplicaAddressHints**
</dt> <dd> <dl>

Eine Netzwerkadresse, die als wahrscheinlicher Verweis auf einen Knoten vorgeschlagen wird, der zum Namenserver führt.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ReplicaAddressHints(
  [out] VARIANT* retval
);
HRESULT put_ReplicaAddressHints(
  [in] VARIANT vReplicaAddressHints
);
```


</dt> </dl> </dd> <dt>

**ReplicaNumber**
</dt> <dd> <dl>

ID des Replikats.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ReplicaNumber(
  [out] LONG* retval
);
HRESULT put_ReplicaNumber(
  [in] LONG lnReplicaNumber
);
```


</dt> </dl> </dd> <dt>

**ReplicaType**
</dt> <dd> <dl>

Replikattyp (master, sekundär oder schreibgeschützt)

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ReplicaType(
  [out] LONG* retval
);
HRESULT put_ReplicaType(
  [in] LONG lnType
);
```


</dt> </dl> </dd> <dt>

**ServerName**
</dt> <dd> <dl>

Name des Namensservers, der das Replikat enthält.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServerName(
  [out] BSTR* retVal
);
HRESULT put_ServerName(
  [in] BSTR bstrServerName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsReplicaPointer ist als F60FB803-4080-11D1-A3AC-00C04FB950DC definiert.<br/>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IADsReplicaPointer**](/windows/desktop/api/Iads/nn-iads-iadsreplicapointer)
</dt> <dt>

[**ADS \_ REPLICAPOINTER**](/windows/win32/api/iads/ns-iads-ads_replicapointer)
</dt> </dl>

 

 





