---
description: Leert den Anwendungskompatibilitätscache.
ms.assetid: 03f47813-87f6-4b71-b453-77a2facab019
title: BaseFlushAppcompatCache-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BaseFlushAppcompatCache
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-appcompat-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-appcompat-l1-1-1.dll
ms.openlocfilehash: 44ea71a28ff85b00c72dc7b0255144381a2d8f01ead0901ee30ff216e17e20d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768750"
---
# <a name="baseflushappcompatcache-function"></a>BaseFlushAppcompatCache-Funktion

Leert den Anwendungskompatibilitätscache.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI BaseFlushAppcompatCache(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt **TRUE zurück,** wenn sie erfolgreich ist, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Der Aufrufer muss administrator sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ShimFlushCache**](shimflushcache.md)
</dt> </dl>

 

 




