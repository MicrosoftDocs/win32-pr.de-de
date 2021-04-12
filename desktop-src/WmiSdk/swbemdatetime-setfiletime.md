---
description: Konvertiert ein Datum im FILETIME-Zeichen folgen Format in das CIM-DateTime-Format.
ms.assetid: e375afda-5e94-46d6-b1ac-e801e0f4a620
ms.tgt_platform: multiple
title: Taubemdatetime. SetFileTime-Methode (wbemdisp. h)
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
ms.openlocfilehash: ca3e36a284e3700e166e86f6786218bada8f369e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130993"
---
# <a name="swbemdatetimesetfiletime-method"></a>Taubemdatetime. SetFileTime-Methode

Die **SetFileTime** -Methode des " [**slibemdatetime**](swbemdatetime.md) "-Objekts konvertiert ein Datum im **FILETIME** -Format der Zeichenfolge in das [CIM-DateTime](date-and-time-format.md) -Format.

Das **FILETIME** -Format ist eine 64-Bit-DateTime-Struktur, die die Anzahl der 100-Nanosecond-Einheiten seit dem Beginn des 1. Januar 1601 darstellt. Windows-Verwaltungsinstrumentation (WMI) behandelt **FILETIME** -Werte als Zeichen folgen Darstellungen von nicht signierten 64-Bit-Zahlen.

Die Syntax Erklärung finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.SetFileTime( _
  ByVal strFileTime, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

" *strinfiletime* \[ " in\]
</dt> <dd>

Der **FILETIME** -Wert, der zum Festlegen des Objekts verwendet wird.

</dd> <dt>

*bislocal* \[ in, optional\]
</dt> <dd>

**True** gibt an, dass " *strinfiletime* " als lokale Zeit interpretiert wird. Die koordinierte Weltzeit (UTC)-Eigenschaft enthält die Ortszeit, die in den korrekten UTC-Offset konvertiert wurde. Wenn " *bislocal" den* Wert " **false**" aufweist, wird " *straufiletime* " direkt in einen UTC-Wert mit einem Offset von 0 (null) konvertiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Nach dem Abschließen der **SetFileTime** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt den Fehlercode in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrInvalidSyntax** -2147749921 (0x80041021)
</dt> <dd>

Das Format von " *straufiletime* " ist ungültig.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Nach einem erfolgreichen Aufruf von **SetFileTime** wird der [**DateTime**](datetime.md) -Wert immer als absoluter Wert (**DateTime**) interpretiert, und [**isinterval**](swbemdatetime-isinterval.md) ist auf **false** festgelegt.

## <a name="examples"></a>Beispiele

Beispiele für die Verwendung des Objekts " [**slibemdatetime**](swbemdatetime.md) " zum Konvertieren von CIM- [**DateTime**](datetime.md) -Werten in das bzw. aus dem **DateTime** -oder **VT \_ Date** -Format finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](wmi-tasks--dates-and-times.md). Eine Beschreibung des CIM- **DateTime** -Formats finden Sie unter [Datums-und Uhrzeit Format](date-and-time-format.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-DateTime<br/>                                                         |
| IID<br/>                      | IID \_ iswbemdatetime<br/>                                                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Slibemdatetime. SetVarDate**](swbemdatetime-setvardate.md)
</dt> <dt>

[**Swap-DateTime**](swbemdatetime.md)
</dt> <dt>

[**DateTime**](datetime.md)
</dt> </dl>

 

