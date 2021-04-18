---
description: Ruft die Zeitdauer in Minuten seit der letzten Aktivität des Benutzers ab.
ms.assetid: 2d1e68ad-6f65-4e64-afbf-505b2c9d3423
title: Getidleminutes-Funktion
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
ms.openlocfilehash: da3064ea96eb8e9835ed1e9d2f564bf922d2f091
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371053"
---
# <a name="getidleminutes-function"></a>Getidleminutes-Funktion

\[Diese Funktion wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen die **getlastinputinfo** -Funktion.\]

Ruft die Zeitdauer in Minuten seit der letzten Aktivität des Benutzers ab.

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

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen. Diese Funktion wird nicht nach dem Namen exportiert. Geben Sie beim Aufruf von **GetProcAddress** die Ordinalzahl 8 an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msidle.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Getlastinputinfo**](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
