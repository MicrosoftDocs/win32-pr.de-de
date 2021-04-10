---
title: Systemmonitor. datapointcount-Eigenschaft
description: Ruft die Anzahl der Datenpunkte ab, die in einem Liniendiagramm angezeigt werden, oder legt Sie fest.
ms.assetid: bc1a86c2-635b-4e93-ac96-e7be4b1d375a
keywords:
- Datapointcount-Eigenschaft (Sysmon)
- Datapointcount-Eigenschaft (Sysmon), Systemmonitor-Objekt
- Systemmonitor-Objekt "sysmon", datapointcount (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.DataPointCount
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fffb8b39216895ce4ebce6924ca7cc99b5366cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949649"
---
# <a name="systemmonitordatapointcount-property"></a>Systemmonitor. datapointcount-Eigenschaft

Ruft die Anzahl der Datenpunkte ab, die in einem Liniendiagramm angezeigt werden, oder legt Sie fest.

## <a name="syntax"></a>Syntax


```VB
Property DataPointCount As Long
```



## <a name="property-value"></a>Eigenschaftswert

Anzahl von Datenpunkten, die in der Ansicht für ein Liniendiagramm angezeigt werden. Der Standardwert ist 100 Datenpunkte. Der gültige Wertebereich ist 2 bis 1.000.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird nur verwendet, wenn [**Systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) **sysmoncurrentactivity** ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





