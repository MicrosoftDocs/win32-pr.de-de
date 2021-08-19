---
description: Ruft einen Wert ab, der die Sekundenkomponente des datetime-Werts darstellt, oder legt diesen fest.
ms.assetid: 194d4309-6abf-4c5f-99f8-60d2c835af6c
ms.tgt_platform: multiple
title: SWbemDateTime.Seconds-Eigenschaft (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Seconds
- ISWbemDateTime.Seconds
- ISWbemDateTime.get_Seconds
- ISWbemDateTime.put_Seconds
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4d30095e5464736b3db984b71f94a216c29f4327227a5e5b99becfbcae5e1a58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118816185"
---
# <a name="swbemdatetimeseconds-property"></a>SWbemDateTime.Seconds-Eigenschaft

Die **Seconds-Eigenschaft** des [**SWbemDateTime-Objekts**](swbemdatetime.md) ruft einen Wert ab, der die Sekundenkomponente des datetime-Werts darstellt, oder legt diesen fest.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.Seconds As Long
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="error-codes"></a>Fehlercodes

Nachdem Sie die **Seconds-Eigenschaft** erhalten oder festgelegt haben, enthält das [Err-Objekt](/previous-versions//sbf5ze0e(v=vs.85)) möglicherweise den folgenden Fehlercode.

<dl> <dt>

**wbemErrValueOutOfRange** – 2147749931 (0x8004102B)
</dt> <dd>

Der Wert lag nicht im Bereich von 0 bis 59.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **SWbemDateTime.Seconds-Eigenschaft** kann einen falschen Wert enthalten, wenn die [**SWbemDateTime.Minutes-Eigenschaft**](swbemdatetime-minutes.md) auf 1 festgelegt wurde. Sie enthält einen Wert, der aufgrund eines Rundungsfehlers, der auftritt, wenn ein CIM [**DATETIME-Wert**](datetime.md) in einen **VT \_ DATE-Wert** übersetzt wird, um eine Sekunde versetzt wird. Wenn die **Minutes-Eigenschaft** stattdessen auf 0 (null) festgelegt ist, gibt die **Seconds-Eigenschaft** den richtigen Wert zurück.

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

[**SWbemDateTime.SecondsSpecified**](swbemdatetime-secondsspecified.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**Datetime**](datetime.md)
</dt> </dl>

 

