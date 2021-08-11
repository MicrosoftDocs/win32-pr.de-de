---
title: IADsHold-Eigenschaftsmethoden (Iads.h)
description: Die -Eigenschaftsmethode der IADsHold-Schnittstelle legt die in der folgenden Tabelle beschriebene Eigenschaft fest. Weitere Informationen finden Sie unter Schnittstelleneigenschaftenmethoden.
ms.assetid: 55968bc1-c44a-4db4-acc8-e1b6f1e4ad4c
ms.tgt_platform: multiple
keywords:
- IADsHold-Eigenschaftsmethoden ADSI
topic_type:
- apiref
api_name:
- IADsHold Property Methods
- IADsHold.ObjectName
- IADsHold.get_ObjectName
- IADsHold.put_ObjectName
- IADsHold.Amount
- IADsHold.get_Amount
- IADsHold.put_Amount
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fae4d5f5a83577d297bfea6e109d78ad3d8bd2291cfa028f37fb8ab1a4f825b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179558"
---
# <a name="iadshold-property-methods"></a>IADsHold-Eigenschaftsmethoden

Die -Eigenschaftsmethode der [**IADsHold-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadshold) legt die in der folgenden Tabelle beschriebene Eigenschaft fest. Weitere Informationen finden Sie unter [Schnittstelleneigenschaftsmethoden.](interface-property-methods.md)

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**Amount (Betrag)**
</dt> <dd> <dl>

Die Höhe der Gebühren für den Zeitraum, in dem der Benutzer zurückgehalten wird, während der Server den Kontostand des Benutzers überprüft.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Amount(
  [out] LONG* retval
);
HRESULT put_Amount(
  [in] LONG lnAmount
);
```


</dt> </dl> </dd> <dt>

**ObjectName**
</dt> <dd> <dl>

Der Name des Objekts, das einen zurückgehaltenen Benutzer darstellt.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **BSTR**
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
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsHold ist als B3EB3B37-4080-11D1-A3AC-00C04FB950DC definiert.<br/>             |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IADsHold**](/windows/desktop/api/Iads/nn-iads-iadshold)
</dt> </dl>

 

 





