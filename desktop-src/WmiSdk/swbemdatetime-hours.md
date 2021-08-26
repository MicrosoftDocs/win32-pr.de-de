---
description: Ruft einen Wert ab, der die Stundenkomponente des datetime-Werts darstellt, oder legt diesen fest.
ms.assetid: 83f084fa-57a5-4467-acea-7e19de82a91f
ms.tgt_platform: multiple
title: SWbemDateTime.Hours-Eigenschaft (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Hours
- ISWbemDateTime.Hours
- ISWbemDateTime.get_Hours
- ISWbemDateTime.put_Hours
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4ebe2cf5d25efd474268cea1459718f4741e4c4c698cbdbe65cc765cc17c2ae7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030380"
---
# <a name="swbemdatetimehours-property"></a>SWbemDateTime.Hours-Eigenschaft

Die **Hours-Eigenschaft** des [**SWbemDateTime-Objekts**](swbemdatetime.md) ruft einen Wert ab, der die Stundenkomponente des datetime-Werts darstellt, oder legt diesen fest.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.Hours As Long
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="error-codes"></a>Fehlercodes

Nachdem Sie die **Hours-Eigenschaft** erhalten oder festgelegt haben, enthält das [Err-Objekt](/previous-versions//sbf5ze0e(v=vs.85)) möglicherweise den folgenden Fehlercode.

<dl> <dt>

**wbemErrValueOutOfRange** – 2147749931 (0x8004102B)
</dt> <dd>

Der Wert lag nicht im Bereich von 0 bis 23.

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

[**SWbemDateTime.HoursSpecified**](swbemdatetime-hoursspecified.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**Datetime**](datetime.md)
</dt> </dl>

 

