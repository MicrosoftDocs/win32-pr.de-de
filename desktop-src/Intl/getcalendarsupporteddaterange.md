---
description: Veraltet. Ruft den unterstützten Datumsbereich für einen angegebenen Kalender ab.
ms.assetid: fe036ac5-77c0-4e83-8d70-db3fa0f7c803
title: Getcalendarsupporteddaterange-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCalendarSupportedDateRange
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 57b1175ef7bcf5b6b5d91af63682ca565bc0f1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960165"
---
# <a name="getcalendarsupporteddaterange-function"></a>Getcalendarsupporteddaterange-Funktion

Veraltet. Ruft den unterstützten Datumsbereich für einen angegebenen Kalender ab.

## <a name="syntax"></a>Syntax


```C++
BOOL GetCalendarSupportedDateRange(
  _In_  CALID         Calendar,
  _Out_ LPCALDATETIME lpCalMinDateTime,
  _Out_ LPCALDATETIME lpCalMaxDateTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Kalender* \[ in\]
</dt> <dd>

Der [Kalender Bezeichner](calendar-identifiers.md) , für den der unterstützte Datumsbereich angezeigt werden soll.

</dd> <dt>

*lpcalmindatetime* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine [**caldatetime**](caldatetime.md) -Struktur, die das unterstützte minimal Datum definiert.

</dd> <dt>

*lpcalmaxdatetime* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine [**caldatetime**](caldatetime.md) -Struktur, die das maximal unterstützte Datum definiert.

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

[NLS: Beispiel für namensbasierte APIs](nls--name-based-apis-sample.md)
</dt> </dl>

 

 
