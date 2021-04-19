---
description: Boolescher Wert, der angibt, ob die Tages Komponente im CIM-DateTime-Wert ein Intervall oder einen Platzhalter Wert enthält.
ms.assetid: a713378b-3953-49d8-9c6a-44aa9337eae2
ms.tgt_platform: multiple
title: "' Swap-DateTime. dayangegebene '-Eigenschaft (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.DaySpecified
- ISWbemDateTime.DaySpecified
- ISWbemDateTime.get_DaySpecified
- ISWbemDateTime.put_DaySpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f295d33940f36212fde4fe821af8d5df24d4f75f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353206"
---
# <a name="swbemdatetimedayspecified-property"></a>Eigenschaft ' Swap DateTime. dayangegebene '

Die **dayangegebene** -Eigenschaft des-Objekts von " [**Swap DateTime**](swbemdatetime.md) " ist ein boolescher Wert, der angibt, ob die Tages Komponente im CIM- [**DateTime**](datetime.md) -Wert ein Intervall oder einen Platzhalter Wert enthält. Wenn **dayfest gelegt** **ist** und [**isinterval**](swbemdatetime-isinterval.md) den Wert **false** aufweist, enthält " [**taubemdatetime. Day**](swbemdatetime-day.md) " einen DateTime-Wert. Ein [**DateTime**](datetime.md) -Wert, der ein Intervall enthält, kann nicht in das **VT- \_ Datums** Format oder das **FILETIME** -Format konvertiert werden. Wenn **dayist** auf **false** festgelegt und **isinterval** den Wert **true** aufweist, enthält " **taubemdatetime. Day** " ein Intervall.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.DaySpecified As BOOLEAN
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

[**Swap-DateTime. Day**](swbemdatetime-day.md)
</dt> <dt>

[**Swap-DateTime**](swbemdatetime.md)
</dt> <dt>

[**DateTime**](datetime.md)
</dt> </dl>

 

 




