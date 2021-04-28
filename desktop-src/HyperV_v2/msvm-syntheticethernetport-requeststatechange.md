---
description: 'RequestStateChange-Methode der Msvm_SyntheticEthernetPort Klasse : Fordert eine Zustandsänderung an.'
ms.assetid: 9aea3a8e-8b62-48c3-bbdb-49f24aeeca22
title: RequestStateChange-Methode der Msvm_SyntheticEthernetPort Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticEthernetPort.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7a751ba40be7ddeb6d71f104036487dd8acb209a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111308"
---
# <a name="requeststatechange-method-of-the-msvm_syntheticethernetport-class"></a>RequestStateChange-Methode der Msvm \_ SyntheticEthernetPort-Klasse

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

Der neue Zustand. Die Informationen werden in der **RequestedState-Eigenschaft** der -Instanz platziert, wenn der Rückgabecode der **RequestStateChange-Methode** 0 (Auftrag ohne Fehler abgeschlossen) oder 4096 (Auftrag gestartet) ist. Weitere Informationen finden Sie in der Beschreibung der **Eigenschaften EnabledState** und **RequestedState** für das Element. Dies muss einer der folgenden Werte sein.

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

Kann einen Verweis auf den [**CIM \_ ConcreteJob**](cim-concretejob.md) enthalten, der erstellt wurde, um den zustandsübergang zu verfolgen, der durch den Methodenaufruf initiiert wurde.

</dd> <dt>

*TimeoutPeriod* \[ In\]
</dt> <dd>

Ein Timeoutzeitraum, der die maximale Zeitspanne angibt, die der Client für den Übergang in den neuen Zustand erwartet. Das Intervallformat muss verwendet werden, um den Timeoutzeitraum anzugeben. Der Wert 0 oder **NULL gibt an,** dass der Client keine Zeitanforderungen für den Übergang hat. Wenn diese Eigenschaft nicht 0 oder **NULL** enthält und die Implementierung diesen Parameter nicht unterstützt, muss der Rückgabecode 4098 (**Use Of Timeout Parameter Not Supported**) zurückgegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück:

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ SyntheticEthernetPort**](msvm-syntheticethernetport.md)
</dt> </dl>

 

 




