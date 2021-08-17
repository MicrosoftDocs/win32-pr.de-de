---
title: LogFiles.Remove-Methode
description: Entfernt die angegebene LogFileItem-Instanz aus der Auflistung.
ms.assetid: d2885ffd-5957-472c-9a67-2f1469d9b48b
keywords:
- Entfernen der SysMon-Methode
- Remove-Methode SysMon , LogFiles-Klasse
- LogFiles-Klasse SysMon , Remove-Methode
topic_type:
- apiref
api_name:
- LogFiles.Remove
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c12c0bae91df3baf421638665a5587612e6d1404c3300cf02b0308b7bef7d016
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117955433"
---
# <a name="logfilesremove-method"></a>LogFiles.Remove-Methode

Entfernt die angegebene [**LogFileItem-Instanz**](logfileitem.md) aus der Auflistung.

## <a name="syntax"></a>Syntax


```VB
LogFiles.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

Ganzzahliger Index der Protokolldatei, die aus der Auflistung entfernt werden soll. Der Index ist 1-basiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

**Vor der Windows Vista:** Protokolldateien können nicht aus der Protokolldateisammlung [**entfernt**](systemmonitor-logfiles.md) werden, wenn der Wert von [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) auf sysmonLogFiles festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[LogFiles](logfiles.md)
</dt> <dt>

[**LogFileItem**](logfileitem.md)
</dt> <dt>

[**LogFiles**](systemmonitor-logfiles.md)
</dt> </dl>

 

 





