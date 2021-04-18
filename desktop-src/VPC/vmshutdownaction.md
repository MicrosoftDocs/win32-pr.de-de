---
title: Vmshutdownaction-Enumeration (vpccominterfaces. h)
description: Gibt an, wie eine virtuelle Maschine heruntergefahren wird, wenn der Host heruntergefahren oder der vpc.exe Prozess beendet wird.
ms.assetid: 271a685a-cac9-4a15-b363-bf8873fd5324
keywords:
- Vmshutdownaction-Enumeration virtueller PC
topic_type:
- apiref
api_name:
- VMShutdownAction
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b939954042a446f7ad9f128580e804d73e9d29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341381"
---
# <a name="vmshutdownaction-enumeration"></a>Vmshutdownaction-Enumeration

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Gibt an, wie eine virtuelle Maschine (VM) heruntergefahren wird, wenn der Host heruntergefahren oder der vpc.exe Prozess beendet wird.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  vmShutdownAction_Save      = 0,
  vmShutdownAction_TurnOff   = 1,
  vmShutdownAction_Shutdown  = 2
} VMShutdownAction;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="vmShutdownAction_Save"></span><span id="vmshutdownaction_save"></span><span id="VMSHUTDOWNACTION_SAVE"></span>**vmshutdownaction \_ Speichern**
</dt> <dd>

Speichern Sie den VM-Status.

</dd> <dt>

<span id="vmShutdownAction_TurnOff"></span><span id="vmshutdownaction_turnoff"></span><span id="VMSHUTDOWNACTION_TURNOFF"></span>**vmshutdownaction- \_ Abzweigung**
</dt> <dd>

Schalten Sie die VM aus, ohne die Laufwerke abzumachen.

</dd> <dt>

<span id="vmShutdownAction_Shutdown"></span><span id="vmshutdownaction_shutdown"></span><span id="VMSHUTDOWNACTION_SHUTDOWN"></span>**vmshutdownaction wird \_ heruntergefahren**
</dt> <dd>

Fahren Sie das Gast Betriebssystem auf dem virtuellen Computer herunter, ohne die Laufwerke abzumachen, wenn die Integrations Komponenten verfügbar sind, und speichern Sie andernfalls die VM.

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

[Windows Virtual PC-Enumerationen](virtual-pc-enumerations.md)
</dt> <dt>

[**Ivmvirtualmachine:: shutdownaktiononquit**](ivmvirtualmachine-shutdownactiononquit.md)
</dt> </dl>

 

