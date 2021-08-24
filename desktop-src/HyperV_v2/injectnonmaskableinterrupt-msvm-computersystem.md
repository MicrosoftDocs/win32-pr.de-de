---
description: Fügt einen nicht maskierbaren Interrupt in den virtuellen Computer ein.
ms.assetid: 897AD1B9-0EDD-4DCE-963D-D5DE03AF55A9
title: Msvm_ComputerSystem::InjectNonMaskableInterrupt-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.InjectNonMaskableInterrupt
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e9019492299d03b31001b60934e00dc40c41b4328e4809fe8e864ef378c30a89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694440"
---
# <a name="msvm_computersysteminjectnonmaskableinterrupt-method"></a>Msvm \_ ComputerSystem::InjectNonMaskableInterrupt-Methode

Fügt einen nicht maskierbaren Interrupt in den virtuellen Computer ein.

## <a name="syntax"></a>Syntax


```C++
uint32 InjectNonMaskableInterrupt(
  [out] CIM_ConcreteJob Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)) abgeleitet wurde, um den Status der Interruptinjektion nachzuverfolgung. Dieser Verweis kann NULL **sein,** wenn die Aufgabe abgeschlossen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Überprüfte Methodenparameter – Auftrag gestartet** (4096)
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\\\Root \\ Virtualization \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ ComputerSystem**](msvm-computersystem.md)
</dt> </dl>

 

