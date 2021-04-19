---
description: Konvertiert einen Datums-und Uhrzeitwert im CIM-DateTime-Format in das VT \_ Date-Format.
ms.assetid: e63e7acc-89d4-458a-a1ab-4d4a65cf7f8b
ms.tgt_platform: multiple
title: "' Slibemdatetime. getVarDate '-Methode (wbemdisp. h)"
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
ms.openlocfilehash: b4d0c71e4748774eacab4b234092178179a4a774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348287"
---
# <a name="swbemdatetimegetvardate-method"></a>Slibemdatetime. getVarDate-Methode

Die **getVarDate** -Methode des " [**slibemdatetime**](swbemdatetime.md) "-Objekts konvertiert einen Datums-und Uhrzeitwert im CIM- [**DateTime**](datetime.md) -Format in das **VT \_ Date** -Format.

Das **VT \_ Date** -Format ist ein [**DateTime**](datetime.md) -Wert für die Automatisierung, der von Visual Basic und ActiveX verwendet wird.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
vdate = .GetVarDate( _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bislocal* \[ in, optional\]
</dt> <dd>

Gibt an, ob der zurückgegebene Wert als Ortszeit interpretiert wird. Die koordinierte Weltzeit (UTC)-Eigenschaft enthält die Ortszeit, die in den korrekten UTC-Offset konvertiert wurde. Wenn der Wert **false** ist, wird der Wert als UTC mit einem Offset von 0 (null) interpretiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Datums-und Uhrzeitwert im **VT- \_ Datums** Format.

## <a name="remarks"></a>Bemerkungen

**VT \_ Datums** -und **FILETIME** -Werte dürfen keine Platzhalter Felder enthalten.

Die **getVarDate** -Methode schlägt fehl (**wbemErrFailed**), wenn eine der folgenden Eigenschaften **false** ist:

-   [**Yearfest gelegt**](swbemdatetime-yearspecified.md)
-   [**Monthspezifiziert**](swbemdatetime-monthspecified.md)
-   [**Dayangegeben**](swbemdatetime-dayspecified.md)
-   [**Sansangegeben**](swbemdatetime-hoursspecified.md)
-   [**Minutesangegeben**](swbemdatetime-minutesspecified.md)
-   [**Secondsspezifiziert**](swbemdatetime-secondsspecified.md)
-   [**' Mikroseconds' angegeben**](swbemdatetime-microsecondsspecified.md)
-   [**Utcangegeben**](swbemdatetime-utcspecified.md)

Bei erfolgreicher Rückgabe von [**SetVarDate**](swbemdatetime-setvardate.md)werden alle diese Eigenschaften auf **true** festgelegt.

Nach einem erfolgreichen Aufruf von [**SetVarDate**](swbemdatetime-setvardate.md)wird der [**DateTime**](datetime.md) -Wert immer als absoluter **DateTime** -Wert anstelle eines Intervalls interpretiert, und [**isinterval**](swbemdatetime-isinterval.md) ist auf **false** festgelegt.

Wenn [**isinterval**](swbemdatetime-isinterval.md) auf **true** festgelegt ist, führt ein Rückruf von **getVarDate** zu einem **wbemErrFailed** -Fehler.

Ein Genauigkeits Verlust tritt auf, wenn Sie **getVarDate** aufrufen, da [DateTime](datetime.md) -Werte eine Auflösung von einer Mikrosekunde (n) aufweisen und die **VT \_ Date** -Werte eine 500 Millisekunde-Auflösung aufweisen.

## <a name="examples"></a>Beispiele

Beispiele für die Verwendung des [**"slibemdatetime**](swbemdatetime.md) "-Objekts zum Konvertieren von CIM- [**DateTime**](datetime.md) -Werten in bzw. aus dem **DateTime** -oder **VT \_ Date** -Format finden Sie unter [WMI-Tasks: Datumsangaben und Uhrzeiten](wmi-tasks--dates-and-times.md). Eine Beschreibung des CIM- **DateTime** -Formats finden Sie unter [Datums-und Uhrzeit Format](date-and-time-format.md).

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

[**' Swap DateTime. GetFileTime '**](swbemdatetime-getfiletime.md)
</dt> <dt>

[**Swap-DateTime**](swbemdatetime.md)
</dt> <dt>

[DateTime](datetime.md)
</dt> </dl>

 

 




