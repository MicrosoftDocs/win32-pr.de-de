---
title: SystemMonitor.ShowTimeAxisLabels-Eigenschaft
description: Ruft einen Wert ab, der bestimmt, ob die horizontale (X)-Achse der Diagrammansicht Bezeichnungen enthält, oder legt diesen fest.
ms.assetid: 9e9d2d2c-f053-4afe-85de-25242842498f
keywords:
- ShowTimeAxisLabels-Eigenschaft SysMon
- ShowTimeAxisLabels-Eigenschaft SysMon , SystemMonitor-Objekt
- SystemMonitor-Objekt SysMon , ShowTimeAxisLabels-Eigenschaft
topic_type:
- apiref
api_name:
- SystemMonitor.ShowTimeAxisLabels
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ae2d6ae1fca7834c58a8ae84d1a4b7800a580b4efb0a5b675b7f95a40127067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117954907"
---
# <a name="systemmonitorshowtimeaxislabels-property"></a>SystemMonitor.ShowTimeAxisLabels-Eigenschaft

Ruft einen Wert ab, der bestimmt, ob die horizontale (X)-Achse der Diagrammansicht Bezeichnungen enthält, oder legt diesen fest.

## <a name="syntax"></a>Syntax


```VB
Property ShowTimeAxisLabels As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

Der Wert True wendet Bezeichnungen auf die x-Achse an. Der Wert False ist nicht. Die Standardeinstellung lautet „false“.

## <a name="remarks"></a>Hinweise

SYSMON ignoriert diese Eigenschaft für Balkendiagramme, Berichte und Histogramme.

Für Liniendiagramme verwendet SYSMON die Zeit, zu der der Indikatorwert als Bezeichnung entnommen wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



 

 





