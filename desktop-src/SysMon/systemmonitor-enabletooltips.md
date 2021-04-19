---
title: Systemmonitor. EnableToolTips (Eigenschaft)
description: Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob eine QuickInfo angezeigt wird, wenn der Mauszeiger über einen Leistungsindikators in einer der Diagramm Ansichten bewegt wird (wird für die Berichtsansicht nicht unterstützt).
ms.assetid: af9a78ea-a9de-4343-8978-4316769a5f30
keywords:
- EnableToolTips-Eigenschaft (Sysmon)
- EnableToolTips-Eigenschaft (Sysmon), Systemmonitor-Objekt
- Systemmonitor-Objekt "sysmon", EnableToolTips (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.EnableToolTips
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 757cdd8a54bf6e5ae6e70b82dfc30865c796f944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342212"
---
# <a name="systemmonitorenabletooltips-property"></a>Systemmonitor. EnableToolTips (Eigenschaft)

Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob eine QuickInfo angezeigt wird, wenn der Mauszeiger über einen Leistungsindikators in einer der Diagramm Ansichten bewegt wird (wird für die Berichtsansicht nicht unterstützt).

## <a name="syntax"></a>Syntax


```VB
Property EnableToolTips As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

True zeigt eine QuickInfo mit den darin angezeigten Informationen zum Gegenstand an. andernfalls false.

## <a name="remarks"></a>Bemerkungen

Bei Linien Diagrammen ist die QuickInfo an dem Datenpunkt verankert, der der Maus am nächsten liegt. Bei Balkendiagrammen und Histogrammen stellt die QuickInfo den gesamten Datenwert des Balkens dar, nicht einen Punkt innerhalb des Balkens.

Die QuickInfo enthält verschiedene Informationen, die auf der Datenquelle basieren. Für Protokolldateien enthält die QuickInfo den Wert für den Leistungswert, den Leistungswert, den Zeitstempel, die Anzahl der Daten Stichproben, die im Datenpunkt enthalten sind, sowie die minimalen und maximalen Datenwerte.

Für echt Zeit Aktivität enthält die QuickInfo den Wert für den Leistungswert, den Leistungswert und den Zeitstempel.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





