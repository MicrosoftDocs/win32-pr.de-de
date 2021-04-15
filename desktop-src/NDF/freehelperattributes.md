---
title: Freehelperattributfunktion (ndattributils. h)
description: Hebt die Zuordnung des intern zugeordneten Arbeitsspeichers zu einem Array von \_ hilfsattribut Strukturen auf.
ms.assetid: d973bdb9-c1d1-4cea-bcc6-98671349413f
keywords:
- Freehelperattributs-Funktion NDF
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
ms.openlocfilehash: 400addd7d32914cb4e849e4e0bfae76ccc3ddf22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475987"
---
# <a name="freehelperattributes-function"></a>Freehelperattributs-Funktion

Die **freehelperattributfunktion** hebt die Zuordnung des intern zugeordneten Arbeitsspeichers zu einem Array von [**\_ hilfsattribut**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) Strukturen auf. Diese Funktion ruft [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) auf, um den Speicherplatz freizugeben.

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

*pinfo* \[ in\]
</dt> <dd>

Type: **[**helper- \_ Attribut**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) \** _

Das Array von-Strukturen. Der zugewiesene Speicher, auf den diese Strukturen zeigen, wird freigegeben.

</dd> <dt>

_HelperAttributeCount * 
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

[**HELPER- \_ Attribut**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

