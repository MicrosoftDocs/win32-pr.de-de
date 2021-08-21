---
description: Stellt die Einstellungsdaten der Portabladungsfunktion dar.
ms.assetid: 7b8d8bee-86f3-4c55-bb32-987bf840d995
title: Msvm_EthernetSwitchPortOffloadSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortOffloadSettingData
- Msvm_EthernetSwitchPortOffloadSettingData.InstanceID
- Msvm_EthernetSwitchPortOffloadSettingData.Caption
- Msvm_EthernetSwitchPortOffloadSettingData.Description
- Msvm_EthernetSwitchPortOffloadSettingData.ElementName
- Msvm_EthernetSwitchPortOffloadSettingData.IPSecOffloadLimit
- Msvm_EthernetSwitchPortOffloadSettingData.VMQOffloadWeight
- Msvm_EthernetSwitchPortOffloadSettingData.IOVOffloadWeight
- Msvm_EthernetSwitchPortOffloadSettingData.IOVQueuePairsRequested
- Msvm_EthernetSwitchPortOffloadSettingData.IOVInterruptModeration
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectModerationInterval
- Msvm_EthernetSwitchPortOffloadSettingData.VmmqQueuePairs
- Msvm_EthernetSwitchPortOffloadSettingData.VrssVmbusChannelAffinityPolicy
- Msvm_EthernetSwitchPortOffloadSettingData.VrssIndependentHostSpreading
- Msvm_EthernetSwitchPortOffloadSettingData.VrssExcludePrimaryProcessor
- Msvm_EthernetSwitchPortOffloadSettingData.VrssQueueSchedulingMode
- Msvm_EthernetSwitchPortOffloadSettingData.VrssMinQueuePairs
- Msvm_EthernetSwitchPortOffloadSettingData.VmmqEnabled
- Msvm_EthernetSwitchPortOffloadSettingData.VrssEnabled
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectModerationCount
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectNumProcs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ddf58a10e85003a00e0d757f29db55a49f98f0ba22e8c3124b83a593f2a3908f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118148299"
---
# <a name="msvm_ethernetswitchportoffloadsettingdata-class"></a>Msvm \_ EthernetSwitchPortOffloadSettingData-Klasse

Stellt die Einstellungsdaten der Portabladungsfunktion dar.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("C885BFD1-ABB7-418F-8163-9F379C9F7166"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("4"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Offload Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortOffloadSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  InstanceID;
  string  Caption = "Ethernet Switch Port Offload Settings";
  string  Description = "Represents the port offload feature setting data.";
  string  ElementName = "Ethernet Switch Port Offload Settings";
  uint32  IPSecOffloadLimit = 512;
  uint32  VMQOffloadWeight = 100;
  uint32  IOVOffloadWeight = 0;
  uint32  IOVQueuePairsRequested = 1;
  uint32  IOVInterruptModeration = 0;
  uint32  PacketDirectModerationInterval = 0;
  uint32  VmmqQueuePairs = 16;
  uint32  VrssVmbusChannelAffinityPolicy = 3;
  boolean VrssIndependentHostSpreading = FALSE;
  boolean VrssExcludePrimaryProcessor = FALSE;
  uint32  VrssQueueSchedulingMode = 2;
  uint32  VrssMinQueuePairs = 1;
  boolean VmmqEnabled = FALSE;
  boolean VrssEnabled = TRUE;
  uint32  PacketDirectModerationCount = 0;
  uint32  PacketDirectNumProcs = 1;
};
```

## <a name="members"></a>Member

Die **Msvm \_ EthernetSwitchPortOffloadSettingData-Klasse** verfügt über folgende Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ EthernetSwitchPortOffloadSettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und immer auf "Ethernet Switch Port Offload Einstellungen" festgelegt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und immer auf "Stellt die Daten der Portabladungsfunktionseinstellung dar" festgelegt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeigename für das Objekt. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und immer auf "Ethernet Switch Port Offload Einstellungen" festgelegt.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**IOVInterruptModeration**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Der Interruptmoderationswert für die E/A-Virtualisierungsabladung (IOV). Die Standardeinstellung ist 0.

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**Standard** (0)


</dt> <dd></dd> <dt>

<span id="Adaptive"></span><span id="adaptive"></span><span id="ADAPTIVE"></span>

**Adaptive** (1)


</dt> <dd></dd> <dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

**Aus** (2)


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

**Niedrig** (100)


</dt> <dd></dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

**Mittel** (200)


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

**Hoch** (300)


</dt> <dd></dd> </dl>

</dd> <dt>

**IOVOffloadWeight**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Die Gewichtung, die diesem Port für die IOV-Auslagerung (E/A-Virtualisierung) zugewiesen ist. Die Gewichtung ist die relative Wichtigkeit beim Zuweisen von IOV-Ressourcen. Wenn Sie die **IOVOffloadWeight-Eigenschaft** auf 0 festlegen, wird die IOV-Auslagerung am Port deaktiviert. Die Standardeinstellung ist 0.

</dd> <dt>

**IOVQueuePairsRequested**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Die Anzahl der Warteschlangenpaare, die für diesen Port für die IOV-Auslagerung (E/A-Virtualisierung) angefordert werden. Der Standardwert ist 1.

</dd> <dt>

**IPSecOffloadLimit**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Die maximale Anzahl von Sicherheitszuordnungsslots(SA), die vom Port zugelassen werden.

</dd> <dt>

**PacketDirectModerationCount**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **WmiDataId** (7), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Der Wert der Interruptmoderationsanzahl für Packet Direct (PD). Der Standardwert ist 0.

> [!Note]  
> In Windows 10 hinzugefügte Eigenschaft.

 

</dd> <dt>

**PacketDirectModerationInterval**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **WmiDataId** (8), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Der Wert des Interruptmoderationsintervalls für Packet Direct (PD). Der Standardwert ist 0.

> [!Note]  
> In Windows 10 hinzugefügte Eigenschaft.

 

</dd> <dt>

**PacketDirectNumProcs**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **WmiDataId** (6), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Die Anzahl der Prozessoren, die vom Host für die Verarbeitung von Paketen verwendet werden, die von diesem Port im Modus "Paket direkt" gesendet werden. Der Standardwert ist 1.

> [!Note]  
> In Windows 10 hinzugefügte Eigenschaft.

 

</dd> <dt>

**VmmqEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **WmiDataId** (10), **InterfaceVersion** (3), **InterfaceRevision** (0)
</dt> </dl>

Aktivieren Sie die VMMQ-Auslagerung, sofern dies von der Hardware unterstützt wird. Der Standardwert ist False.

> [!Note]  
> Diese Eigenschaft wurde in Windows 10 Version 1703 und Windows Server 2016 hinzugefügt.

 

</dd> <dt>

**VmmqQueuePairs**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)
</dt> </dl>

Die Anzahl der Warteschlangen, die zugeordnet werden sollen, wenn VRSS aktiviert ist. Der Standardwert ist 16.

> [!Note]  
> Diese Eigenschaft wurde in Windows 10 Version 1703 und Windows Server 2016 hinzugefügt.

 

</dd> <dt>

**VMQOffloadWeight**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Die Gewichtung, die diesem Port für die VMQ-Auslagerung (Virtual Machine Queue) zugewiesen ist. Die Gewichtung ist die relative Wichtigkeit beim Zuweisen von VMQ-Ressourcen. Wenn Sie die **VMQOffloadWeight-Eigenschaft** auf 0 festlegen, wird VMQ am Port deaktiviert. Der Standardwert ist 100.

</dd> <dt>

**VrssEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **WmiDataId** (9), **InterfaceVersion** (3), **InterfaceRevision** (0)
</dt> </dl>

Aktivieren Sie VRSS. Der Standardwert ist "True".

> [!Note]  
> Diese Eigenschaft wurde in Windows 10 Version 1703 und Windows Server 2016 hinzugefügt.

 

</dd> <dt>

**VrssExcludePrimaryProcessor**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **WmiDataId** (14), **InterfaceVersion** (4), **InterfaceRevision** (0)
</dt> </dl>

Gibt an, ob der primäre VMQ-Prozessor aus der VRSS-Dekonstruktionstabelle ausgeschlossen werden soll, wenn VRSS aktiviert ist. Der Standardwert ist FALSE.

> [!Note]  
> Hinzugefügt in Windows 10 Version 1709.

 

</dd> <dt>

**VrssIndependentHostSpreading**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **WmiDataId** (15), **InterfaceVersion** (4), **InterfaceRevision** (0)
</dt> </dl>

Gibt an, ob bei aktiviertem VRSS immer eine hostseitige VRSS-Funktion erfolgt, unabhängig von der RSS-Einstellung der virtuellen NIC. Der Standardwert ist FALSE.

> [!Note]  
> Hinzugefügt in Windows 10 Version 1709.

 

</dd> <dt>

**VrssMinQueuePairs**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **WmiDataId** (12), **InterfaceVersion** (4), **InterfaceRevision** (0)
</dt> </dl>

Die Mindestanzahl von Warteschlangen, die zugeordnet werden sollen, wenn VRSS aktiviert ist. Der Standardwert ist 1.

> [!Note]  
> Hinzugefügt in Windows 10 Version 1709.

 

</dd> <dt>

**VrssQueueSchedulingMode**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **WmiDataId** (13), **InterfaceVersion** (4), **InterfaceRevision** (0)
</dt> </dl>

Der Warteschlangenplanungsmodus, der verwendet werden soll, wenn VRSS aktiviert ist. Der Standardwert ist die statische Zeitplanung.

> [!Note]  
> Hinzugefügt in Windows 10 Version 1709.

 

</dd> <dt>

**VrssVmbusChannelAffinityPolicy**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **WmiDataId** (16), **InterfaceVersion** (4), **InterfaceRevision** (0)
</dt> </dl>

Die vmbus-Kanalaffinitätsrichtlinie, die verwendet werden soll, wenn VRSS aktiviert ist. Der Standardwert ist stark.

> [!Note]  
> Hinzugefügt in Windows 10 Version 1709.

 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

