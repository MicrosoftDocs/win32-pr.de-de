---
description: Leert den Anwendungskompatibilitäts-Cache.
ms.assetid: 03f47813-87f6-4b71-b453-77a2facab019
title: Baseflushappcompatcache-Funktion
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
ms.openlocfilehash: 6118c78784bb96b9f25e008cd2221112eeb646f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126212"
---
# <a name="baseflushappcompatcache-function"></a>Baseflushappcompatcache-Funktion

Leert den Anwendungskompatibilitäts-Cache.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI BaseFlushAppcompatCache(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt **true** zurück, wenn Sie erfolgreich ist, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Der Aufrufer muss ein Administrator sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Shimflushcache**](shimflushcache.md)
</dt> </dl>

 

 




