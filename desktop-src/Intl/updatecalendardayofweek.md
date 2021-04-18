---
description: Veraltet. Ruft den Wochentag ab, der einem angegebenen Tag entspricht, und füllt den DayOfWeek-Member in der angegebenen caldatetime-Struktur mit diesem Wert auf.
ms.assetid: b9ae250a-73bb-4ec2-bb0d-e1f8b25c173c
title: Updatecalendardayosweek-Funktion
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
ms.openlocfilehash: 316af539e6ca0476f0f8d575a160fcd7c3219e90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354852"
---
# <a name="updatecalendardayofweek-function"></a>Updatecalendardayosweek-Funktion

Veraltet. Ruft den Wochentag ab, der einem angegebenen Tag entspricht, und füllt den **DayOfWeek** -Member in der angegebenen [**caldatetime**](caldatetime.md) -Struktur mit diesem Wert auf.

## <a name="syntax"></a>Syntax


```C++
BOOL UpdateCalendarDayOfWeek(
  _Inout_ LPCALDATETIME lpCalDateTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpcaldatetime* \[ in, out\]
</dt> <dd>

Ein Zeiger auf die [**caldatetime**](caldatetime.md) -Struktur, die das Datum enthält, für das der Wochentag festgelegt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** . Um erweiterte Fehlerinformationen abzurufen, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, die einen der folgenden Fehlercodes zurückgeben kann:

-   das Fehler \_ Datum liegt \_ außerhalb des zulässigen \_ \_ Bereichs. Das angegebene Datum lag außerhalb des gültigen Bereichs.
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
</dt> <dt>

[**Caldatetime**](caldatetime.md)
</dt> </dl>

 

 
