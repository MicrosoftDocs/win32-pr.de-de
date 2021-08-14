---
title: SystemMonitor.DataPointCount-Eigenschaft
description: Ruft die Anzahl der in einem Liniendiagramm angezeigten Datenpunkte ab oder legt diese fest.
ms.assetid: bc1a86c2-635b-4e93-ac96-e7be4b1d375a
keywords:
- DataPointCount-Eigenschaft SysMon
- DataPointCount-Eigenschaft SysMon , SystemMonitor-Objekt
- SystemMonitor-Objekt SysMon , DataPointCount-Eigenschaft
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
ms.openlocfilehash: 3d7d1212f3f1467c0fb505e84dffdd9cc6bb381c19d8ccc34ad38ee46562ec6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882625"
---
# <a name="systemmonitordatapointcount-property"></a>SystemMonitor.DataPointCount-Eigenschaft

Ruft die Anzahl der in einem Liniendiagramm angezeigten Datenpunkte ab oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
Property DataPointCount As Long
```



## <a name="property-value"></a>Eigenschaftswert

Anzahl von Datenpunkten, die in der Ansicht für ein Liniendiagramm angezeigt werden. Der Standardwert ist 100 Datenpunkte. Der gültige Wertebereich ist 2 bis 1.000.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird nur verwendet, wenn [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) **sysmonCurrentActivity** ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



 

 





