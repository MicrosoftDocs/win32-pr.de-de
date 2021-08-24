---
title: FreeRepairInfoExs-Funktion (Ndattributils.h)
description: Gibt den intern zugeordneten Arbeitsspeicher einem Array von RepairInfoEx-Strukturen zu.
ms.assetid: b4e3e758-88cd-4ce2-b1a4-5b47889aae9b
keywords:
- FreeRepairInfoExs-Funktion NDF
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
ms.openlocfilehash: b75d3d3ee8ba710b0b0ed4755e5ee01309f955bcc1658145dc1d42fe3b9e1ed8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802420"
---
# <a name="freerepairinfoexs-function"></a>FreeRepairInfoExs-Funktion

Die **FreeRepairInfoExs-Funktion** gibt den intern zugeordneten Arbeitsspeicher einem Array von [**RepairInfoEx-Strukturen**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex) frei. Diese Funktion ruft [**CoTaskMemFree auf,**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) um die Speicherverteilung frei zu machen.

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

*pInfo* \[ In\]
</dt> <dd>

Typ: **[ **RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex)\***

Das Array von -Strukturen. Der zugeordnete Arbeitsspeicher, auf den diese Strukturen zeigt, wird frei.

</dd> <dt>

*RepairCount* 
</dt> <dd>

Typ: **ULONG**

Die Anzahl der Strukturen im Array, auf die *pInfo zeigt.*

</dd> <dt>

*bFreePointer* 
</dt> <dd>

Typ: **BOOL**

TRUE, wenn das Array von Strukturen ebenfalls gelöscht werden soll; andernfalls FALSE.

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

[**RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

