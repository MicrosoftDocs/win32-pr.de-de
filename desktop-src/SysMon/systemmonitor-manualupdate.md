---
title: Systemmonitor. ManualUpdate (Eigenschaft)
description: Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob der Inhalt des System Monitors manuell oder in angegebenen Intervallen automatisch aktualisiert wird.
ms.assetid: e068a955-ec1d-4f93-9261-25ba87773913
keywords:
- ManualUpdate-Eigenschaft (Sysmon)
- ManualUpdate-Eigenschaft (Sysmon), Systemmonitor-Klasse
- Systemmonitor-Klasse "sysmon", ManualUpdate (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.ManualUpdate
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d1ecb426b47ba9cb7ec50b737f4f32d5ce274eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341605"
---
# <a name="systemmonitormanualupdate-property"></a>Systemmonitor. ManualUpdate (Eigenschaft)

Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob der Inhalt des System Monitors manuell oder in angegebenen Intervallen automatisch aktualisiert wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Property ManualUpdate As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

True gibt an, dass das Diagramm manuell aktualisiert wird. False gibt an, dass das Diagramm automatisch basierend auf dem in [**Systemmonitor. updateingeterval**](systemmonitor-updateinterval.md)angegebenen Aktualisierungs Intervall aktualisiert wird.

## <a name="remarks"></a>Bemerkungen

Standardmäßig wird das Diagramm automatisch aktualisiert.

Um das Diagramm manuell zu aktualisieren, wenden Sie die [**Systemmonitor. collectsample**](systemmonitor-collectsample.md) -Methode an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**System Monitor**](systemmonitor.md)
</dt> <dt>

[**Systemmonitor. collectsample**](systemmonitor-collectsample.md)
</dt> <dt>

[**Systemmonitor. updategraph**](systemmonitor-updategraph.md)
</dt> </dl>

 

 





