---
description: Migriert ein virtuelles System oder den Speicher eines virtuellen Systems zu einem Zielhost, der durch einen Hostnamen angegeben wird.
ms.assetid: 796b043c-5ac9-4c69-9838-0f415be5a63e
title: MigrateVirtualSystemToHost-Methode der Msvm_VirtualSystemMigrationService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.MigrateVirtualSystemToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7e6ebff1fabf1ed0b705dcbc4571566a5965b9120463bb009e68196f0c1f9a49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118149655"
---
# <a name="migratevirtualsystemtohost-method-of-the-msvm_virtualsystemmigrationservice-class"></a>MigrateVirtualSystemToHost-Methode der Msvm \_ VirtualSystemMigrationService-Klasse

Migriert ein virtuelles System oder den Speicher eines virtuellen Systems zu einem Zielhost, der durch einen Hostnamen angegeben wird.

## <a name="syntax"></a>Syntax


```mof
uint32 MigrateVirtualSystemToHost(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ComputerSystem* \[ In\]
</dt> <dd>

Ein Verweis auf eine Instanz der [**Msvm \_ ComputerSystem-Klasse,**](msvm-computersystem.md) die das zu migrierende virtuelle Computersystem darstellt.

</dd> <dt>

*DestinationHost* \[ In\]
</dt> <dd>

Der Name des Hostsystems für die Migration. Das Format dieses Namens wird von der **DestinationHostFormatsSupported-Eigenschaft** der [**Msvm \_ VirtualSystemMigrationCapabilities-Klasse**](msvm-virtualsystemmigrationcapabilities.md) angegeben, die dieser Klasse zugeordnet ist.

</dd> <dt>

*MigrationSettingData* \[ In\]
</dt> <dd>

Eine eingebettete Instanz der [**Msvm \_ VirtualSystemMigrationSettingData-Klasse,**](msvm-virtualsystemmigrationsettingdata.md) die Einstellungen für den Migrationsvorgang darstellt.

</dd> <dt>

*NewSystemSettingData* \[ In\]
</dt> <dd>

Eine eingebettete Instanz der [**Msvm \_ VirtualSystemSettingData-Klasse,**](msvm-virtualsystemsettingdata.md) die neue Eigenschaften darstellt, die nach der Migration auf das virtuelle System anwendbar sind.

</dd> <dt>

*NewResourceSettingData* \[ In\]
</dt> <dd>

Ein Array von Zeichenfolgen, das eine eingebettete Instanz der [**Msvm \_ ResourceAllocationSettingData-Klasse**](msvm-resourceallocationsettingdata.md) enthält, die die neuen Eigenschaften darstellt, die nach der Migration auf virtuelle Ressourcen des virtuellen Systems anwendbar sind.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ ConcreteJob abgeleitet wurde.**](/previous-versions//cc136808(v=vs.85))

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Überprüfte Methodenparameter – Auftrag gestartet** (4096)
</dt> <dt>

**Fehler** (32768)
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

**Status ist unbekannt** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger** Parameter (32773)
</dt> <dt>

**System wird verwendet** (32774)
</dt> <dt>

**Ungültiger Zustand für diesen Vorgang** (32775)
</dt> <dt>

**Falscher Datentyp** (32776)
</dt> <dt>

**System ist nicht verfügbar** (32777)
</dt> <dt>

**Nicht genügend Arbeitsspeicher** (32778)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

