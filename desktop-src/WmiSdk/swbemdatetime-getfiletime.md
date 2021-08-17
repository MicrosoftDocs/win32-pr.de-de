---
description: Konvertiert einen Datums- und Uhrzeitwert im CIM DATETIME-Format in das FILETIME-Format.
ms.assetid: 08e0761d-e735-454a-8429-2bd1eb331123
ms.tgt_platform: multiple
title: SWbemDateTime.GetFileTime-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.GetFileTime
- ISWbemDateTime.GetFileTime
- ISWbemDateTime.GetFileTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8c35daf5b6e986b2519f127969edc5bbcf05a260bd23e8aa1168b1a7c20a5372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739437"
---
# <a name="swbemdatetimegetfiletime-method"></a>SWbemDateTime.GetFileTime-Methode

Die **GetFileTime-Methode** des [**SWbemDateTime-Objekts**](swbemdatetime.md) konvertiert einen Datums- und Uhrzeitwert im CIM [DATETIME-Format](datetime.md) in das FILETIME-Format.

Wenn der Parameter auf **TRUE festgelegt ist,** stellt der Rückgabewert eine lokale Zeit für den Client dar. Andernfalls ist der Rückgabewert eine koordinierte Weltzeit (UTC)-Zeit. Eine **FILETIME** [DATETIME-Struktur](datetime.md) ist ein 64-Bit-Wert, der die Anzahl der Einheiten von 100 Nanosekunden seit dem 1. Januar 1601 darstellt. Windows Die Verwaltungsinstrumentation (WMI) behandelt **FILETIME-Werte** als Zeichenfolgendarstellungen von 64-Bit-Zahlen ohne Vorzeichen.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
vDate = .GetFileTime( _
  [ ByVal bIsLocaL ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bIsLocaL* \[ in, optional\]
</dt> <dd>

Gibt an, ob der zurückgegebene Wert als Ortszeit interpretiert wird. Die UTC-Eigenschaft enthält dann die Ortszeit, die in den richtigen UTC-Offset (Coordinated Universal Times) konvertiert wird. Wenn der Wert **FALSE ist,** wird der Wert als UTC mit einem Nulloffset (0) interpretiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Das Datum und die Uhrzeit im **FILETIME-Format.**

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **GetFileTime-Methode** enthält das [Err-Objekt](/previous-versions//sbf5ze0e(v=vs.85)) möglicherweise den Fehlercode in der folgenden Liste.

<dl> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Der Aufruf schlug fehl.

</dd> </dl>

## <a name="remarks"></a>Hinweise

**VT \_ DATE-** **und FILETIME-Werte** dürfen keine Platzhalterfelder enthalten.

Die **GetFileTime-Methode** schlägt fehl (wbemErrFailed), wenn eine der folgenden Eigenschaften **FALSE ist:**

-   [**YearSpecified**](swbemdatetime-yearspecified.md)
-   [**MonthSpecified**](swbemdatetime-monthspecified.md)
-   [**DaySpecified**](swbemdatetime-dayspecified.md)
-   [**HoursSpecified**](swbemdatetime-hoursspecified.md)
-   [**MinutesSpecified**](swbemdatetime-minutesspecified.md)
-   [**SecondsSpecified**](swbemdatetime-secondsspecified.md)
-   [**MicrosecondsSpecified**](swbemdatetime-microsecondsspecified.md)
-   [**UTCSpecified**](swbemdatetime-utcspecified.md)

Bei einer erfolgreichen Rückgabe [**von SetFileTime**](swbemdatetime-setfiletime.md)werden alle diese Eigenschaften auf **TRUE festgelegt.**

## <a name="examples"></a>Beispiele

Beispiele für die Verwendung des [**SWbemDateTime-Objekts**](swbemdatetime.md) zum Konvertieren von CIM [**DATETIME-Werten**](datetime.md) in und aus dem **FILETIME-Format** oder dem **VT \_ DATE-Format** finden Sie unter [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md). Eine Beschreibung des CIM **DATETIME-Formats** finden Sie unter [Datums- und Uhrzeitformat.](date-and-time-format.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemDateTime<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemDateTime<br/>                                                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SWbemDateTime.GetVarDate**](swbemdatetime-getvardate.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**Datetime**](datetime.md)
</dt> </dl>

 

