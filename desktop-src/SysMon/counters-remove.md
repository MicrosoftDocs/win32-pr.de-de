---
title: Counters. Remove-Methode
description: Entfernt eine-Instanz aus der Auflistung.
ms.assetid: 88e5907a-8c8f-4a24-9c5d-0c592f61dac0
keywords:
- Remove-Methode (Sysmon)
- Remove-Methode (Sysmon), counters-Klasse
- Zähler Klasse sysmon, Methode entfernen
topic_type:
- apiref
api_name:
- Counters.Remove
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa82a1a988be3554c265c097ba2a582035547391
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949747"
---
# <a name="countersremove-method"></a>Counters. Remove-Methode

Entfernt eine [**-**](counteritem.md) Instanz aus der Auflistung.

## <a name="syntax"></a>Syntax


```VB
Counters.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

Der Index des aus der Auflistung zu entfernenden [**ratteritem**](counteritem.md) -Objekts. Der Index ist 1-basiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="exceptions"></a>Ausnahmen



| Ausnahmetyp                                  | Bedingung                                                      |
|-------------------------------------------------|----------------------------------------------------------------|
| **System. Runtime. InteropServices. COMException** | Der angegebene Index ist ungültig. Der Err. Number-Wert ist???. |



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie alle Leistungsindikatoren aus der Sammlung entfernen möchten, können Sie [**Systemmonitor. Reset**](systemmonitor-reset.md)abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Counters**](counters.md)
</dt> <dt>

[**Systemmonitor. Reset**](systemmonitor-reset.md)
</dt> </dl>

 

 





