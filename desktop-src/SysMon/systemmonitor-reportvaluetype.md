---
title: SystemMonitor.ReportValueType-Eigenschaft
description: Ruft einen Wert ab, der bestimmt, ob das Histogramm und die Berichtsansicht den letzten wert, der während des Samplingintervalls entnommen wurde, oder einen berechneten Wert aus der Stichprobenentnahme, z. B. den Durchschnitts- oder Mindestzählerwert, darstellt, oder legt diesen fest.
ms.assetid: add75744-c3ab-48ab-b567-28a072facfdd
keywords:
- ReportValueType-Eigenschaft SysMon
- ReportValueType-Eigenschaft SysMon , SystemMonitor-Klasse
- SystemMonitor-Klasse SysMon , ReportValueType-Eigenschaft
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
ms.openlocfilehash: 95282c48ac30b13af07c124ea21f36f91c7ae658b10d290a109fdd1dcc7a5ee5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117955008"
---
# <a name="systemmonitorreportvaluetype-property"></a>SystemMonitor.ReportValueType-Eigenschaft

Ruft einen Wert ab, der bestimmt, ob das Histogramm und die Berichtsansicht den letzten wert, der während des Samplingintervalls entnommen wurde, oder einen berechneten Wert aus der Stichprobenentnahme, z. B. den Durchschnitts- oder Mindestzählerwert, darstellt, oder legt diesen fest.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Property ReportValueType As ReportValueTypeConstants
```



## <a name="property-value"></a>Eigenschaftswert

Bestimmt, ob die Histogramm- und Berichtsansichten den letzten wert graphieren, der während des Samplingintervalls entnommen wurde, oder einen berechneten Wert aus dem Samplingintervall. Mögliche Werte finden Sie unter [**ReportValueTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants).

## <a name="remarks"></a>Hinweise

SYSMON ignoriert diesen Wert und verwendet [**ReportValueTypeConstants.sysmonDefaultValue,**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants) wenn [**SystemMonitor.DisplayType**](systemmonitor-displaytype.md) nicht [**DisplayTypeConstants.sysmonHistogram**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants) oder **DisplayTypeConstants.sysmonReport** ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





