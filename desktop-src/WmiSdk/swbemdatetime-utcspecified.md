---
description: Boolescher Wert, der angibt, ob die UTC-Komponente (Universal Coordinated Time) im CIM-datetime-Wert ein Intervall oder einen Platzhalterwert enthält.
ms.assetid: 9cb04351-294b-48ba-8d1c-2f28cb9ce463
ms.tgt_platform: multiple
title: SWbemDateTime.UTCSpecified-Eigenschaft (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.UTCSpecified
- ISWbemDateTime.UTCSpecified
- ISWbemDateTime.get_UTCSpecified
- ISWbemDateTime.put_UTCSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 80c8ab92d07c2ef75ea57a66f6bae26c428780e15beeae31c9e5bd883407f03f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640370"
---
# <a name="swbemdatetimeutcspecified-property"></a>SWbemDateTime.UTCSpecified-Eigenschaft

Die **UTCSpecified-Eigenschaft** des [**SWbemDateTime-Objekts**](swbemdatetime.md) ist ein boolescher Wert, der angibt, ob die UTC-Komponente (Universal Coordinated Time) im CIM-datetime-Wert ein Intervall oder einen Platzhalterwert enthält. Wenn **UTCSpecified** **TRUE** und [**IsInterval**](swbemdatetime-isinterval.md) **FALSE** ist, enthält [**SWbemDateTime.UTC**](swbemdatetime-utc.md) einen [**DATETIME-Wert.**](datetime.md) Ein **DATETIME-Wert,** der ein Intervall enthält, kann weder in das **\_ VT-DATE-Format** noch in das **FILETIME-Format** konvertiert werden. Wenn **UTCSpecified** **FALSE** und **IsInterval** **TRUE** ist, enthält **SWbemDateTime.UTC** ein Intervall.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.UTCSpecified As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="examples"></a>Beispiele

Beispiele für die Verwendung des [**SWbemDateTime-Objekts**](swbemdatetime.md) zum Konvertieren von CIM [**DATETIME-Werten**](datetime.md) in und aus dem **FILETIME-Format** oder dem **VT \_ DATE-Format** finden Sie unter [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md). Eine Beschreibung des CIM-datetime-Formats finden Sie unter [Datums- und Uhrzeitformat.](date-and-time-format.md)

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

[**SWbemDateTime.UTC**](swbemdatetime-utc.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[Datetime](datetime.md)
</dt> </dl>

 

 




