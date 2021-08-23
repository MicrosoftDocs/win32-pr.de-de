---
description: Veraltet. Konvertiert eine angegebene CALDATETIME-Struktur in eine SYSTEMTIME-Struktur.
ms.assetid: 0c3f602d-62de-4c27-95d9-d35738f3279d
title: ConvertCalDateTimeToSystemTime-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertCalDateTimeToSystemTime
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: cb579eb80c421d6f206045889edfe3f1b64130f58d02d96c61b3867abcaabb75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631930"
---
# <a name="convertcaldatetimetosystemtime-function"></a>ConvertCalDateTimeToSystemTime-Funktion

Veraltet. Konvertiert eine angegebene [**CALDATETIME-Struktur**](caldatetime.md) in eine [**SYSTEMTIME-Struktur.**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)

## <a name="syntax"></a>Syntax


```C++
BOOL ConvertCalDateTimeToSystemTime(
  _In_  const LPCALDATETIME lpCalDateTime,
  _Out_       SYSTEMTIME    *lpSysTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpCalDateTime* \[ In\]
</dt> <dd>

Zeiger auf die [**zu konvertierende CALDATETIME-Struktur.**](caldatetime.md)

</dd> <dt>

*lpSysTime* \[ out\]
</dt> <dd>

Zeiger auf die entsprechende [**SYSTEMTIME-Struktur.**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, **andernfalls FALSE.** Um erweiterte Fehlerinformationen zu erhalten, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, wodurch einer der folgenden Fehlercodes zurückgegeben werden kann:

-   FEHLERDATUM \_ \_ LIEGT NICHT IM \_ \_ BEREICH. Das angegebene Datum lag nicht im Bereich.
-   FEHLER \_ \_ UNGÜLTIGER PARAMETER. Jeder der Parameterwerte war ungültig.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Headerdatei oder Bibliotheksdatei zugeordnet. Die Anwendung kann [**LoadLibrary mit**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) dem DLL-Namen (Kernel32.dll) aufrufen, um ein Modulhand handle zu erhalten. Sie kann dann [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) mit dem Modulhandle und dem Namen dieser Funktion aufrufen, um die Funktionsadresse zu erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Unterstützung der Landessprache](national-language-support.md)
</dt> <dt>

[Unterstützungsfunktionen für nationale Sprachen](national-language-support-functions.md)
</dt> <dt>

[Abrufen von Zeit- und Datumsinformationen](time-and-date.md)
</dt> </dl>

 

 
