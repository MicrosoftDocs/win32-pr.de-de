---
description: Ruft die koordinierte Weltzeit (UTC) des DateTime-Werts ab oder legt diese fest.
ms.assetid: 43d9d0c8-5521-410f-825b-6b00c3dd0039
ms.tgt_platform: multiple
title: Taubemdatetime. UTC-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.UTC
- ISWbemDateTime.UTC
- ISWbemDateTime.get_UTC
- ISWbemDateTime.put_UTC
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 80a4c32e47b94289f66999fdbf1f7daf5f9f03cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360168"
---
# <a name="swbemdatetimeutc-property"></a>Taubemdatetime. UTC (Eigenschaft)

Die **UTC** -Eigenschaft des " [**Swap DateTime**](swbemdatetime.md) "-Objekts Ruft die koordinierte Weltzeit (UTC) des **DateTime** -Werts ab oder legt diese fest. UTC ist die Zeit, die durch den Welt Zeit Standard festgelegt wird. Die UTC hat eine Ortszeit (GMT) ersetzt. Ein UTC-Wert mit einem Offset von 0 (null) entspricht der GMT-Abweichung mit einem Offset von 0. Die Zahl mit Vorzeichen muss im Bereich von-720 bis 720 liegen, oder der Fehler **wbemErrValueOutOfRange** wird zurückgegeben.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.UTC As Long
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="error-codes"></a>Fehlercodes

Nachdem Sie die **UTC** -Eigenschaft erhalten oder festgelegt haben, enthält das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt möglicherweise den folgenden Fehlercode.

<dl> <dt>

**wbemErrValueOutOfRange** -2147749931 (0x8004102b)
</dt> <dd>

Der Wert lag nicht im Bereich von-720 bis 720.

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

[**' Taubemdatetime. utc' angegeben**](swbemdatetime-utcspecified.md)
</dt> <dt>

[**Swap-DateTime**](swbemdatetime.md)
</dt> <dt>

[**DateTime**](datetime.md)
</dt> </dl>

 

