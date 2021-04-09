---
description: Boolescher Wert, der angibt, ob die Sekunden Komponente im CIM-DateTime-Wert ein Intervall oder einen Platzhalter Wert enthält.
ms.assetid: 9f9b75c3-ae08-49a6-b747-294831601a62
ms.tgt_platform: multiple
title: "' Swap DateTime. secondsangegebene '-Eigenschaft (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SecondsSpecified
- ISWbemDateTime.SecondsSpecified
- ISWbemDateTime.get_SecondsSpecified
- ISWbemDateTime.put_SecondsSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e0cf97eff544d6e244890014108506f39b1934b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868388"
---
# <a name="swbemdatetimesecondsspecified-property"></a>' Swap DateTime. secondsangegebene '-Eigenschaft

Die **secondsspezifisierte** Eigenschaft des-Objekts von " [**Swap DateTime**](swbemdatetime.md) " ist ein boolescher Wert, der angibt, ob die Sekunden Komponente im CIM- [**DateTime**](datetime.md) -Wert ein Intervall oder einen Platzhalter Wert enthält. Wenn **secondsspezifiziert** **true** und [**isinterval**](swbemdatetime-isinterval.md) den Wert **false** aufweist, enthält " [**slibemdatetime. seconds**](swbemdatetime-seconds.md) " einen Datumswert. Ein DateTime-Wert, der ein Intervall enthält, kann nicht in das **VT- \_ Datums** Format oder das **FILETIME** -Format konvertiert werden. Wenn **secondsist** auf **false** festgelegt und **isinterval** den Wert **true** aufweist, enthält der Wert von " **taubemdatetime. seconds** " ein Intervall.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.SecondsSpecified As Boolean
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

[**Swap-DateTime. Sekunden**](swbemdatetime-seconds.md)
</dt> <dt>

[**Swap-DateTime**](swbemdatetime.md)
</dt> <dt>

[DateTime](datetime.md)
</dt> </dl>

 

 




