---
title: Vmvirtualmachineevents-Enumeration (vpccominterfaces. h)
description: Gibt die VM-Ereignisse an.
ms.assetid: 158bdada-6fd3-488c-9ff1-e04df9a79127
keywords:
- Vmvirtualmachineevents-Enumeration virtueller PC
topic_type:
- apiref
api_name:
- VMVirtualMachineEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1e1d8f4d89c28f63886444537fb9d894fc42e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040906"
---
# <a name="vmvirtualmachineevents-enumeration"></a>Vmvirtualmachineevents-Enumeration

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Gibt die Ereignisse des virtuellen Computers (Virtual Machine, VM) an.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  vmVirtualMachineEvent_StateChanged              = 1,
  vmVirtualMachineEvent_RequestShutdown           = 2,
  vmVirtualMachineEvent_Reset                     = 3,
  vmVirtualMachineEvent_TripleFault               = 4,
  vmVirtualMachineEvent_HeartbeatStopped          = 5,
  vmVirtualMachineEvent_ConfigurationChanged      = 6,
  vmVirtualMachineEvent_EnhancedVideoModeChanged  = 7,
  vmVirtualMachineEvent_AdditionsUninstalled      = 8,
  vmVirtualMachineEvent_AdditionsAvailable        = 9,
  vmVirtualMachineEvent_GuestShutdown             = 10,
  vmVirtualMachineEvent_GuestLogoff               = 11,
  vmVirtualMachineEvent_DiskOutOfSpace            = 12
} VMVirtualMachineEvents;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="vmVirtualMachineEvent_StateChanged"></span><span id="vmvirtualmachineevent_statechanged"></span><span id="VMVIRTUALMACHINEEVENT_STATECHANGED"></span>**vmvirtualmachineevent \_ StateChanged**
</dt> <dd>

Der Status eines virtuellen Computers wurde geändert.

</dd> <dt>

<span id="vmVirtualMachineEvent_RequestShutdown"></span><span id="vmvirtualmachineevent_requestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_REQUESTSHUTDOWN"></span>**vmvirtualmachineevent \_ requestshutdown**
</dt> <dd>

Ein Herunterfahren wurde angefordert.

</dd> <dt>

<span id="vmVirtualMachineEvent_Reset"></span><span id="vmvirtualmachineevent_reset"></span><span id="VMVIRTUALMACHINEEVENT_RESET"></span>**vmvirtualmachineevent \_ Reset**
</dt> <dd>

Ein virtueller Computer wurde zurückgesetzt.

</dd> <dt>

<span id="vmVirtualMachineEvent_TripleFault"></span><span id="vmvirtualmachineevent_triplefault"></span><span id="VMVIRTUALMACHINEEVENT_TRIPLEFAULT"></span>**vmvirtualmachineevent-Auswert \_ Fehler**
</dt> <dd>

Ein virtueller Computer hat einen dreifachen Fehler verursacht.

</dd> <dt>

<span id="vmVirtualMachineEvent_HeartbeatStopped"></span><span id="vmvirtualmachineevent_heartbeatstopped"></span><span id="VMVIRTUALMACHINEEVENT_HEARTBEATSTOPPED"></span>**tabeatbeendete vmvirtualmachineevent \_**
</dt> <dd>

Der Takt einer VM wurde beendet. Dies weist normalerweise darauf hin, dass das Gast Betriebssystem abgestürzt ist.

</dd> <dt>

<span id="vmVirtualMachineEvent_ConfigurationChanged"></span><span id="vmvirtualmachineevent_configurationchanged"></span><span id="VMVIRTUALMACHINEEVENT_CONFIGURATIONCHANGED"></span>**vmvirtualmachineevent \_ configurationchanged**
</dt> <dd>

Ein Wert in der Konfiguration für diesen virtuellen Computer wurde geändert.

</dd> <dt>

<span id="vmVirtualMachineEvent_EnhancedVideoModeChanged"></span><span id="vmvirtualmachineevent_enhancedvideomodechanged"></span><span id="VMVIRTUALMACHINEEVENT_ENHANCEDVIDEOMODECHANGED"></span>**vmvirtualmachineevent \_ enhancedvideomode Changed**
</dt> <dd>

Der Videomodus eines virtuellen Computers wurde geändert.

</dd> <dt>

<span id="vmVirtualMachineEvent_AdditionsUninstalled"></span><span id="vmvirtualmachineevent_additionsuninstalled"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSUNINSTALLED"></span>**vmvirtualmachineevent \_ additionsuninstalliert**
</dt> <dd>

Integrations Komponenten wurden auf der VM deinstalliert.

</dd> <dt>

<span id="vmVirtualMachineEvent_AdditionsAvailable"></span><span id="vmvirtualmachineevent_additionsavailable"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSAVAILABLE"></span>**vmvirtualmachineevent \_ additionsavailable**
</dt> <dd>

Integration ist im Gast Betriebssystem verfügbar.

</dd> <dt>

<span id="vmVirtualMachineEvent_GuestShutdown"></span><span id="vmvirtualmachineevent_guestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_GUESTSHUTDOWN"></span>**vmvirtualmachineevent \_ guestshutdown**
</dt> <dd>

Ein Gast Betriebssystem wird heruntergefahren.

</dd> <dt>

<span id="vmVirtualMachineEvent_GuestLogoff"></span><span id="vmvirtualmachineevent_guestlogoff"></span><span id="VMVIRTUALMACHINEEVENT_GUESTLOGOFF"></span>**vmvirtualmachineevent \_ guestlogoff**
</dt> <dd>

Ein Benutzer hat sich vom Gast Betriebssystem abgemeldet.

</dd> <dt>

<span id="vmVirtualMachineEvent_DiskOutOfSpace"></span><span id="vmvirtualmachineevent_diskoutofspace"></span><span id="VMVIRTUALMACHINEEVENT_DISKOUTOFSPACE"></span>**vmvirtualmachineevent \_ diskouesleerraum**
</dt> <dd>

Für den virtuellen Computer ist wenig Speicherplatz auf dem Datenträger erforderlich.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmvirtualmachineevents**](ivmvirtualmachineevents.md)
</dt> </dl>

 

