---
title: Logfiles. Remove-Methode
description: Entfernt die angegebene logfileitem-Instanz aus der Auflistung.
ms.assetid: d2885ffd-5957-472c-9a67-2f1469d9b48b
keywords:
- Remove-Methode (Sysmon)
- Remove-Methode (Sysmon), Logfiles-Klasse
- Logfiles-Klasse sysmon, Remove-Methode
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
ms.openlocfilehash: 057607c57db600ca7a28c8a5bb6d75d5570829cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742936"
---
# <a name="logfilesremove-method"></a>Logfiles. Remove-Methode

Entfernt die angegebene [**logfileitem**](logfileitem.md) -Instanz aus der Auflistung.

## <a name="syntax"></a>Syntax


```VB
LogFiles.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

Ganzzahliger Index der Protokolldatei, der aus der Auflistung entfernt werden soll. Der Index ist 1-basiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

**Vor Windows Vista:** Sie können Protokolldateien nicht aus der [**Protokolldatei Sammlung**](systemmonitor-logfiles.md) entfernen, wenn der Wert von [**Systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) auf sysmonlogfiles festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[LogFiles](logfiles.md)
</dt> <dt>

[**Logfileitem**](logfileitem.md)
</dt> <dt>

[**LogFiles**](systemmonitor-logfiles.md)
</dt> </dl>

 

 





