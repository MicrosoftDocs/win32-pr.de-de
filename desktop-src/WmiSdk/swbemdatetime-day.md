---
description: Ruft einen Wert ab, der die Tageskomponente des datetime-Werts darstellt, oder legt diesen fest.
ms.assetid: 60da99bc-560c-45bc-b787-f4bef8e5a509
ms.tgt_platform: multiple
title: SWbemDateTime.Day-Eigenschaft (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Day
- ISWbemDateTime.Day
- ISWbemDateTime.get_Day
- ISWbemDateTime.put_Day
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d2483e52d9b40978a28f96bb5352df4f9abf4f89becf52550b82fd931580d7e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640500"
---
# <a name="swbemdatetimeday-property"></a>SWbemDateTime.Day-Eigenschaft

Die **Day-Eigenschaft** des [**SWbemDateTime-Objekts**](swbemdatetime.md) ruft einen Wert ab, der die Tageskomponente des datetime-Werts darstellt, oder legt diesen fest. Der Wert muss im Bereich von 1 bis 31 liegen, wenn [**IsInterval**](swbemdatetime-isinterval.md) **FALSE** ist. Bei der Fehlerüberprüfung wird der Monatswert jedoch nicht berücksichtigt. Daher gibt der In-Range-Wert von 31 keinen Fehler zurück, wenn der [**SWbemDateTime.Month-Wert**](swbemdatetime-month.md) für einen Monat von weniger als 31 Tagen gilt (Februar, April, Juni, September, November).

Der Standardwert für **Day** ist 01.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.Day As Long
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="error-codes"></a>Fehlercodes

Nachdem Sie die **Day-Eigenschaft** erhalten oder festgelegt haben, enthält das [Err-Objekt](/previous-versions//sbf5ze0e(v=vs.85)) möglicherweise den folgenden Fehlercode.

<dl> <dt>

**wbemErrValueOutOfRange** – 2147749931 (0x8004102B)
</dt> <dd>

Wenn [**IsInterval**](swbemdatetime-isinterval.md) **TRUE** ist und der Bereich der richtigen Werte 0 bis 99999999 überschreitet.

</dd> </dl>

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

[**SWbemDateTime.DaySpecified**](swbemdatetime-dayspecified.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[Datetime](datetime.md)
</dt> </dl>

 

