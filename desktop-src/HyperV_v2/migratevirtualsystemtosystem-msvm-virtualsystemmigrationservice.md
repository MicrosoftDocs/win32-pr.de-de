---
description: Verschiebt, migriert oder verschiebt ein virtuelles System in ein Zielsystem.
ms.assetid: 3a0be791-4514-4ce2-b4e8-3735bd6ea1d7
title: MigrateVirtualSystemToSystem-Methode der Msvm_VirtualSystemMigrationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.MigrateVirtualSystemToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 398c4ae9d9d8ad89f7188ecbfe19e1b687bd694f7e716e88bd5231e79a38a665
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694279"
---
# <a name="migratevirtualsystemtosystem-method-of-the-msvm_virtualsystemmigrationservice-class"></a>MigrateVirtualSystemToSystem-Methode der Msvm \_ VirtualSystemMigrationService-Klasse

Verschiebt, migriert oder verschiebt ein virtuelles System in ein Zielsystem.

## <a name="syntax"></a>Syntax


```mof
uint32 MigrateVirtualSystemToSystem(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  CIM_System         REF DestinationSystem,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ComputerSystem REF NewComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ComputerSystem* \[ In\]
</dt> <dd>

Ein Verweis auf eine Instanz der [**Msvm \_ ComputerSystem-Klasse,**](msvm-computersystem.md) die das zu migrierende virtuelle Computersystem darstellt.

</dd> <dt>

*DestinationSystem* \[ In\]
</dt> <dd>

Ein Verweis auf eine Instanz der [**Msvm \_ ComputerSystem-Klasse,**](msvm-computersystem.md) die das System darstellt, zu dem migriert werden soll.

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

*NewComputerSystem* \[ out\]
</dt> <dd>

Ein Verweis auf eine Instanz der [**Msvm \_ ComputerSystem-Klasse,**](msvm-computersystem.md) die das neue migrierte System darstellt.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ ConcreteJob abgeleitet wurde.**](/previous-versions//cc136808(v=vs.85))

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

**Fehler** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Ungültiger Parameter** (4)
</dt> <dt>

**Ungültiger Zustand** (5)
</dt> <dt>

**Inkompatible** Parameter (6)
</dt> <dt>

**DMTF Reserved** (..)
</dt> <dt>

**Überprüfte Methodenparameter – Auftrag gestartet** (4096)
</dt> <dt>

**Reservierte Methode** (4097..32767)
</dt> <dt>

**Herstellerspezifisch** (32768..65535 )
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

 

