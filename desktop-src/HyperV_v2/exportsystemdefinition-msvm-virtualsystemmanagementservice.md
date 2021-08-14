---
description: Exportiert einen virtuellen Computer oder eine Momentaufnahme eines virtuellen Computers in eine Datei.
ms.assetid: b88712e4-a1a6-4188-8082-f4973f89018d
title: ExportSystemDefinition-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ExportSystemDefinition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 72198055a81ce13a6b38859ed5ba6370faf7de046bc9f2cc3a158548c2679685
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119254035"
---
# <a name="exportsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a>ExportSystemDefinition-Methode der Msvm \_ VirtualSystemManagementService-Klasse

Exportiert einen virtuellen Computer oder eine Momentaufnahme eines virtuellen Computers in eine Datei. Der virtuelle Computer muss sich im Zustand "Ausgeschaltet" oder "Gespeichert" befinden, um exportiert zu werden. Der virtuelle Computer, die zugehörigen Konfigurationseinstellungen und die zugehörigen Ressourceneinstellungen werden in der resultierenden Datei beibehalten.

## <a name="syntax"></a>Syntax


```mof
uint32 ExportSystemDefinition(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ExportDirectory,
  [in]  string                 ExportSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ComputerSystem* \[ In\]
</dt> <dd>

Ein Verweis auf ein [**\_ CIM-Computersystem, das**](/windows/desktop/CIMWin32Prov/cim-computersystem) den zu exportierenden virtuellen Computer darstellt.

</dd> <dt>

*ExportDirectory* \[ In\]
</dt> <dd>

Der vollqualifizierte Pfad des Verzeichnisses, in das der virtuelle Computer exportiert werden soll. Wenn die **CreateVmExportSubdirectory-Eigenschaft** der [**Msvm \_ VirtualSystemExportSettingData-Klasse**](msvm-virtualsystemexportsettingdata.md) im *ExportSettingData-Parameter* auf **True** festgelegt ist, kann dieses Verzeichnis zum Exportieren mehrerer virtueller Computer wiederverwendet werden, und diese Methode platziert jede Definition des virtuellen Computers in einem separaten Unterverzeichnis unter diesem Pfad.

</dd> <dt>

*ExportSettingData* \[ In\]
</dt> <dd>

Eine eingebettete Instanz der [**Msvm \_ VirtualSystemExportSettingData-Klasse,**](msvm-virtualsystemexportsettingdata.md) die die Einstellungen für den Exportvorgang darstellt.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein objekt, das von [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))abgeleitet wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Überprüfte Methodenparameter – Auftragsstart** (4096)
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

**Ungültiger Parameter** (32773)
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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

