---
description: Ruft die Zeitspanne in Minuten seit der letzten Aktivität des Benutzers ab.
ms.assetid: 2d1e68ad-6f65-4e64-afbf-505b2c9d3423
title: GetIdleMinutes-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetIdleMinutes
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: d3397de5d792181958891eef9693d29b2d7d4e56f9bbc7f7e1cfef19171625b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118404583"
---
# <a name="getidleminutes-function"></a>GetIdleMinutes-Funktion

\[Diese Funktion wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen die **GetLastInputInfo-Funktion.**\]

Ruft die Zeitspanne in Minuten seit der letzten Aktivität des Benutzers ab.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI GetIdleMinutes(
   DWORD dwReserved
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwReserved* 
</dt> <dd>

Dieser Parameter muss auf 0 (null) festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl von Minuten seit der letzten Aktivität des Benutzers zurück.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen. Diese Funktion wird nicht anhand des Namens exportiert. Geben Sie beim Aufrufen von **GetProcAddress** die Ordnungszahl 8 an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msidle.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**GetLastInputInfo**](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
