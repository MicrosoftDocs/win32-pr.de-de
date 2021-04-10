---
title: Systemmonitor. reportvaluetype (Eigenschaft)
description: Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob im Histogramm und in den Berichts Ansichten der letzte Wert, der während des Samplingintervalls Stichprobe oder ein berechneter Wert aus der Stichprobe erfasst wurde
ms.assetid: add75744-c3ab-48ab-b567-28a072facfdd
keywords:
- Reportvaluetype-Eigenschaft (Sysmon)
- Reportvaluetype-Eigenschaft sysmon, Systemmonitor-Klasse
- Systemmonitor-Klasse (Sysmon), reportvaluetype-Eigenschaft
topic_type:
- apiref
api_name:
- SystemMonitor.ReportValueType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc340516f1d99bb77dcc5a31c03eb189d2d70a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956426"
---
# <a name="systemmonitorreportvaluetype-property"></a>Systemmonitor. reportvaluetype (Eigenschaft)

Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob im Histogramm und in den Berichts Ansichten der letzte Wert, der während des Samplingintervalls Stichprobe oder ein berechneter Wert aus der Stichprobe erfasst wurde

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Property ReportValueType As ReportValueTypeConstants
```



## <a name="property-value"></a>Eigenschaftswert

Bestimmt, ob das Histogramm und die Berichts Sichten den letzten Wert, der während des Samplingintervalls als Stichprobe oder einen berechneten Wert aus dem Samplingintervall Mögliche Werte finden Sie unter [**reportvaluetypeer Konstanten**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants).

## <a name="remarks"></a>Bemerkungen

Sysmon ignoriert diesen Wert und verwendet [**ReportValueTypeConstants.sysmondefaultvalue**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants) , wenn [**Systemmonitor. DisplayType**](systemmonitor-displaytype.md) nicht [**DisplayTypeConstants.sysmonhistogram**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants) oder **DisplayTypeConstants.sysmonreport** ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**System Monitor**](systemmonitor.md)
</dt> </dl>

 

 





