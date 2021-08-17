---
title: SystemMonitor.LogFiles(Eigenschaft)
description: Sammlung von protokollierten Dateien, die als Quelle von Indikatorwerten verwendet werden, die im Systemmonitor angezeigt werden.
ms.assetid: 6e9e7205-3516-404d-b67d-777e484900da
keywords:
- LogFiles-Eigenschaft SysMon
- LogFiles-Eigenschaft SysMon , SystemMonitor-Objekt
- SystemMonitor-Objekt SysMon , LogFiles-Eigenschaft
topic_type:
- apiref
api_name:
- SystemMonitor.LogFiles
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bed0ea39809d3dfe40ebcedf2fbf2105833af836c12b95ffdfe442d3956d52a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882180"
---
# <a name="systemmonitorlogfiles-property"></a>SystemMonitor.LogFiles(Eigenschaft)

Sammlung von protokollierten Dateien, die als Quelle von Indikatorwerten verwendet werden, die im Systemmonitor angezeigt werden.

## <a name="syntax"></a>Syntax


```VB
Property LogFiles As ILogFiles
```



## <a name="property-value"></a>Eigenschaftswert

Sammlung von [**LogFileItem-Objekten,**](logfileitem.md) die die Protokolldateien angeben, die als Datenquelle für das Diagramm verwendet werden.

## <a name="remarks"></a>Hinweise

Zum Hinzufügen oder Entfernen einer Protokolldatei aus der Protokolldateisammlung darf der Wert von [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) nicht auf sysmonLogFiles festgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md)
</dt> <dt>

[**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md)
</dt> <dt>

[**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md)
</dt> <dt>

[**SystemMonitor.SqlLogSetName**](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





