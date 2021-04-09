---
title: Systemmonitor. chartscroll-Eigenschaft
description: Ruft einen Wert ab, der bestimmt, ob das Liniendiagramm in der Ansicht einen Bildlauf ausführt, oder legt diesen fest
ms.assetid: df4806be-dfd3-4ff7-985d-b46c00bb19f8
keywords:
- Chartscroll-Eigenschaft (Sysmon)
- Chartscroll-Eigenschaft (Sysmon), Systemmonitor-Objekt
- Systemmonitor-Objekt (Sysmon), chartscroll (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.ChartScroll
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51288af710e5ae94baf46acf0d2ed91732a1d310
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956570"
---
# <a name="systemmonitorchartscroll-property"></a>Systemmonitor. chartscroll-Eigenschaft

Ruft einen Wert ab, der bestimmt, ob das Liniendiagramm in der Ansicht einen Bildlauf ausführt, oder legt diesen fest

## <a name="syntax"></a>Syntax


```VB
Property ChartScroll As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

True, wenn das Liniendiagramm von rechts nach links verschoben wird. andernfalls false, wenn das Liniendiagramm von links nach rechts gezeichnet wird und sich auf sich selbst in der Ansicht umschließt. "False" ist der Standardwert.

## <a name="remarks"></a>Bemerkungen

Dieser Wert wird ignoriert, wenn [**System Monitor. Display Type**](systemmonitor-displaytype.md) nicht [**DisplayTypeConstants.sysmonlinegraph**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants)ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





