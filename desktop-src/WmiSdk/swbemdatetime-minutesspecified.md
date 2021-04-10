---
description: Gibt an, ob die Minuten Komponente im CIM-DateTime-Wert ein Intervall oder einen Platzhalter Wert enthält.
ms.assetid: de15f87e-0092-467e-b0d7-42ef447fa00a
ms.tgt_platform: multiple
title: "' Taubemdatetime. minutesangegebene '-Eigenschaft (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.MinutesSpecified
- ISWbemDateTime.MinutesSpecified
- ISWbemDateTime.get_MinutesSpecified
- ISWbemDateTime.put_MinutesSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 62f64ad749ee020093008a308a3244e045f9995d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130996"
---
# <a name="swbemdatetimeminutesspecified-property"></a>"Taubemdatetime. minutesangegebene"-Eigenschaft

Die **minutesspezifizierte** -Eigenschaft des-Objekts von " [**Swap DateTime**](swbemdatetime.md) " ist ein boolescher Wert, der angibt, ob die Minuten Komponente im CIM-DateTime-Wert ein Intervall oder einen Platzhalter Wert enthält. Wenn **minutesist** **true** und [**isinterval**](swbemdatetime-isinterval.md) auf **false** festgelegt ist (was bedeutet, dass der CIM-DateTime-Wert keine Platzhalter hat), enthält " [**slibemdatetime. minutes**](swbemdatetime-minutes.md) " einen Datumswert. Ein DateTime-Wert, der ein Intervall enthält, kann nicht in das **VT- \_ Datums** Format oder das **FILETIME** -Format konvertiert werden. Wenn [**"hoursist**](swbemdatetime-hoursspecified.md) **false** " und " **isinterval** " auf " **true**" festgelegt ist, enthält " **taubemdatetime. minutes** " ein Intervall.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.MinutesSpecified As boolean
```



## <a name="property-value"></a>Eigenschaftswert

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

[**Swap DateTime. Minutes**](swbemdatetime-minutes.md)
</dt> <dt>

[**Swap-DateTime**](swbemdatetime.md)
</dt> <dt>

[DateTime](datetime.md)
</dt> </dl>

 

 




