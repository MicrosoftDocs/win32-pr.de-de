---
description: Ruft einen Wert ab, der die Minutenkomponente des datetime-Werts darstellt, oder legt diesen fest.
ms.assetid: a52a66c2-f7ab-48d0-bdee-a07984ed3bc2
ms.tgt_platform: multiple
title: SWbemDateTime.Minutes-Eigenschaft (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Minutes
- ISWbemDateTime.Minutes
- ISWbemDateTime.get_Minutes
- ISWbemDateTime.put_Minutes
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5a6150dcdee6051fdfb8737618f4735cfe1e568da05ec35a6cd935be197a56ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992240"
---
# <a name="swbemdatetimeminutes-property"></a>SWbemDateTime.Minutes-Eigenschaft

Die **Minutes-Eigenschaft** des [**SWbemDateTime-Objekts**](swbemdatetime.md) ruft einen Wert ab, der die Minutenkomponente des datetime-Werts darstellt, oder legt diesen fest.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.Minutes As Long
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="error-codes"></a>Fehlercodes

Nachdem Sie die **Minutes-Eigenschaft** erhalten oder festgelegt haben, kann das [Err-Objekt](/previous-versions//sbf5ze0e(v=vs.85)) den folgenden Fehlercode enthalten.

<dl> <dt>

**wbemErrValueOutOfRange** – 2147749931 (0x8004102B)
</dt> <dd>

Der Wert lag nicht im Bereich von 0 bis 59.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn die **SWbemDateTime.Minutes-Eigenschaft** auf 1 festgelegt ist, enthält die [**SWbemDateTime.Seconds-Eigenschaft**](swbemdatetime-seconds.md) einen Wert, der um eine Sekunde versetzt wird. Ein Rundungsfehler tritt auf, wenn ein **CIM-datetime-Wert** in einen **VT \_ DATE-Wert** übersetzt wird. Wenn die **Minutes-Eigenschaft** stattdessen auf 0 festgelegt ist, gibt die **Seconds-Eigenschaft** den richtigen Wert zurück.

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

[**SWbemDateTime.MinutesSpecified**](swbemdatetime-minutesspecified.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**Datetime**](datetime.md)
</dt> </dl>

 

