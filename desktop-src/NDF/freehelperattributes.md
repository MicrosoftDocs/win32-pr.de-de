---
title: FreeHelperAttributes-Funktion (Ndattributils.h)
description: Gibt den intern zugeordneten Arbeitsspeicher einem Array von HELPER \_ ATTRIBUTE-Strukturen zu.
ms.assetid: d973bdb9-c1d1-4cea-bcc6-98671349413f
keywords:
- FreeHelperAttributes-Funktion NDF
topic_type:
- apiref
api_name:
- FreeHelperAttributes
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb16ad2d7f505a90d806e3f6a155f2c20affce2c71267316c2278e2320c371b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802430"
---
# <a name="freehelperattributes-function"></a>FreeHelperAttributes-Funktion

Die **FreeHelperAttributes-Funktion** gibt den intern zugeordneten Arbeitsspeicher einem Array von [**HELPER \_ ATTRIBUTE-Strukturen**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) frei. Diese Funktion ruft [**CoTaskMemFree auf,**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) um die Speicherverteilung frei zu machen.

## <a name="syntax"></a>Syntax


```C++
VOID FreeHelperAttributes(
  _In_ HELPER_ATTRIBUTE *pInfo,
       ULONG            HelperAttributeCount,
       BOOL             bFreePointer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pInfo* \[ In\]
</dt> <dd>

Typ: **[ **HILFSATTRIBUT \_**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)\***

Das Array von -Strukturen. Der zugeordnete Arbeitsspeicher, auf den diese Strukturen zeigt, wird frei.

</dd> <dt>

*HelperAttributeCount* 
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

[**\_HILFSATTRIBUT**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

