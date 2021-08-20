---
description: Boolescher Wert, der angibt, ob die Mikrosekundenkomponente im CIM-datetime-Wert ein Intervall oder einen Platzhalterwert enthält.
ms.assetid: 65244ece-2326-4edc-b982-57e2046ec33e
ms.tgt_platform: multiple
title: SWbemDateTime.MicrosecondsSpecified-Eigenschaft (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.MicrosecondsSpecified
- ISWbemDateTime.MicrosecondsSpecified
- ISWbemDateTime.get_MicrosecondsSpecified
- ISWbemDateTime.put_MicrosecondsSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1b516b5fbe98c8bf481eaeed5b01c11f2dde6697a5832afc9d505d49254db2a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118816378"
---
# <a name="swbemdatetimemicrosecondsspecified-property"></a>SWbemDateTime.MicrosecondsSpecified-Eigenschaft

Die **MicrosecondsSpecified-Eigenschaft** des [**SWbemDateTime-Objekts**](swbemdatetime.md) ist ein boolescher Wert, der angibt, ob die Mikrosekundenkomponente im CIM-datetime-Wert ein Intervall oder einen Platzhalterwert enthält. Wenn **MicrosecondsSpecified** **TRUE** und [**IsInterval**](swbemdatetime-isinterval.md) **FALSE** ist, enthält [**SWbemDateTime.Microseconds**](swbemdatetime-microseconds.md) einen datetime-Wert. Ein datetime-Wert, der ein Intervall enthält, kann weder in das **VT \_ DATE-Format** noch in das **FILETIME-Format** konvertiert werden. Wenn [**HoursSpecified**](swbemdatetime-hoursspecified.md) **FALSE** und **IsInterval** **TRUE** ist, enthält **SWbemDateTime.Microseconds** ein Intervall.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.MicrosecondsSpecified As Boolean
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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SWbemDateTime.Microseconds**](swbemdatetime-microseconds.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[Datetime](datetime.md)
</dt> </dl>

 

 




