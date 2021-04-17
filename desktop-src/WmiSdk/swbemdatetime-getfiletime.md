---
description: Konvertiert einen Datums-und Uhrzeitwert im CIM-DateTime-Format in das FILETIME-Format.
ms.assetid: 08e0761d-e735-454a-8429-2bd1eb331123
ms.tgt_platform: multiple
title: Methode ' Swap DateTime. GetFileTime ' (wbemdisp. h)
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
ms.openlocfilehash: 3f8a8c85cb4c78be578187b1f55afce078fe7bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485731"
---
# <a name="swbemdatetimegetfiletime-method"></a>Methode ' Swap DateTime. GetFileTime '

Die **GetFileTime** -Methode des " [**slibemdatetime**](swbemdatetime.md) "-Objekts konvertiert einen Datums-und Uhrzeitwert im CIM- [DateTime](datetime.md) -Format in das FILETIME-Format.

Wenn der-Parameter auf **true** festgelegt ist, stellt der Rückgabewert eine Ortszeit für den Client dar. Andernfalls ist der Rückgabewert eine koordinierte Weltzeit (UTC). Eine **FILETIME** - [DateTime](datetime.md) -Struktur ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Einheiten seit dem Beginn des 1. Januar 1601 darstellt. Windows-Verwaltungsinstrumentation (WMI) behandelt **FILETIME** -Werte als Zeichen folgen Darstellungen von nicht signierten 64-Bit-Zahlen.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
vDate = .GetFileTime( _
  [ ByVal bIsLocaL ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bislocal* \[ in, optional\]
</dt> <dd>

Gibt an, ob der zurückgegebene Wert als Ortszeit interpretiert wird. Die UTC-Eigenschaft enthält dann die Ortszeit, die in den richtigen UTC-Offset (koordinierte Weltzeit) konvertiert wurde. Wenn der Wert **false** ist, wird der Wert als UTC mit einem Offset von 0 (null) interpretiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Das Datum und die Uhrzeit im **FILETIME** -Format.

## <a name="error-codes"></a>Fehlercodes

Nach dem Abschließen der **GetFileTime** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt den Fehlercode in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Der Aufruf schlug fehl.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

**VT \_ Datums** -und **FILETIME** -Werte dürfen keine Platzhalter Felder enthalten.

Bei der **GetFileTime** -Methode tritt ein Fehler auf (wbemErrFailed), wenn eine der folgenden Eigenschaften **false** ist:

-   [**Yearfest gelegt**](swbemdatetime-yearspecified.md)
-   [**Monthspezifiziert**](swbemdatetime-monthspecified.md)
-   [**Dayangegeben**](swbemdatetime-dayspecified.md)
-   [**Sansangegeben**](swbemdatetime-hoursspecified.md)
-   [**Minutesangegeben**](swbemdatetime-minutesspecified.md)
-   [**Secondsspezifiziert**](swbemdatetime-secondsspecified.md)
-   [**' Mikroseconds' angegeben**](swbemdatetime-microsecondsspecified.md)
-   [**Utcangegeben**](swbemdatetime-utcspecified.md)

Bei erfolgreicher Rückgabe von [**SetFileTime**](swbemdatetime-setfiletime.md)werden alle diese Eigenschaften auf **true** festgelegt.

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

[**"Slibemdatetime. getVarDate"**](swbemdatetime-getvardate.md)
</dt> <dt>

[**Swap-DateTime**](swbemdatetime.md)
</dt> <dt>

[**DateTime**](datetime.md)
</dt> </dl>

 

