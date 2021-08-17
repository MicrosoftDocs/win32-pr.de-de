---
description: Gibt an, ob die Minutenkomponente im CIM-datetime-Wert ein Intervall oder einen Platzhalterwert enthält.
ms.assetid: de15f87e-0092-467e-b0d7-42ef447fa00a
ms.tgt_platform: multiple
title: SWbemDateTime.MinutesSpecified-Eigenschaft (Wbemdisp.h)
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
ms.openlocfilehash: a780d9bed3224e1b9be006a2bdf94b2b411951ceb3ef4d82a439ba5ec451fd44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992190"
---
# <a name="swbemdatetimeminutesspecified-property"></a>SWbemDateTime.MinutesSpecified-Eigenschaft

Die **MinutesSpecified-Eigenschaft** des [**SWbemDateTime-Objekts**](swbemdatetime.md) ist ein boolescher Wert, der angibt, ob die Minutenkomponente im CIM-datetime-Wert ein Intervall oder einen Platzhalterwert enthält. Wenn **MinutesSpecified** **auf TRUE** und [**IsInterval**](swbemdatetime-isinterval.md) auf **FALSE** festgelegt ist (was angibt, dass der CIM-datetime-Wert keine Platzhalter hat), enthält [**SWbemDateTime.Minutes**](swbemdatetime-minutes.md) einen Datumswert. Ein datetime-Wert, der ein Intervall enthält, kann weder in das **VT \_ DATE-Format** noch in das **FILETIME-Format** konvertiert werden. Wenn [**HoursSpecified**](swbemdatetime-hoursspecified.md) **FALSE** und **IsInterval** **TRUE** ist, enthält **SWbemDateTime.Minutes** ein Intervall.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.MinutesSpecified As boolean
```



## <a name="property-value"></a>Eigenschaftswert

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

[**SWbemDateTime.Minutes**](swbemdatetime-minutes.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[Datetime](datetime.md)
</dt> </dl>

 

 




