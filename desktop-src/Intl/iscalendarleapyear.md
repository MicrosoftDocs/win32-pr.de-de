---
description: Veraltet. Gibt an, ob das angegebene Jahr ein Schaltjahr innerhalb des angegebenen Zeitraums für den jeweiligen Kalender ist.
ms.assetid: 91f58915-f0c6-4c7a-9d9a-96e255d799fd
title: Iscalendarleapyear-Funktion
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
ms.openlocfilehash: 484531f8107bacb70f9e24ba2537090317825e26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865491"
---
# <a name="iscalendarleapyear-function"></a>Iscalendarleapyear-Funktion

Veraltet. Gibt an, ob das angegebene Jahr ein Schaltjahr innerhalb des angegebenen Zeitraums für den jeweiligen Kalender ist.

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

*Calid* \[ in\]
</dt> <dd>

Der für die Überprüfung des Schalt Jahrs zu verwendende [Kalender Bezeichner](calendar-identifiers.md) .

</dd> <dt>

*Jahr* \[ in\]
</dt> <dd>

Das zu überprüfen Jahr.

</dd> <dt>

 Zeitraum \[ in\]
</dt> <dd>

Der Zeitraum, der überprüft werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn das angegebene Jahr ein Schaltjahr ist, andernfalls **false** . Um erweiterte Fehlerinformationen abzurufen, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, die einen der folgenden Fehlercodes zurückgeben kann:

-   Fehler \_ : Ungültiger \_ Parameter. Jeder Parameterwert war ungültig.

## <a name="remarks"></a>Bemerkungen

Diese Funktion verfügt über keine zugeordnete Header Datei oder Bibliotheksdatei. Die Anwendung kann [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) mit dem DLL-Namen (Kernel32.dll) aufzurufen, um ein Modul Handle zu erhalten. Anschließend kann [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) mit diesem Modul Handle und dem Namen dieser Funktion aufgerufen werden, um die Funktions Adresse abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Unterstützung für nationale Sprache](national-language-support.md)
</dt> <dt>

[Funktionen zur Unterstützung der Landessprache](national-language-support-functions.md)
</dt> </dl>

 

 
