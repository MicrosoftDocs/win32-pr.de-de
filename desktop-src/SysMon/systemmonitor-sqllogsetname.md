---
title: Systemmonitor sqllogsetname (Eigenschaft)
description: Ruft den anzeigen amen des Protokoll Satzes ab oder legt ihn fest.
ms.assetid: a4593743-6b70-4f70-8e91-3324a808d97b
keywords:
- Sqllogsetname-Eigenschaft (Sysmon)
- Sqllogsetname-Eigenschaft (Sysmon), Systemmonitor-Schnittstelle
- Systemmonitor-Schnittstelle sysmon, sqllogsetname (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.SqlLogSetName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be20ccc561eb3e9292b4a95dcc654ed7bac00ba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040063"
---
# <a name="systemmonitorsqllogsetname-property"></a>Systemmonitor:: sqllogsetname (Eigenschaft)

Ruft den anzeigen amen des Protokoll Satzes ab oder legt ihn fest.

## <a name="syntax"></a>Syntax


```VB
Property SqlLogSetName As String
```



## <a name="property-value"></a>Eigenschaftswert

Anzeige Name des Protokoll Satzes, der einer einzelnen Protokolldatei entspricht, die Binär-oder Textdaten in der SQL-Datenbank enthält.

## <a name="remarks"></a>Bemerkungen

**Vor Windows Vista:** Sie können diese Eigenschaft nicht ändern, wenn der Wert von [**Systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) auf sysmonsqllog festgelegt ist.

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

[**Systemmonitor. sqldsnname**](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





