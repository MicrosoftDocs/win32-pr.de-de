---
title: Systemmonitor. showtimeaxislabels (Eigenschaft)
description: Ruft einen Wert ab, der bestimmt, ob die horizontale Achse (X) der Diagramm Ansicht Bezeichnungen enthält, oder legt ihn fest.
ms.assetid: 9e9d2d2c-f053-4afe-85de-25242842498f
keywords:
- Showtimeaxislabels-Eigenschaft (Sysmon)
- Showtimeaxislabels-Eigenschaft (Sysmon), Systemmonitor-Objekt
- Systemmonitor-Objekt "sysmon", showtimeaxislabels (Eigenschaft)
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
ms.openlocfilehash: 06569dcd4702ae687b09bfae88c84482a49afb71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337306"
---
# <a name="systemmonitorshowtimeaxislabels-property"></a>Systemmonitor. showtimeaxislabels (Eigenschaft)

Ruft einen Wert ab, der bestimmt, ob die horizontale Achse (X) der Diagramm Ansicht Bezeichnungen enthält, oder legt ihn fest.

## <a name="syntax"></a>Syntax


```VB
Property ShowTimeAxisLabels As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

Mit dem Wert true werden Bezeichnungen auf die x-Achse angewendet. Der Wert false ist nicht. Die Standardeinstellung lautet „false“.

## <a name="remarks"></a>Bemerkungen

Sysmon ignoriert diese Eigenschaft für Balkendiagramme, Berichte und Histogramme.

Bei Linien Diagrammen verwendet sysmon die Zeit, in der der Wert des Leistungs Zählers als Bezeichnung erfasst wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





