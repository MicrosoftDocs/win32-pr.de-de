---
title: FreeRootCauseInfos-Funktion (Ndattributils.h)
description: Gibt den intern zugeordneten Arbeitsspeicher einem Array von RootCauseInfo-Strukturen zu.
ms.assetid: b45fa432-0db4-470b-80ce-ae25c33f88d6
keywords:
- FreeRootCauseInfos-Funktion NDF
topic_type:
- apiref
api_name:
- FreeRootCauseInfos
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9cbd0386af86ebe5e1fdc5e6350cebfb305f44544f8822e0f2bde4d46cb55f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065240"
---
# <a name="freerootcauseinfos-function"></a>FreeRootCauseInfos-Funktion

Die **FreeRootCauseInfos-Funktion** gibt den intern zugeordneten Arbeitsspeicher einem Array von [**RootCauseInfo-Strukturen**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) frei. Diese Funktion ruft [**CoTaskMemFree auf,**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) um die Speicherverteilung frei zu machen.

## <a name="syntax"></a>Syntax


```C++
VOID FreeRootCauseInfos(
  _In_ RootCauseInfo *pInfo,
       ULONG         RootCauseCount,
       BOOL          bFreePointer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pInfo* \[ In\]
</dt> <dd>

Typ: **[ **RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)\***

Das Array von -Strukturen. Der zugeordnete Arbeitsspeicher, auf den diese Strukturen zeigt, wird frei.

</dd> <dt>

*RootCauseCount* 
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

[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

