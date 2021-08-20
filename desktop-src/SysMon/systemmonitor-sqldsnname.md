---
title: SystemMonitor-Eigenschaft "SqlDsnName"
description: Ruft den ODBC-Datenquellennamen (DSN) ab oder legt diese fest.
ms.assetid: 7906204a-a208-42c7-855b-c29689b4d36a
keywords:
- SqlDsnName-Eigenschaft SysMon
- SqlDsnName-Eigenschaft SysMon, SystemMonitor-Schnittstelle
- SystemMonitor-Schnittstelle SysMon , SqlDsnName-Eigenschaft
topic_type:
- apiref
api_name:
- SystemMonitor.SqlDsnName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4673ec5e753b91bb8022abe78efca4a5665d086e271c0b57407ed019d794d16f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117954819"
---
# <a name="systemmonitorsqldsnname-property"></a>SystemMonitor::SqlDsnName(Eigenschaft)

Ruft den ODBC-Datenquellennamen (DSN) ab oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
Property SqlDsnName As String
```



## <a name="property-value"></a>Eigenschaftswert

Odbc-Datenquellenname, der auf eine Datenbank verweist, die die richtigen Perfmon-Tabellen enthält. Das Format ist SQL:D SN.

## <a name="remarks"></a>Hinweise

Sie müssen das MmC-Snap-In Perfmon.msc verwenden, um die SQL zu generieren. Die Leistungsindikatorprotokolle befinden sich unter **Leistungsprotokolle und -warnungen**. Um ein SQL anzugeben, klicken Sie mit der rechten Maustaste auf die erstellte Protokolldatei, und wählen **Sie im Menü Eigenschaften** aus. Wählen Sie **auf der Eigenschaftenseite** Protokolldateien im **SQL-Datenbank** Dropdownliste **Protokolldateityp** die Option Protokolldateityp aus.

**Vor der Windows Vista:** Sie können diese Eigenschaft nicht ändern, wenn der Wert von [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) aufDataSourceTypeConstants.sys [**monSqlLog festgelegt ist.**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants) Sie müssen zuerst den Namen angeben und dann **SystemMonitor.DataSourceType** auf **DataSourceTypeConstants.sysmonSqlLog festlegen.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.SqlLogSetName**](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





