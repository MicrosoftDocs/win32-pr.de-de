---
description: Leert den Shim-Daten Bank Cache. Diese Funktion sollte nach der Installation einer neuen Shimdatenbank aufgerufen werden.
ms.assetid: 7e5bbdca-7b58-4c51-9cd1-105b05ee7fbe
title: Shimflushcache-Funktion
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
ms.openlocfilehash: 35e279c5036142ec87c5bad6d7c512388033bc94
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041322"
---
# <a name="shimflushcache-function"></a>Shimflushcache-Funktion

Leert den Shim-Daten Bank Cache. Diese Funktion sollte nach der Installation einer neuen Shimdatenbank aufgerufen werden.

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

*HWND* \[ in, optional\]
</dt> <dd>

Genutzt muss 0 sein.

</dd> <dt>

*HINSTANCE* \[ in, optional\]
</dt> <dd>

Genutzt muss 0 sein.

</dd> <dt>

*lpszCmdLine* \[ in, optional\]
</dt> <dd>

Genutzt muss 0 sein.

</dd> <dt>

*nCmdShow* \[ in\]
</dt> <dd>

Genutzt muss 0 sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei einem Fehler gibt die Funktion **true** oder **false** zurück.

## <a name="remarks"></a>Bemerkungen

Der Aufrufer muss ein Administrator sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Baseflushappcompatcache**](baseflushappcompatcache.md)
</dt> </dl>

 

 




