---
description: Ruft das RAW-CIM-Datum im DMTF-Format (verteilter Verwaltungs Task Force) ab oder legt es fest.
ms.assetid: 426a60d5-c364-406e-8346-049a13d59c7f
ms.tgt_platform: multiple
title: "' Taubemdatetime. Value '-Eigenschaft (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Value
- ISWbemDateTime.Value
- ISWbemDateTime.get_Value
- ISWbemDateTime.put_Value
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2ecb3a42a865559ba9b3c3e5fbec7302f975fa0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130992"
---
# <a name="swbemdatetimevalue-property"></a>Swap DateTime. Value-Eigenschaft

Die **value** -Eigenschaft des " [**slibemdatetime**](swbemdatetime.md) "-Objekts Ruft das RAW-CIM-Datum im DMTF-Format (verteilter Verwaltungs Task Force) ab oder legt es fest. Das DMTF-Format ist eine Zeichen folgen Darstellung des [**DateTime**](datetime.md) -Werts. Diese Eigenschaft ist die Standard Eigenschaft für " **Swap DateTime** "-Objekte. Die **value** -Eigenschaft hat den Standardwert 00000101000000.000000 + 000.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.Value As String
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="error-codes"></a>Fehlercodes

Nachdem Sie die **value** -Eigenschaft erhalten oder festgelegt haben, enthält das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt möglicherweise den folgenden Fehlercode.

<dl> <dt>

**wbemErrInvalidSyntax** -2147749921 (0x80041021)
</dt> <dd>

Das Format von " *strevalue* " ist ungültig.

</dd> </dl>

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

[**Swap-DateTime**](swbemdatetime.md)
</dt> <dt>

[**DateTime**](datetime.md)
</dt> </dl>

 

