---
description: Startet die Überwachung der Inaktivität.
ms.assetid: fed5e4ae-2c2b-4b00-9230-b71aec9335c8
title: Beginidleerkennungs-Funktion
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
ms.openlocfilehash: 06cd016dc4102ef2f5b0f351aa4836a7f9980645
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361336"
---
# <a name="beginidledetection-function"></a>Beginidleerkennungs-Funktion

\[Diese Funktion wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen die **getlastinputinfo** -Funktion.\]

Startet die Überwachung der Inaktivität.

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

*pfncallback* 
</dt> <dd>

Die Funktion, die aufgerufen wird, wenn sich der Leerlaufzustand ändert. Dieser Rückruf wird wie folgt definiert:

``` syntax
typedef void (WINAPI* _IDLECALLBACK) (DWORD dwState);

#define STATE_USER_IDLE_BEGIN       1
#define STATE_USER_IDLE_END         2
```

</dd> <dt>

*dwidlemin* 
</dt> <dd>

Die Anzahl der Minuten der Inaktivität, bevor der Rückruf an die Rückruffunktion erfolgt.

</dd> <dt>

*dwReserved* 
</dt> <dd>

Dieser Parameter muss auf 0 (null) festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 zurück, wenn die Funktion erfolgreich ausgeführt wird. Andernfalls wird ein Fehlercode zurückgegeben. Wenn *dwReserved* beispielsweise etwas anderes als 0 ist, werden **\_ ungültige \_ Daten** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen. Diese Funktion wird nicht nach dem Namen exportiert. Geben Sie beim Aufrufen von " **GetProcAddress**" Ordnungszahl 3 an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msidle.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Getlastinputinfo**](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
