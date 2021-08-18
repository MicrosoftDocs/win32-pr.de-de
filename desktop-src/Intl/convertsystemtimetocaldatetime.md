---
description: Veraltet. Konvertiert eine angegebene SYSTEMTIME-Struktur in eine CALDATETIME-Struktur.
ms.assetid: d21f75bc-1a93-4cb9-8b9b-6fa0e81886bf
title: ConvertSystemTimeToCalDateTime-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertSystemTimeToCalDateTime
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 01eb78f9045e43db3e97b252a8fdf8fe8ed7297905174efeff2f3b2bbe1a5171
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746040"
---
# <a name="convertsystemtimetocaldatetime-function"></a>ConvertSystemTimeToCalDateTime-Funktion

Veraltet. Konvertiert eine angegebene [**SYSTEMTIME-Struktur**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) in eine [**CALDATETIME-Struktur.**](caldatetime.md)

## <a name="syntax"></a>Syntax


```C++
BOOL ConvertSystemTimeToCalDateTime(
  _In_  const SYSTEMTIME   *lpSysTime,
  _In_        CALID         calId,
  _Out_       LPCALDATETIME lpCalDateTime

);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpSysTime* \[ In\]
</dt> <dd>

Zeiger auf die zu konvertierende [**SYSTEMTIME-Struktur.**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)

</dd> <dt>

*calId* \[ In\]
</dt> <dd>

Der bei der Konvertierung zu [verwendende Systemkalenderbezeichner.](calendar-identifiers.md)

</dd> <dt>

*lpCalDateTime* \[ out\]
</dt> <dd>

Zeiger auf die entsprechende [**CALDATETIME-Struktur.**](caldatetime.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.** Um erweiterte Fehlerinformationen abzurufen, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, wodurch einer der folgenden Fehlercodes zurückgegeben werden kann:

-   FEHLER: \_ UNGÜLTIGER \_ PARAMETER. Jeder der Parameterwerte war ungültig.

## <a name="remarks"></a>Hinweise

Das früheste von dieser Funktion unterstützte Datum ist der 1. Januar 1601.

Dieser Funktion ist keine Header- oder Bibliotheksdatei zugeordnet. Die Anwendung kann [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) mit dem DLL-Namen (Kernel32.dll) aufrufen, um ein Modulhandle abzurufen. Anschließend kann [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) mit dem Modulhandle und dem Namen dieser Funktion aufgerufen werden, um die Funktionsadresse abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Unterstützung für nationale Sprachen](national-language-support.md)
</dt> <dt>

[Unterstützungsfunktionen für nationale Sprachen](national-language-support-functions.md)
</dt> <dt>

[Abrufen von Uhrzeit- und Datumsinformationen](time-and-date.md)
</dt> </dl>

 

 
