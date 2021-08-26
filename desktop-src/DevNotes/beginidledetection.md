---
description: Beginnt mit der Überwachung der Inaktivität.
ms.assetid: fed5e4ae-2c2b-4b00-9230-b71aec9335c8
title: BeginIdleDetection-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BeginIdleDetection
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: 1bbb27114177a6f64f471b0122832bc09180988019bc23a63343920eb76221f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002320"
---
# <a name="beginidledetection-function"></a>BeginIdleDetection-Funktion

\[Diese Funktion wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen die **GetLastInputInfo-Funktion.**\]

Beginnt mit der Überwachung der Inaktivität.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI BeginIdleDetection(
   _IDLECALLBACK pfnCallback,
   DWORD         dwIdleMin,
   DWORD         dwReserved
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfnCallback* 
</dt> <dd>

Die Funktion, die aufgerufen wird, wenn sich der Leerlaufzustand ändert. Dieser Rückruf ist wie folgt definiert:

``` syntax
typedef void (WINAPI* _IDLECALLBACK) (DWORD dwState);

#define STATE_USER_IDLE_BEGIN       1
#define STATE_USER_IDLE_END         2
```

</dd> <dt>

*dwIdleMin* 
</dt> <dd>

Die Anzahl der Minuten der Inaktivität, bevor der Aufruf der Rückruffunktion erfolgt.

</dd> <dt>

*dwReserved* 
</dt> <dd>

Dieser Parameter muss auf 0 (null) festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 zurück, wenn die Funktion erfolgreich ausgeführt wird. Andernfalls wird ein Fehlercode zurückgegeben. Wenn *dwReserved* beispielsweise etwas anderes als 0 ist, wird **ERROR INVALID \_ \_ DATA** zurückgegeben.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen. Diese Funktion wird nicht anhand des Namens exportiert. Geben Sie beim Aufrufen von **GetProcAddress** die Ordnungszahl 3 an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msidle.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**GetLastInputInfo**](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
