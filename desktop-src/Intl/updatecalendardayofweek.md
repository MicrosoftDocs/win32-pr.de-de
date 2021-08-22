---
description: Veraltet. Ruft den Wochentag ab, der einem angegebenen Tag entspricht, und füllt das DayOfWeek-Element in der angegebenen CALDATETIME-Struktur mit diesem Wert auf.
ms.assetid: b9ae250a-73bb-4ec2-bb0d-e1f8b25c173c
title: UpdateCalendarDayOfWeek-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateCalendarDayOfWeek
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 0e7060c03b06fe855c096e94469797dedb20d74ec1d9de43e11b866c3afb0ed3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119560650"
---
# <a name="updatecalendardayofweek-function"></a>UpdateCalendarDayOfWeek-Funktion

Veraltet. Ruft den Wochentag ab, der einem angegebenen Tag entspricht, und füllt das **DayOfWeek-Element** in der angegebenen [**CALDATETIME-Struktur**](caldatetime.md) mit diesem Wert auf.

## <a name="syntax"></a>Syntax


```C++
BOOL UpdateCalendarDayOfWeek(
  _Inout_ LPCALDATETIME lpCalDateTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpCalDateTime* \[ in, out\]
</dt> <dd>

Zeiger auf die [**CALDATETIME-Struktur,**](caldatetime.md) die das Datum enthält, für das der Wochentag festgelegt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.** Um erweiterte Fehlerinformationen abzurufen, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, wodurch einer der folgenden Fehlercodes zurückgegeben werden kann:

-   FEHLERDATUM \_ \_ LIEGT AUßERHALB DES \_ \_ BEREICHS. Das angegebene Datum lag außerhalb des Bereichs.
-   FEHLER: \_ UNGÜLTIGER \_ PARAMETER. Jeder der Parameterwerte war ungültig.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Header- oder Bibliotheksdatei zugeordnet. Die Anwendung kann [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) mit dem DLL-Namen (Kernel32.dll) aufrufen, um ein Modulhandle abzurufen. Anschließend kann [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) mit diesem Modulhandle und dem Namen dieser Funktion aufgerufen werden, um die Funktionsadresse abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Unterstützung für nationale Sprachen](national-language-support.md)
</dt> <dt>

[Unterstützungsfunktionen für nationale Sprachen](national-language-support-functions.md)
</dt> <dt>

[**CALDATETIME**](caldatetime.md)
</dt> </dl>

 

 
