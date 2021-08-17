---
title: VMShutdownAction-Enumeration (VPCCOMInterfaces.h)
description: Gibt an, wie ein virtueller Computer heruntergefahren wird, wenn der Host heruntergefahren wird oder der vpc.exe Prozess beendet wird.
ms.assetid: 271a685a-cac9-4a15-b363-bf8873fd5324
keywords:
- VMShutdownAction-Enumeration Virtueller PC
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
ms.openlocfilehash: df1f8b5bc21021e7771c14c0c3c6399e1d6342d7ebe3803759c8adb5c45024cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119248410"
---
# <a name="vmshutdownaction-enumeration"></a>VMShutdownAction-Enumeration

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Gibt an, wie ein virtueller Computer (VM) heruntergefahren wird, wenn der Host heruntergefahren oder der vpc.exe Prozess beendet wird.

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

<span id="vmShutdownAction_Save"></span><span id="vmshutdownaction_save"></span><span id="VMSHUTDOWNACTION_SAVE"></span>**vmShutdownAction \_ Save**
</dt> <dd>

Speichern Sie den VM-Status.

</dd> <dt>

<span id="vmShutdownAction_TurnOff"></span><span id="vmshutdownaction_turnoff"></span><span id="VMSHUTDOWNACTION_TURNOFF"></span>**vmShutdownAction \_ TurnOff**
</dt> <dd>

Deaktivieren Sie den virtuellen Computer, ohne die Laufwerke rückgängig zu machen.

</dd> <dt>

<span id="vmShutdownAction_Shutdown"></span><span id="vmshutdownaction_shutdown"></span><span id="VMSHUTDOWNACTION_SHUTDOWN"></span>**vmShutdownAction \_ Shutdown**
</dt> <dd>

Fahren Sie das Gastbetriebssystem auf dem virtuellen Computer herunter, ohne die Laufwerke rückgängig zu macht, wenn die Integrationskomponenten verfügbar sind, und speichern Sie die VM andernfalls.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Windows Enumerationen virtueller PCs](virtual-pc-enumerations.md)
</dt> <dt>

[**IVMVirtualMachine::ShutdownActionOnQuit**](ivmvirtualmachine-shutdownactiononquit.md)
</dt> </dl>

 

