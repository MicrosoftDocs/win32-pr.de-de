---
description: Exportiert einen virtuellen Computer oder eine Momentaufnahme eines virtuellen Computers in eine Datei.
ms.assetid: b88712e4-a1a6-4188-8082-f4973f89018d
title: Exportsystemdefinition-Methode der Msvm_VirtualSystemManagementService-Klasse
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
ms.openlocfilehash: 9f6b6dc5728a4275965ccd482d851601ecd1c6e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749640"
---
# <a name="exportsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Exportsystemdefinition-Methode der MSVM \_ virtualsystemmanagementservice-Klasse

Exportiert einen virtuellen Computer oder eine Momentaufnahme eines virtuellen Computers in eine Datei. Der virtuelle Computer muss sich im Zustand "ausgeschaltet" oder "gespeichert" befinden, um exportiert werden zu können. Der virtuelle Computer, die zugehörigen Konfigurationseinstellungen und die zugehörigen Ressourcen Einstellungen werden in der resultierenden Datei beibehalten.

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

*Computersystem* \[ in\]
</dt> <dd>

Ein Verweis auf ein [**CIM- \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , das den zu exportierenden virtuellen Computer darstellt.

</dd> <dt>

*Exportdirectory* \[ in\]
</dt> <dd>

Der voll qualifizierte Pfad des Verzeichnisses, in das der virtuelle Computer exportiert werden soll. Wenn die Eigenschaft " **kreatevmexportsubdirectory** " der [**MSVM-Klasse " \_ virtualsystemexportsettingdata**](msvm-virtualsystemexportsettingdata.md) " im Parameter " *exportsettingdata* " auf " **true**" festgelegt ist, kann dieses Verzeichnis für den Export mehrerer virtueller Computer wieder verwendet werden, und diese Methode platziert die Definitionen der virtuellen Maschinen in einem separaten Unterverzeichnis unter diesem Pfad.

</dd> <dt>

*Exportsettingdata* \[ in\]
</dt> <dd>

Eine eingebettete Instanz der [**MSVM \_ virtualsystemexportsettingdata**](msvm-virtualsystemexportsettingdata.md) -Klasse, die die Einstellungen für den Export Vorgang darstellt.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)
</dt> <dt>

Fehler **(32768** )
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

Der **Status ist "Unknown** " (32771).
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger Parameter** (32773)
</dt> <dt>

**System wird verwendet** (32774)
</dt> <dt>

**Ungültiger Status für diesen Vorgang** (32775).
</dt> <dt>

**Falscher Datentyp** (32776).
</dt> <dt>

Das **System ist nicht verfügbar** (32777).
</dt> <dt>

**Nicht** genügend Arbeitsspeicher (32778)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

