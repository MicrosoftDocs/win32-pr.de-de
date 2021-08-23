---
description: Veraltet. Passt ein Datum um eine angegebene Anzahl von Jahren, Monaten, Wochen oder Tagen an.
ms.assetid: be8d61fd-efa3-4386-969f-30216c282ebc
title: AdjustCalendarDate-Funktion
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
ms.openlocfilehash: 061d0e246f7839345b0f1e55221d26d276f52af4997a7cb47d62b680d2638fb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520620"
---
# <a name="adjustcalendardate-function"></a>AdjustCalendarDate-Funktion

Veraltet. Passt ein Datum um eine angegebene Anzahl von Jahren, Monaten, Wochen oder Tagen an.

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

*lpCalDateTime* \[ in, out\]
</dt> <dd>

Zeiger auf eine [**CALDATETIME-Struktur,**](caldatetime.md) die die anzupassenden Datums- und Kalenderinformationen enthält.

</dd> <dt>

*calUnit* \[ In\]
</dt> <dd>

Der [**CALDATETIME \_ DATEUNIT-Enumerationswert,**](caldatetime-dateunit.md) der die Datumseinheit angibt, z. B. DayUnit.

</dd> <dt>

*amount* \[ out\]
</dt> <dd>

Der Betrag, um den das angegebene Datum angepasst werden soll.

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

[NLS: Beispiel für namensbasierte APIs](nls--name-based-apis-sample.md)
</dt> </dl>

 

 
