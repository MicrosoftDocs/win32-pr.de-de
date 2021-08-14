---
description: Konvertiert einen Datums- und Uhrzeitwert im CIM DATETIME-Format in das VT \_ DATE-Format.
ms.assetid: e63e7acc-89d4-458a-a1ab-4d4a65cf7f8b
ms.tgt_platform: multiple
title: SWbemDateTime.GetVarDate-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.GetVarDate
- ISWbemDateTime.GetVarDate
- ISWbemDateTime.GetVarDate
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 506c897da130b9558b37637918674a7c6024adb787ac3d91e53e430a6edfcd1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314755"
---
# <a name="swbemdatetimegetvardate-method"></a>SWbemDateTime.GetVarDate-Methode

Die **GetVarDate-Methode** des [**SWbemDateTime-Objekts**](swbemdatetime.md) konvertiert einen Datums- und Uhrzeitwert im CIM [**DATETIME-Format**](datetime.md) in das **VT \_ DATE-Format.**

Das **VT \_ DATE-Format** ist eine Automatisierungsvariante des [**DATETIME-Werts,**](datetime.md) Visual Basic und ActiveX wird.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
vdate = .GetVarDate( _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bIsLocal* \[ in, optional\]
</dt> <dd>

Gibt an, ob der zurückgegebene Wert als Ortszeit interpretiert wird. Die koordinierte Weltzeit (UTC) enthält die lokale Zeit, die in den richtigen UTC-Offset konvertiert wurde. Wenn der Wert **FALSE ist,** wird der Wert als UTC mit einem Nulloffset (0) interpretiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Datums- und Uhrzeitwert im **VT \_ DATE-Format.**

## <a name="remarks"></a>Hinweise

**VT \_ DATE-** **und FILETIME-Werte** dürfen keine Platzhalterfelder enthalten.

Die **GetVarDate-Methode** schlägt fehl (**wbemErrFailed**), wenn eine der folgenden Eigenschaften **FALSE ist:**

-   [**YearSpecified**](swbemdatetime-yearspecified.md)
-   [**MonthSpecified**](swbemdatetime-monthspecified.md)
-   [**DaySpecified**](swbemdatetime-dayspecified.md)
-   [**HoursSpecified**](swbemdatetime-hoursspecified.md)
-   [**MinutesSpecified**](swbemdatetime-minutesspecified.md)
-   [**SecondsSpecified**](swbemdatetime-secondsspecified.md)
-   [**MicrosecondsSpecified**](swbemdatetime-microsecondsspecified.md)
-   [**UTCSpecified**](swbemdatetime-utcspecified.md)

Bei erfolgreicher Rückgabe [**von SetVarDate**](swbemdatetime-setvardate.md)werden alle diese Eigenschaften auf **TRUE festgelegt.**

Nach einem erfolgreichen Aufruf von [**SetVarDate**](swbemdatetime-setvardate.md)wird der [**DATETIME-Wert**](datetime.md) immer als absoluter **DATETIME-Wert** und nicht als Intervall interpretiert, und [**IsInterval**](swbemdatetime-isinterval.md) wird auf **FALSE festgelegt.**

Wenn [**IsInterval**](swbemdatetime-isinterval.md) auf **TRUE** festgelegt ist, führt ein Aufruf von **GetVarDate** zum **wbemErrFailed-Fehler.**

Beim Aufrufen von **GetVarDate** tritt ein Genauigkeitsverlust auf, da [datetime-Werte](datetime.md) eine Auflösung von 1 Mikrosekunden (s) und **VT \_ DATE-Werte** eine Auflösung von 500 Millisekunden haben.

## <a name="examples"></a>Beispiele

Beispiele für die Verwendung des [**SWbemDateTime-Objekts**](swbemdatetime.md) zum Konvertieren von CIM [**DATETIME-Werten**](datetime.md) in und aus dem **FILETIME-** oder **VT \_ DATE-Format** finden Sie unter [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md). Eine Beschreibung des CIM **DATETIME-Formats** finden Sie unter [Datums- und Uhrzeitformat.](date-and-time-format.md)

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

[**SWbemDateTime.GetFileTime**](swbemdatetime-getfiletime.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[Datetime](datetime.md)
</dt> </dl>

 

 




