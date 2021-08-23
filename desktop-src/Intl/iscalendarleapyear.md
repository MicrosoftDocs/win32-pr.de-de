---
description: Veraltet. Gibt an, ob das angegebene Jahr ein Schaltjahr innerhalb des angegebenen Zeitraumes für den jeweiligen Kalender ist.
ms.assetid: 91f58915-f0c6-4c7a-9d9a-96e255d799fd
title: IsCalendarLeapYear-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsCalendarLeapYear
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: fe89f11bbaf41235449e882626680cf4d4af075d93f76c2d2aacd90d8d38707a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948728"
---
# <a name="iscalendarleapyear-function"></a>IsCalendarLeapYear-Funktion

Veraltet. Gibt an, ob das angegebene Jahr ein Schaltjahr innerhalb des angegebenen Zeitraumes für den jeweiligen Kalender ist.

## <a name="syntax"></a>Syntax


```C++
BOOL IsCalendarLeapYear(
  _In_ CALID calId,
  _In_ UINT  year,
  _In_ UINT  era
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*calId* \[ In\]
</dt> <dd>

Der [Kalenderbezeichner,](calendar-identifiers.md) der zum Überprüfen des Schaltjahrs verwendet werden soll.

</dd> <dt>

*year* \[ In\]
</dt> <dd>

Das zu überprüfende Jahr.

</dd> <dt>

*-Zeit* \[ In\]
</dt> <dd>

Der zu überprüfende Zeitraum.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn das angegebene Jahr ein Schaltjahr ist, andernfalls **FALSE.** Um erweiterte Fehlerinformationen abzurufen, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, wodurch einer der folgenden Fehlercodes zurückgegeben werden kann:

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
</dt> </dl>

 

 
