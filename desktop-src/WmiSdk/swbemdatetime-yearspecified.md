---
description: Boolescher Wert, der angibt, ob die Jahreskomponente im CIM-datetime-Wert ein Intervall oder einen Platzhalterwert enthält.
ms.assetid: afac0a08-7bd0-42f1-b5a7-8664f9db8615
ms.tgt_platform: multiple
title: SWbemDateTime.YearSpecified-Eigenschaft (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.YearSpecified
- ISWbemDateTime.YearSpecified
- ISWbemDateTime.get_YearSpecified
- ISWbemDateTime.put_YearSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2cb8a3733d6aaf5679c47d0cf61ca05b2154b57edfd64e5152c0da1f8c822dd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118815959"
---
# <a name="swbemdatetimeyearspecified-property"></a>SWbemDateTime.YearSpecified-Eigenschaft

Die **YearSpecified-Eigenschaft** des [**SWbemDateTime-Objekts**](swbemdatetime.md) ist ein boolescher Wert, der angibt, ob die Year-Komponente im CIM-datetime-Wert ein Intervall oder einen Platzhalterwert enthält. Wenn **YearSpecified** **TRUE** und [**IsInterval**](swbemdatetime-isinterval.md) **FALSE** ist, enthält [**SWbemDateTime.Year**](swbemdatetime-year.md) einen datetime-Wert. Ein datetime-Wert, der ein Intervall enthält, kann weder in das **VT \_ DATE-Format** noch in das **FILETIME-Format** konvertiert werden. Wenn **YearSpecified** **FALSE** und **IsInterval** **TRUE** ist, enthält **SWbemDateTime.Year** ein Intervall.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.YearSpecified As Boolean
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

[**SWbemDateTime.Year**](swbemdatetime-year.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[Datetime](datetime.md)
</dt> </dl>

 

 




