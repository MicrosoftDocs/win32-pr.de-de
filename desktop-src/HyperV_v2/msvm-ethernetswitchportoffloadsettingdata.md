---
description: Stellt die Einstellungsdaten für die Port Auslagerung dar.
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
ms.openlocfilehash: 150a7b5e54e371c11741dd7c763b0ae145354b09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355480"
---
# <a name="msvm_ethernetswitchportoffloadsettingdata-class"></a>MSVM \_ ethernezwitchportoffloadsettingdata-Klasse

Stellt die Einstellungsdaten für die Port Auslagerung dar.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

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

Die **MSVM \_ ethernezwitchportoffloadsettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ ethernezwitchportoffloadsettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des-Objekts. Diese Eigenschaft wird vom [**CIM \_ managedelta-Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet Switch Port Offload Settings" festgelegt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "stellt die Einstellung für die Funktion der Port Abladung" dar.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeige Name für das-Objekt. Diese Eigenschaft wird vom [**CIM \_ managedelta-Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet Switch Port Offload Settings" festgelegt.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Iovinterruptmode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (5), **interfacetten** (1), **interfakerevision** (0)
</dt> </dl>

Der Wert für die Unterbrechungs Moderation für die e/a-Virtualisierung (IOV). Die Standardeinstellung ist 0.

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

**Iovoffloadweight**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (3), **interfacetten** (1), **interfakerevision** (0)
</dt> </dl>

Die Gewichtung, die diesem Port für die e/a-Virtualisierung (IOV) zugewiesen wird. Die Gewichtung ist die relative Wichtigkeit beim Zuweisen von IOV-Ressourcen. Wenn Sie die **iovoffloadweight** -Eigenschaft auf 0 festlegen, wird die IOV-Auslagerung auf dem Port deaktiviert. Die Standardeinstellung ist 0.

</dd> <dt>

**Iovqueuepairrsangefordert**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (4), **interfacetten** (1), **interfakerevision** (0)
</dt> </dl>

Die Anzahl der für diesen Port angeforderten Warteschlangen Paare für die e/a-Virtualisierung (IOV). Der Standardwert ist 1.

</dd> <dt>

**Ipmencoffloadlimit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (1), **interfacetten** (1), **interfakerevision** (0)
</dt> </dl>

Die maximale Anzahl von Auslagerungs Slots (Security Association, SA), die vom Port zugelassen werden.

</dd> <dt>

**Packetdirectmoderationcount**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (7), **interfacetten** (2), **interfakerevision** (0)
</dt> </dl>

Der Wert der Unterbrechungs Moderations Moderation für "Packet Direct" (PD). Der Standardwert ist 0.

> [!Note]  
> Die Eigenschaft wurde in Windows 10 hinzugefügt.

 

</dd> <dt>

**Packetdirectmoderationinterval**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (8), **interfacetten** (2), **interfakerevision** (0)
</dt> </dl>

Der Wert für das interruptermoderationsintervall für "Packet Direct" (PD). Der Standardwert ist 0.

> [!Note]  
> Die Eigenschaft wurde in Windows 10 hinzugefügt.

 

</dd> <dt>

**Packetdirectnumprocs**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (6), **interfacetten** (2), **interfakerevision** (0)
</dt> </dl>

Die Anzahl der Prozessoren, die vom Host für die Verarbeitung von Paketen verwendet werden, die von diesem Port im Paket direkt Modus gesendet werden. Der Standardwert ist 1.

> [!Note]  
> Die Eigenschaft wurde in Windows 10 hinzugefügt.

 

</dd> <dt>

**Vmmqaktivierte**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (10), **interfacetten** (3), **interfakerevision** (0)
</dt> </dl>

Aktivieren Sie vmmq-Auslagerung, wenn dies von Hardware unterstützt wird. Der Standardwert ist false.

> [!Note]  
> Diese Eigenschaft wurde in Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.

 

</dd> <dt>

**Vmmqqueuepairs**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (11), **interfacetten** (3), **interfakerevision** (0)
</dt> </dl>

Die Anzahl der Warteschlangen, die bei Aktivierung von vrss zuzuordnen sind. Der Standardwert ist 16.

> [!Note]  
> Diese Eigenschaft wurde in Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.

 

</dd> <dt>

**Vmqoffloadweight**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (2), **interfacetten** (1), **interfakerevision** (0)
</dt> </dl>

Die Gewichtung, die diesem Port für die VM-Offloads (Virtual Machine Queue, VMQ) zugewiesen ist. Die Gewichtung ist die relative Wichtigkeit beim Zuweisen von VMQ-Ressourcen. Wenn Sie die **vmqoffloadweight** -Eigenschaft auf 0 festlegen, wird VMQ auf dem Port deaktiviert. Der Standard ist 100.

</dd> <dt>

**Vrssaktivierte**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (9), **interfacetten** (3), **interfakerevision** (0)
</dt> </dl>

Aktivieren Sie vrss. Der Standardwert ist "True".

> [!Note]  
> Diese Eigenschaft wurde in Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.

 

</dd> <dt>

**Vrssexcludeprimaryprocessor**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (14), **interfacetten** (4), **interfakerevision** (0)
</dt> </dl>

Ob primärer VMQ-Prozessor aus der vrss-dereferenzierungstabelle ausgeschlossen werden soll, wenn vrss aktiviert ist. Der Standardwert ist false.

> [!Note]  
> Hinzugefügt in Windows 10, Version 1709.

 

</dd> <dt>

**Vrssindependenthostverteilung**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (15), **interfacetten** (4), **interfakerevision** (0)
</dt> </dl>

Gibt an, ob bei aktiviertem vrss immer Host seitiger vrss durchzuführen ist, unabhängig von der RSS-Einstellung der virtuellen NIC. Der Standardwert ist false.

> [!Note]  
> Hinzugefügt in Windows 10, Version 1709.

 

</dd> <dt>

**Vrssminqueuepairs**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (12), **interfacetten** (4), **interfakerevision** (0)
</dt> </dl>

Die Mindestanzahl von Warteschlangen, die bei Aktivierung von vrss zuzuordnen sind. Der Standardwert ist 1.

> [!Note]  
> Hinzugefügt in Windows 10, Version 1709.

 

</dd> <dt>

**Vrssqueueschedulingmode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (13), **interfacetten** (4), **interfakerevision** (0)
</dt> </dl>

Der zu verwendende Warteschlangen Planungsmodus, wenn vrss aktiviert ist. Der Standardwert ist die statische Zeitplanung.

> [!Note]  
> Hinzugefügt in Windows 10, Version 1709.

 

</dd> <dt>

**Vrssvmbuschannelaffinitypolicy**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (16), **interfacetten** (4), **interfakerevision** (0)
</dt> </dl>

Die zu verwendende VMBus-channelaffinitäts Richtlinie, wenn vrss aktiviert ist. Der Standardwert ist "Strong".

> [!Note]  
> Hinzugefügt in Windows 10, Version 1709.

 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

