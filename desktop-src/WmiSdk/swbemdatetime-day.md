---
description: Ruft einen Wert ab, der die Tages Komponente des DateTime-Werts darstellt, oder legt diesen fest.
ms.assetid: 60da99bc-560c-45bc-b787-f4bef8e5a509
ms.tgt_platform: multiple
title: Taubemdatetime. Day-Eigenschaft (wbemdisp. h)
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
ms.openlocfilehash: 1de77a8e5d616284c3dc13a19bce2526db371c20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960611"
---
# <a name="swbemdatetimeday-property"></a>Taubemdatetime. Day (Eigenschaft)

Die **Day** -Eigenschaft des " [**Swap DateTime**](swbemdatetime.md) "-Objekts Ruft einen Wert ab, der die Tages Komponente des DateTime-Werts darstellt, oder legt diesen fest. Der Wert muss zwischen 1 und 31 liegen, wenn [**isinterval**](swbemdatetime-isinterval.md) den Wert **false** hat. Allerdings ist die Fehlerüberprüfung für den Monatswert nicht vertraulich. Folglich gibt der in-Range-Wert 31 in den Fällen, in denen der Wert für " [**Swap DateTime. Month**](swbemdatetime-month.md) " für einen Monat weniger als 31 Tage beträgt (Februar, April, Juni, September, November), keinen Fehler zurück.

Der Standardwert für **Day** ist 01.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.Day As Long
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="error-codes"></a>Fehlercodes

Nachdem Sie die **Day** -Eigenschaft festgelegt oder festgelegt haben, enthält das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt möglicherweise den folgenden Fehlercode.

<dl> <dt>

**wbemErrValueOutOfRange** -2147749931 (0x8004102b)
</dt> <dd>

Wenn [**isinterval**](swbemdatetime-isinterval.md) den Wert **true** hat und der Bereich der korrekten Werte 0 bis 99999999 überschreitet.

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

[**Swap-DateTime. dayangegebene**](swbemdatetime-dayspecified.md)
</dt> <dt>

[**Swap-DateTime**](swbemdatetime.md)
</dt> <dt>

[DateTime](datetime.md)
</dt> </dl>

 

