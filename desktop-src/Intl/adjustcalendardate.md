---
description: Veraltet. Passt ein Datum an eine angegebene Anzahl von Jahren, Monaten, Wochen oder Tagen an.
ms.assetid: be8d61fd-efa3-4386-969f-30216c282ebc
title: "\"-Funktion\""
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AdjustCalendarDate
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: ce2f61fd7d7d6354130873b5b2b2376c856e3958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345691"
---
# <a name="adjustcalendardate-function"></a>"-Funktion"

Veraltet. Passt ein Datum an eine angegebene Anzahl von Jahren, Monaten, Wochen oder Tagen an.

## <a name="syntax"></a>Syntax


```C++
BOOL AdjustCalendarDate(
  _Inout_ LPCALDATETIME        lpCalDateTime,
  _In_    CALDATETIME_DATEUNIT calUnit,
  _Out_   INT                  amount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpcaldatetime* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine [**caldatetime**](caldatetime.md) -Struktur, die die Datums-und Kalenderinformationen enthält, die angepasst werden sollen.

</dd> <dt>

*calunit* \[ in\]
</dt> <dd>

Der [**\_ dateunit**](caldatetime-dateunit.md) -Enumerationswert caldatetime, der die Datums Einheit angibt, z. b. dayunit.

</dd> <dt>

*Betrag* \[ vorgenommen\]
</dt> <dd>

Der Betrag, um den das angegebene Datum angepasst werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** . Um erweiterte Fehlerinformationen abzurufen, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, die einen der folgenden Fehlercodes zurückgeben kann:

-   das Fehler \_ Datum liegt \_ außerhalb des zulässigen \_ \_ Bereichs. Das angegebene Datum lag außerhalb des gültigen Bereichs.
-   Fehler \_ : Ungültiger \_ Parameter. Jeder Parameterwert war ungültig.

## <a name="remarks"></a>Bemerkungen

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

 

 
