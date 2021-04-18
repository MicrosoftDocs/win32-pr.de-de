---
title: Systemmonitor. Logfiles (Eigenschaft)
description: Sammlung von einer oder mehreren Protokolldateien, die als Quelle der im System Monitor angezeigten Indikatoren verwendet werden sollen.
ms.assetid: 6e9e7205-3516-404d-b67d-777e484900da
keywords:
- Logfiles-Eigenschaft (Sysmon)
- Logfiles-Eigenschaft (Sysmon), Systemmonitor-Objekt
- Systemmonitor-Objekt "sysmon", Logfiles (Eigenschaft)
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
ms.openlocfilehash: c8127433319290b44498b272834923784b714052
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340329"
---
# <a name="systemmonitorlogfiles-property"></a>Systemmonitor. Logfiles (Eigenschaft)

Sammlung von einer oder mehreren Protokolldateien, die als Quelle der im System Monitor angezeigten Indikatoren verwendet werden sollen.

## <a name="syntax"></a>Syntax


```VB
Property LogFiles As ILogFiles
```



## <a name="property-value"></a>Eigenschaftswert

Sammlung von [**logfileitem**](logfileitem.md) -Objekten, die die Protokolldateien angeben, die als Datenquelle für das Diagramm verwendet werden.

## <a name="remarks"></a>Bemerkungen

Der Wert von [**Systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) darf nicht auf sysmonlogfiles festgelegt werden, um eine Protokolldatei in der Protokolldatei Sammlung hinzuzufügen oder zu entfernen.

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

[**Systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md)
</dt> <dt>

[**Systemmonitor. logviewstart**](systemmonitor-logviewstart.md)
</dt> <dt>

[**Systemmonitor. logviewstoppt**](systemmonitor-logviewstop.md)
</dt> <dt>

[**Systemmonitor. sqllogsetname**](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





