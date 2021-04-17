---
description: Ändert die Einstellungen der virtuellen Ressource.
ms.assetid: 4942f167-0e53-4ae2-b973-4a06b636b44a
title: Modifyresourcesettings-Methode der CIM_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.ModifyResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e27729429d02c2412e05344779cc40461dbd9dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485363"
---
# <a name="modifyresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a>Modifyresourcesettings-Methode der CIM \_ virtualsystemmanagementservice-Klasse

Ändert die Einstellungen der virtuellen Ressource.

Wenn Sie auf Teile einer "aktuellen" virtuellen Systemkonfiguration angewendet werden, können die Ressourcen des aktiven virtuellen Systems ggf. geändert werden.

## <a name="syntax"></a>Syntax


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Resourcesettings* \[ in\]
</dt> <dd>

Ein Array von Zeichen folgen, die jeweils eine eingebettete Instanz der Klasse [**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md) enthalten, die Änderungen an den virtuellen Aspekten einer vorhandenen virtuellen Ressource beschreibt. Alle Instanzen müssen über eine gültige **InstanceId** verfügen, um die zu ändernde virtuelle Ressourcen Einstellung zu identifizieren.

</dd> <dt>

*Resultingresourcesettings* \[ vorgenommen\]
</dt> <dd>

Array von Verweisen auf Instanzen der Klasse [**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md) , die virtuelle Aspekte der geänderten virtuellen Ressourcen darstellen.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Wenn der Vorgang lange ausgeführt wird, wird optional ein Auftrag zurückgegeben. In diesem Fall sind die Instanzen der Klasse " [**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md) ", die die geänderten Ressourcen Einstellungen darstellen, über Association CIM "Configuration Manager" aus der Instanz der Klasse " [**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md) " verfügbar, die die betroffene virtuelle Systemkonfiguration darstellt. **\_**

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

 

 




