---
description: Konvertiert ein Datum im VT- \_ Datumsformat in das CIM-DateTime-Format.
ms.assetid: 24c39d44-22ac-44ac-9e05-72a5b666ab19
ms.tgt_platform: multiple
title: "' Slibemdatetime. SetVarDate '-Methode (wbemdisp. h)"
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
ms.openlocfilehash: 8641bad2c59f100b689c74e23faf727bc80d2f49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348888"
---
# <a name="swbemdatetimesetvardate-method"></a>Slibemdatetime. SetVarDate-Methode

Die **SetVarDate** -Methode des [**"slibemdatetime**](swbemdatetime.md) "-Objekts konvertiert ein Datum im Format " **VT \_ Date** " in das [CIM-DateTime](date-and-time-format.md) -Format.

Ein **VT- \_ Datums** Wert ist ein Variant-DateTime-Wert, der von Visual Basic und ActiveX verwendet wird.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.SetVarDate( _
  ByVal vdate, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*vdate* \[ in\]
</dt> <dd>

Der Variant-Datumswert zum Festlegen des-Objekts. Dieser Parameter muss das **VT \_ Date** -Format aufweisen.

</dd> <dt>

*bislocal* \[ in, optional\]
</dt> <dd>

Wenn **true**, wird *vdate* als Ortszeit interpretiert, und die koordinierte Weltzeit (UTC)-Eigenschaft enthält die Ortszeit, die in den korrekten UTC-Offset konvertiert wird. Wenn *bislocal den* Wert **false** aufweist, wird *vdate* direkt in einen UTC-Wert mit einem Offset von 0 (null) konvertiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **SetVarDate** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt den Fehlercode in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrInvalidSyntax** -2147749921 (0x80041021)
</dt> <dd>

Das Format von *vdate* ist ungültig.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Nach einem erfolgreichen Aufruf von **SetVarDate** wird der [**DateTime**](datetime.md) -Wert als absoluter DateTime-Wert anstelle eines Intervalls interpretiert, und die [**isinterval**](swbemdatetime-isinterval.md) -Eigenschaft ist auf **false** festgelegt.

Die intrinsische Visual Basic-oder VBScript-Funktion [CDate](/previous-versions//2dt118h2(v=vs.85)) stellt einen [**DateTime**](datetime.md) -Wert im **VT- \_ Datums** Format für die Eingabe in **SetVarDate** bereit.

## <a name="examples"></a>Beispiele

Beispiele für die Verwendung des Objekts " [**slibemdatetime**](swbemdatetime.md) " zum Konvertieren von CIM- [**DateTime**](datetime.md) -Werten in das bzw. aus dem **DateTime** -oder **VT \_ Date** -Format finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](wmi-tasks--dates-and-times.md). Eine Beschreibung des CIM- **DateTime** -Formats finden Sie unter [Datums-und Uhrzeit Format](date-and-time-format.md).

Im Codebeispiel [Convert Date to WMI Date-Time Format](https://Gallery.TechNet.Microsoft.Com/33beff76-1b5f-4ba1-a8ea-5e124eb74306) VBScript in der TechNet Gallery wird SetVarDate verwendet, um einen regulären Datums-/Uhrzeitwert in das UTC-Datums-/Uhrzeitformat zu konvertieren.

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

[**' Swap DateTime. SetFileTime '**](swbemdatetime-setfiletime.md)
</dt> <dt>

[**Swap-DateTime**](swbemdatetime.md)
</dt> <dt>

[**DateTime**](datetime.md)
</dt> </dl>

 

