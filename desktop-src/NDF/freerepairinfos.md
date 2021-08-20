---
title: FreeRepairInfos-Funktion (Ndattributils.h)
description: Hebt die Zuordnung des intern zugeordneten Arbeitsspeichers zu einem Array von RepairInfo-Strukturen auf.
ms.assetid: c40f9d10-8d9e-4c79-ac0b-fa88608888f1
keywords:
- FreeRepairInfos-Funktion NDF
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
ms.openlocfilehash: 745f6cd9a7fd484db943fc91c5c9dadf440b3635f31cdb539b356358c22362a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798605"
---
# <a name="freerepairinfos-function"></a>FreeRepairInfos-Funktion

Die **FreeRepairInfos-Funktion** hebt die Zuordnung des intern zugewiesenen Arbeitsspeichers zu einem Array von [**RepairInfo-Strukturen**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) auf. Diese Funktion ruft [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) auf, um die Zuordnung des Arbeitsspeichers freizugeben.

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

*pInfo* \[ In\]
</dt> <dd>

Typ: **[ **RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)\***

Das Array von -Strukturen. Der zugeordnete Arbeitsspeicher, auf den diese Strukturen verweisen, wird freigegeben.

</dd> <dt>

*RepairCount* 
</dt> <dd>

Typ: **ULONG**

Die Anzahl der Strukturen im Array, auf die *pInfo* zeigt.

</dd> <dt>

*bFreePointer* 
</dt> <dd>

Typ: **BOOL**

True, wenn auch das Array von Strukturen gelöscht werden soll. andernfalls FALSE.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Ndattributils.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

