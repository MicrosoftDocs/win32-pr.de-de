---
description: Boolescher Wert, der angibt, ob die Monats Komponente im CIM-DateTime-Wert ein Intervall oder einen Platzhalter Wert enthält.
ms.assetid: 12dd94de-24be-4b13-bde5-2fc28be94efa
ms.tgt_platform: multiple
title: "' Taubemdatetime. monthspezifi'-Eigenschaft (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.MonthSpecified
- ISWbemDateTime.MonthSpecified
- ISWbemDateTime.get_MonthSpecified
- ISWbemDateTime.put_MonthSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 52b44444a5810577289353778c2c00b1ebfb80fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372956"
---
# <a name="swbemdatetimemonthspecified-property"></a>' Swap DateTime. monthangegebene '-Eigenschaft

Die **monthspezifisierte** Eigenschaft des Objekts " [**Swap DateTime**](swbemdatetime.md) " ist ein boolescher Wert, der angibt, ob die Monats Komponente im CIM-DateTime-Wert ein Intervall oder einen Platzhalter Wert enthält. Wenn **monthspezifiziert** **true** und [**isinterval**](swbemdatetime-isinterval.md) den Wert **false** aufweist, enthält " [**slibemdatetime. Month**](swbemdatetime-month.md) " einen Datumswert. Ein DateTime-Wert, der ein Intervall enthält, kann nicht in das **VT- \_ Datums** Format oder das **FILETIME** -Format konvertiert werden. Wenn **monthist** auf " **false** " festgelegt ist und **isinterval** " **true**" ist, enthält " **taubemdatetime. Month** " ein Intervall.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.MonthSpecified As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

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

[**Swap-DateTime. Month**](swbemdatetime-month.md)
</dt> <dt>

[**Swap-DateTime**](swbemdatetime.md)
</dt> <dt>

[DateTime](datetime.md)
</dt> </dl>

 

 




