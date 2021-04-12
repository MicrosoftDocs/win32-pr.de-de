---
title: Freerepirren infoexs-Funktion (ndattributils. h)
description: Hebt die Zuordnung des intern zugeordneten Arbeitsspeichers zu einem Array von repairiinfoex-Strukturen auf.
ms.assetid: b4e3e758-88cd-4ce2-b1a4-5b47889aae9b
keywords:
- Freerepirren infoexs-Funktion NDF
topic_type:
- apiref
api_name:
- FreeRepairInfoExs
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 094c745486526caa870a500019de3aa819b6fe5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517927"
---
# <a name="freerepairinfoexs-function"></a>Freerepirren infoexs-Funktion

Die **freerepirren infoexs** -Funktion hebt die Zuordnung des intern zugeordneten Arbeitsspeichers zu einem Array der [**repauninfoex**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex) -Strukturen auf. Diese Funktion ruft [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) auf, um den Speicherplatz freizugeben.

## <a name="syntax"></a>Syntax


```C++
VOID FreeRepairInfoExs(
  _In_ RepairInfoEx *pInfo,
       ULONG        RepairCount,
       BOOL         bFreePointer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pinfo* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: **[**repairren INFOEX**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex) \** _

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

[**Repairren INFOEX**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

