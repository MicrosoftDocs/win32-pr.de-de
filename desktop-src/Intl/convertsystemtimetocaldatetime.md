---
description: Veraltet. Konvertiert eine angegebene SYSTEMTIME-Struktur in eine caldatetime-Struktur.
ms.assetid: d21f75bc-1a93-4cb9-8b9b-6fa0e81886bf
title: Convertsystemtimeumcaldatetime-Funktion
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
ms.openlocfilehash: 738899c7307797f0edeade93f7e4e706919be900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106367975"
---
# <a name="convertsystemtimetocaldatetime-function"></a>Convertsystemtimeumcaldatetime-Funktion

Veraltet. Konvertiert eine angegebene [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) -Struktur in eine [**caldatetime**](caldatetime.md) -Struktur.

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

*lpsystime* \[ in\]
</dt> <dd>

Zeiger auf die zu konvertierende [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) -Struktur.

</dd> <dt>

*Calid* \[ in\]
</dt> <dd>

Der für die Konvertierung zu verwendende System [Kalender Bezeichner](calendar-identifiers.md) .

</dd> <dt>

*lpcaldatetime* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die entsprechende [**caldatetime**](caldatetime.md) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** . Um erweiterte Fehlerinformationen abzurufen, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, die einen der folgenden Fehlercodes zurückgeben kann:

-   Fehler \_ : Ungültiger \_ Parameter. Jeder Parameterwert war ungültig.

## <a name="remarks"></a>Bemerkungen

Das früheste von dieser Funktion unterstützte Datum ist der 1. Januar 1601.

Diese Funktion verfügt über keine zugeordnete Header Datei oder Bibliotheksdatei. Die Anwendung kann [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) mit dem DLL-Namen (Kernel32.dll) aufzurufen, um ein Modul Handle zu erhalten. Anschließend kann [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) mit dem Modul Handle und dem Namen dieser Funktion aufgerufen werden, um die Funktions Adresse abzurufen.

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
</dt> <dt>

[Abrufen von Zeit-und Datumsinformationen](time-and-date.md)
</dt> </dl>

 

 
