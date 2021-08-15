---
description: Konvertiert ein Datum im VT \_ DATE-Format in das CIM-DateTime-Format.
ms.assetid: 24c39d44-22ac-44ac-9e05-72a5b666ab19
ms.tgt_platform: multiple
title: SWbemDateTime.SetVarDate-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SetVarDate
- ISWbemDateTime.SetVarDate
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 56d193bd2faffd51507ec4a913c7ee068b055dcf45ca756e801431659768c47d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050098"
---
# <a name="swbemdatetimesetvardate-method"></a>SWbemDateTime.SetVarDate-Methode

Die **SetVarDate-Methode** des [**SWbemDateTime-Objekts**](swbemdatetime.md) konvertiert ein Datum im **VT \_ DATE-Format** in das [CIM datetime-Format.](date-and-time-format.md)

Ein **VT \_ DATE-Wert** ist ein variant datetime-Wert, der Visual Basic und ActiveX wird.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.SetVarDate( _
  ByVal vdate, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*vdate* \[ In\]
</dt> <dd>

Der Variant-Datumswert zum Festlegen des -Objekts. Dieser Parameter muss im **VT \_ DATE-Format** vorliegen.

</dd> <dt>

*bIsLocal* \[ in, optional\]
</dt> <dd>

True **gibt an,** *dass vdate* als lokale Zeit interpretiert wird, und die koordinierte Weltzeit (UTC)-Eigenschaft enthält die Ortszeit, die in den richtigen UTC-Offset konvertiert wird. Wenn *bIsLocal* **FALSE ist,** wird *vdate* direkt in einen UTC-Wert mit einem Offset von 0 (null) konvertiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **SetVarDate-Methode** enthält das [Err-Objekt](/previous-versions//sbf5ze0e(v=vs.85)) möglicherweise den Fehlercode in der folgenden Liste.

<dl> <dt>

**wbemErrInvalidSyntax** – 2147749921 (0x80041021)
</dt> <dd>

Das Format *von vdate* ist ungültig.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Nach einem erfolgreichen Aufruf von **SetVarDate** wird der [**DATETIME-Wert**](datetime.md) als absoluter datetime-Wert anstelle eines Intervalls interpretiert, und die [**IsInterval-Eigenschaft**](swbemdatetime-isinterval.md) wird auf **FALSE festgelegt.**

Die systeminterne Visual Basic- oder VBScript-Funktion [CDate](/previous-versions//2dt118h2(v=vs.85)) stellt einen [**datetime-Wert**](datetime.md) im **VT \_ DATE-Format** für die Eingabe in **SetVarDate zur Verfügung.**

## <a name="examples"></a>Beispiele

Beispiele für die Verwendung des [**SWbemDateTime-Objekts**](swbemdatetime.md) zum Konvertieren von CIM [**DATETIME-Werten**](datetime.md) in und aus dem **FILETIME-Format** oder dem **VT \_ DATE-Format** finden Sie unter [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md). Eine Beschreibung des CIM **DATETIME-Formats** finden Sie unter [Datums- und Uhrzeitformat.](date-and-time-format.md)

Im Codebeispiel Convert [Date to WMI Date-Time Format](https://Gallery.TechNet.Microsoft.Com/33beff76-1b5f-4ba1-a8ea-5e124eb74306) VBScript im TechNet Gallery wird SetVarDate verwendet, um einen regulären Datums-/Uhrzeitwert in das UTC-Format für Datum und Uhrzeit zu konvertieren.

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

[**SWbemDateTime.SetFileTime**](swbemdatetime-setfiletime.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**Datetime**](datetime.md)
</dt> </dl>

 

