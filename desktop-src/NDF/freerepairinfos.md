---
title: Freerepirren Infos-Funktion (ndattributils. h)
description: Hebt die Zuordnung des intern zugeordneten Arbeitsspeichers zu einem Array von repairren Info-Strukturen auf.
ms.assetid: c40f9d10-8d9e-4c79-ac0b-fa88608888f1
keywords:
- Freerepaarinfos-Funktion NDF
topic_type:
- apiref
api_name:
- FreeRepairInfos
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63bf6ab2154376302e4c9dd076ccaf83a0c565c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103287"
---
# <a name="freerepairinfos-function"></a>Freerepirren Infos-Funktion

Die **freerepirren Infos** -Funktion hebt die Zuordnung des intern zugeordneten Arbeitsspeichers zu einem Array von [**repauninfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) -Strukturen auf. Diese Funktion ruft [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) auf, um den Speicherplatz freizugeben.

## <a name="syntax"></a>Syntax


```C++
VOID FreeRepairInfos(
  _In_ RepairInfo *pInfo,
       ULONG      RepairCount,
       BOOL       bFreePointer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pinfo* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: **[**repairren Info**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _

Das Array von-Strukturen. Der zugewiesene Speicher, auf den diese Strukturen zeigen, wird freigegeben.

</dd> <dt>

_RepairCount * 
</dt> <dd>

Typ: **ulong**

Die Anzahl der Strukturen im Array, auf die von *pinfo* verwiesen wird.

</dd> <dt>

*bfrepointer* 
</dt> <dd>

Typ: **bool**

True, wenn das Array von-Strukturen ebenfalls gelöscht werden soll. andernfalls false.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Ndattributils. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Repairren Info**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

