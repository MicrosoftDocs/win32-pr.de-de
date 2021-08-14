---
description: Konvertiert ein Datum im FILETIME-Format der Zeichenfolge in das CIM-datetime-Format.
ms.assetid: e375afda-5e94-46d6-b1ac-e801e0f4a620
ms.tgt_platform: multiple
title: SWbemDateTime.SetFileTime-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SetFileTime
- ISWbemDateTime.SetFileTime
- ISWbemDateTime.SetFileTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 138685ba4d6b63591bf460da3cdba219685f015d54789ca60a52660845b2e41a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739457"
---
# <a name="swbemdatetimesetfiletime-method"></a>SWbemDateTime.SetFileTime-Methode

Die **SetFileTime-Methode** des [**SWbemDateTime-Objekts**](swbemdatetime.md) konvertiert ein Datum im **FILETIME-Format** der Zeichenfolge in das [CIM-datetime-Format.](date-and-time-format.md)

Das **FILETIME-Format** ist eine datetime-Struktur mit 64 Bit, die die Anzahl von 100 Nanosekunden seit Dem 1. Januar 1601 darstellt. Windows Die Verwaltungsinstrumentation (Management Instrumentation, WMI) behandelt **FILETIME-Werte** als Zeichenfolgendarstellungen von 64-Bit-Zahlen ohne Vorzeichen.

Die Syntaxerklärung finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.SetFileTime( _
  ByVal strFileTime, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*strFileTime* \[ In\]
</dt> <dd>

**FILETIME-Wert,** der zum Festlegen des Objekts verwendet wird.

</dd> <dt>

*bIsLocal* \[ in, optional\]
</dt> <dd>

True gibt an, dass *strFileTime* als Ortszeit interpretiert wird. Die eigenschaft koordinierte Weltzeit (UTC) enthält die in den richtigen UTC-Offset konvertierte Ortszeit. Wenn *bIsLocal* **FALSE** ist, wird *strFileTime* direkt in einen UTC-Wert mit einem Offset von 0 (null) konvertiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **SetFileTime-Methode** kann das [Err-Objekt](/previous-versions//sbf5ze0e(v=vs.85)) den Fehlercode in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrInvalidSyntax** – 2147749921 (0x80041021)
</dt> <dd>

Das Format von *strFileTime* ist ungültig.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Nach einem erfolgreichen Aufruf von **SetFileTime** wird der [**datetime-Wert**](datetime.md) immer als absoluter Wert (**datetime**) interpretiert, und [**IsInterval**](swbemdatetime-isinterval.md) wird auf **FALSE** festgelegt.

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

[**SWbemDateTime.SetVarDate**](swbemdatetime-setvardate.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**Datetime**](datetime.md)
</dt> </dl>

 

