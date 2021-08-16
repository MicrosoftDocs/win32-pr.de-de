---
description: RequestStateChange-Methode der Msvm_Ps2Mouse - Fordert eine Zustandsänderung an.
ms.assetid: a61c17a8-f89d-47aa-8c4f-46ccf478103e
title: RequestStateChange-Methode der Msvm_Ps2Mouse-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 28136033b3c43c49f127ecd59a79bb85d96a0f341d7c9f8f8f1e7c664e419cb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148263"
---
# <a name="requeststatechange-method-of-the-msvm_ps2mouse-class"></a>RequestStateChange-Methode der Msvm \_ Ps2Mouse-Klasse

Fordert eine Zustandsänderung an.

## <a name="syntax"></a>Syntax


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*RequestedState* \[ In\]
</dt> <dd>

Der für das Element angeforderte Zustand. Diese Informationen werden in die RequestedState-Eigenschaft der -Instanz platziert, wenn der Rückgabecode der RequestStateChange-Methode 0 ('Completed with No Error') oder 4096 (0x1000) ('Job Started') ist. Ausführliche Erläuterungen zu den RequestedState-Werten finden Sie in der Beschreibung der Eigenschaften EnabledState und RequestedState.

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Aktiviert** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deaktiviert** (3)


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

**Herunterfahren** (4)


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

**Offline** (6)


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

**Test** (7)


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

**Zurückern** (8)


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

**Ruhe** (9)


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

**Neustart** (10)


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

**Zurücksetzen** (11)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reserved** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Reservierter Anbieter** (32768..65535)


</dt> <dd></dd> </dl> </dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Kann einen Verweis auf den ConcreteJob enthalten, der zum Nachverfolgen des Zustandsübergangs erstellt wurde, der durch den Methodenaufruf initiiert wurde.

</dd> <dt>

*TimeoutPeriod* \[ In\]
</dt> <dd>

Ein Timeoutzeitraum, der die maximale Zeitspanne angibt, die der Client für den Übergang in den neuen Zustand erwartet. Das Intervallformat muss verwendet werden, um timeoutPeriod anzugeben. Der Wert 0 oder ein NULL-Parameter gibt an, dass der Client keine Zeitanforderungen für den Übergang hat.

Wenn diese Eigenschaft nicht 0 oder NULL enthält und die Implementierung diesen Parameter nicht unterstützt, wird der Rückgabecode "Use Of Timeout Parameter Not Supported" zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück:

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ Ps2Mouse**](msvm-ps2mouse.md)
</dt> </dl>

 

 




