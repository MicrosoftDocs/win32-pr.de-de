---
title: Systemmonitor sqldsnname (Eigenschaft)
description: Ruft den ODBC-Datenquellen Namen (DSN) ab oder legt ihn fest.
ms.assetid: 7906204a-a208-42c7-855b-c29689b4d36a
keywords:
- Sqldsnname-Eigenschaft (Sysmon)
- Sqldsnname-Eigenschaft (Sysmon), Systemmonitor-Schnittstelle
- Systemmonitor-Schnittstelle sysmon, sqldsnname (Eigenschaft)
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
ms.openlocfilehash: 666b10ad91956adf7148e54b68f2b6db98e9a5b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391496"
---
# <a name="systemmonitorsqldsnname-property"></a>Systemmonitor:: sqldsnname (Eigenschaft)

Ruft den ODBC-Datenquellen Namen (DSN) ab oder legt ihn fest.

## <a name="syntax"></a>Syntax


```VB
Property SqlDsnName As String
```



## <a name="property-value"></a>Eigenschaftswert

Der ODBC-Datenquellen Name, der auf eine Datenbank verweist, die die richtigen Perfmon-Tabellen enthält. Das Format ist SQL: DSN.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie das MMC-Snap-in "Perfmon. msc", um die SQL-Protokolldatei zu generieren. Die Counter-Protokolle befinden sich unter **Leistungsprotokolle und-Warnungen**. Um ein SQL-Protokoll anzugeben, klicken Sie mit der rechten Maustaste auf die von Ihnen erstellte Protokolldatei, und wählen Sie im Menü **Eigenschaften** aus. Wählen Sie auf der Eigenschaften Seite **Protokolldateien** im Dropdown-Listenfeld **Protokoll Dateityp** die Option **SQL-Datenbank** aus.

**Vor Windows Vista:** Sie können diese Eigenschaft nicht ändern, wenn der Wert von [**Systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) auf [**DataSourceTypeConstants.sysmonsqllog**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants)festgelegt ist. Sie müssen zuerst den Namen angeben und dann **Systemmonitor. DataSourceType** auf **DataSourceTypeConstants.sysmonsqllog** festlegen.

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

[**Systemmonitor. sqllogsetname**](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





