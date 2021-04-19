---
title: Vmvmstate-Enumeration (vpccominterfaces. h)
description: Gibt den Status einer virtuellen Maschine an.
ms.assetid: 952dab9d-3d38-4cc5-ab75-4ee5096f7923
keywords:
- Vmvmstate-Enumeration virtueller PC
topic_type:
- apiref
api_name:
- VMVMState
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45505e4fb4b444b15697afca4576e889f2da9a6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339586"
---
# <a name="vmvmstate-enumeration"></a>Vmvmstate-Enumeration

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Gibt den Status einer virtuellen Maschine an.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  vmVMState_Invalid        = 0,
  vmVMState_TurnedOff      = 1,
  vmVMState_Saved          = 2,
  vmVMState_TurningOn      = 3,
  vmVMState_Restoring      = 4,
  vmVMState_Running        = 5,
  vmVMState_Paused         = 6,
  vmVMState_Saving         = 7,
  vmVMState_TurningOff     = 8,
  vmVMState_MergingDrives  = 9,
  vmVMState_DeleteMachine  = 10
} VMVMState;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="vmVMState_Invalid"></span><span id="vmvmstate_invalid"></span><span id="VMVMSTATE_INVALID"></span>**vmvmstate ist \_ ungültig.**
</dt> <dd>

Ungültiger Status (sollte nicht auftreten, wenn der virtuelle Computer vorhanden ist).

</dd> <dt>

<span id="vmVMState_TurnedOff"></span><span id="vmvmstate_turnedoff"></span><span id="VMVMSTATE_TURNEDOFF"></span>**vmvmstate \_ turnetdoff**
</dt> <dd>

Off und nicht gespeichert.

</dd> <dt>

<span id="vmVMState_Saved"></span><span id="vmvmstate_saved"></span><span id="VMVMSTATE_SAVED"></span>**vmvmstate wurde \_ gespeichert.**
</dt> <dd>

Aus, aber der Gast wird gespeichert.

</dd> <dt>

<span id="vmVMState_TurningOn"></span><span id="vmvmstate_turningon"></span><span id="VMVMSTATE_TURNINGON"></span>**vmvmstate- \_ turningon**
</dt> <dd>

Beim Einschalten.

</dd> <dt>

<span id="vmVMState_Restoring"></span><span id="vmvmstate_restoring"></span><span id="VMVMSTATE_RESTORING"></span>**vmvmstate- \_ Wiederherstellung**
</dt> <dd>

Der Zustand wird wieder hergestellt.

</dd> <dt>

<span id="vmVMState_Running"></span><span id="vmvmstate_running"></span><span id="VMVMSTATE_RUNNING"></span>**vmvmstate wird \_ ausgeführt**
</dt> <dd>

Wird ausgeführt und nicht angehalten.

</dd> <dt>

<span id="vmVMState_Paused"></span><span id="vmvmstate_paused"></span><span id="VMVMSTATE_PAUSED"></span>**vmvmstate \_ angehalten**
</dt> <dd>

Wird ausgeführt und angehalten.

</dd> <dt>

<span id="vmVMState_Saving"></span><span id="vmvmstate_saving"></span><span id="VMVMSTATE_SAVING"></span>**Speichern von vmvmstate \_**
</dt> <dd>

Der Zustand wird gespeichert.

</dd> <dt>

<span id="vmVMState_TurningOff"></span><span id="vmvmstate_turningoff"></span><span id="VMVMSTATE_TURNINGOFF"></span>**vmvmstate ( \_ turningoff)**
</dt> <dd>

Beim Ausschalten.

</dd> <dt>

<span id="vmVMState_MergingDrives"></span><span id="vmvmstate_mergingdrives"></span><span id="VMVMSTATE_MERGINGDRIVES"></span>**vmvmstate- \_ mergingdrives**
</dt> <dd>

Beim Zusammenführen von rückgängig-Laufwerken.

</dd> <dt>

<span id="vmVMState_DeleteMachine"></span><span id="vmvmstate_deletemachine"></span><span id="VMVMSTATE_DELETEMACHINE"></span>**vmvmstate \_ deletemachine**
</dt> <dd>

Der virtuelle Computer wird gelöscht.

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

[**Ivmvirtualmachine:: State**](ivmvirtualmachine-state.md)
</dt> <dt>

[**Ivmvirtualmachineevents:: OnStateChange**](ivmvirtualmachineevents-onstatechange.md)
</dt> <dt>

[**Ivmvirtualpcevents:: onvmstatechange**](ivmvirtualpcevents-onvmstatechange.md)
</dt> </dl>

 

