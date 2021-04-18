---
description: Boolescher Wert, der angibt, ob die Komponente für die universelle koordinierte Uhrzeit (UTC) im CIM-DateTime-Wert ein Intervall oder einen Platzhalter Wert enthält.
ms.assetid: 9cb04351-294b-48ba-8d1c-2f28cb9ce463
ms.tgt_platform: multiple
title: "' Taubemdatetime. utcangegebene '-Eigenschaft (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.UTCSpecified
- ISWbemDateTime.UTCSpecified
- ISWbemDateTime.get_UTCSpecified
- ISWbemDateTime.put_UTCSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e2ada5bbbfa68e6cb63c0e060d6c3a12c0f771a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347472"
---
# <a name="swbemdatetimeutcspecified-property"></a>"Taubemdatetime. utcangegebene"-Eigenschaft

Die **utcspezifische** Eigenschaft des Objekts " [**Swap DateTime**](swbemdatetime.md) " ist ein boolescher Wert, der angibt, ob die Komponente für die universelle koordinierte Uhrzeit (UTC) im CIM-DateTime-Wert ein Intervall oder einen Platzhalter Wert enthält. Wenn **utcif** **true** und [**isinterval**](swbemdatetime-isinterval.md) den Wert **false** aufweist, enthält die Datei "- [**DateTime**](datetime.md) [**. UTC**](swbemdatetime-utc.md) " einen DateTime-Wert. Ein **DateTime** -Wert, der ein Intervall enthält, kann nicht in das **VT- \_ Datums** Format oder das **FILETIME** -Format konvertiert werden. Wenn **utcif** **false** ist und **isinterval** den Wert **true** aufweist, enthält " **taubemdatetime. UTC** " ein Intervall.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.UTCSpecified As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="examples"></a>Beispiele

Beispiele für die Verwendung des Objekts " [**slibemdatetime**](swbemdatetime.md) " zum Konvertieren von CIM- [**DateTime**](datetime.md) -Werten in das bzw. aus dem **DateTime** -oder **VT \_ Date** -Format finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](wmi-tasks--dates-and-times.md). Eine Beschreibung des CIM-DateTime-Formats finden Sie unter [Datums-und Uhrzeit Format](date-and-time-format.md).

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

[**"Taubemdatetime. UTC"**](swbemdatetime-utc.md)
</dt> <dt>

[**Swap-DateTime**](swbemdatetime.md)
</dt> <dt>

[DateTime](datetime.md)
</dt> </dl>

 

 




