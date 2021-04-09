---
description: Ändert die Einstellungen des virtuellen Systems.
ms.assetid: 9c3d28f8-9806-411a-866f-d062c6d31818
title: Modifysystemsettings-Methode der CIM_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.ModifySystemSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: da610d03e683b06ad743d1b6d4fe413dc5b31d34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959404"
---
# <a name="modifysystemsettings-method-of-the-cim_virtualsystemmanagementservice-class"></a>Modifysystemsettings-Methode der CIM \_ virtualsystemmanagementservice-Klasse

Ändert die Einstellungen des virtuellen Systems.

Wenn Sie auf die Systemeinstellungen einer "aktuellen" virtuellen Systemkonfiguration angewendet werden, kann die virtuelle System Instanz als Nebeneffekt geändert werden.

## <a name="syntax"></a>Syntax


```mof
uint32 ModifySystemSettings(
  [in]  string              SystemSettings,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SystemSettings* \[ in\]
</dt> <dd>

Eine Zeichenfolge, die eine Instanz der Klasse [**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md) enthält, die zum Ändern der Einstellungen des virtuellen Systems verwendet wird. Die Instanz muss eine gültige **InstanceId** aufweisen, um die zu ändernde Einstellung des virtuellen Systems zu identifizieren.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Wenn der Vorgang lange ausgeführt wird, kann optional ein [**CIM-" \_ concretejob**](cim-concretejob.md) " zurückgegeben werden, der den Auftrag darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

Fehler **(2** )
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Ungültiger Parameter** (4)
</dt> <dt>

**Ungültiger Status** (5)
</dt> <dt>

Nicht **kompatible Parameter** (6)
</dt> <dt>

**DMTF reserviert** (..)
</dt> <dt>

Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)
</dt> <dt>

**Reservierte Methode** (4097.32767)
</dt> <dt>

**Hersteller spezifisch** (32768.65535)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ virtualsystemmanagementservice**](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




