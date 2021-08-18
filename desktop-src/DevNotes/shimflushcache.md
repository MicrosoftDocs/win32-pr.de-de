---
description: Leert den Shim-Datenbankcache. Diese Funktion sollte nach der Installation einer neuen Shim-Datenbank aufgerufen werden.
ms.assetid: 7e5bbdca-7b58-4c51-9cd1-105b05ee7fbe
title: ShimFlushCache-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShimFlushCache
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: ecf1291b7fdcfb43170ec7e269fa140c321fafdbc09989fc7ee2b392f11c1160
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075914"
---
# <a name="shimflushcache-function"></a>ShimFlushCache-Funktion

Leert den Shim-Datenbankcache. Diese Funktion sollte nach der Installation einer neuen Shim-Datenbank aufgerufen werden.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI ShimFlushCache(
  _In_opt_ HWND      hwnd,
  _In_opt_ HINSTANCE hInstance,
  _In_opt_ LPCSTR    lpszCmdLine,
  _In_     int       nCmdShow
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwnd* \[ in, optional\]
</dt> <dd>

Nicht verwendet; muss 0 sein.

</dd> <dt>

*hInstance* \[ in, optional\]
</dt> <dd>

Nicht verwendet; muss 0 sein.

</dd> <dt>

*lpszCmdLine* \[ in, optional\]
</dt> <dd>

Nicht verwendet; muss 0 sein.

</dd> <dt>

*nCmdShow* \[ In\]
</dt> <dd>

Nicht verwendet; muss 0 sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt **TRUE** bei Erfolg oder **FALSE** bei Einem Fehler zurück.

## <a name="remarks"></a>Hinweise

Der Aufrufer muss ein Administrator sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**BaseFlushAppcompatCache**](baseflushappcompatcache.md)
</dt> </dl>

 

 




