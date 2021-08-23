---
description: Fordert an, dass der Zustand des Elements geändert wird.
ms.assetid: D1742588-D932-4FE1-8D2A-E410BEE371FF
title: RequestStateChange-Methode der Msvm_Keyboard Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 457ed1e98714a2a20169fd1139b7f42475e5d893756591930b6a25147f756897
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119522240"
---
# <a name="requeststatechange-method-of-the-msvm_keyboard-class"></a>RequestStateChange-Methode der Msvm \_ Keyboard-Klasse

Fordert an, dass der Zustand des Elements geändert wird.

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

Der für das Element angeforderte neue Zustand. Diese Informationen werden in die **RequestedState-Eigenschaft** der Instanz platziert, wenn der Rückgabecode 0 ('Completed with No Error'), 3 ('Timeout') oder 4096 (0x1000) ('Job Started') ist. Ausführliche Erläuterungen zu den *RequestedState-Werten* finden Sie in der Beschreibung der **Eigenschaften EnabledState** **und RequestedState.**

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

**Anbieter reserviert** (32768..65535)


</dt> <dd></dd> </dl> </dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Ein Verweis auf den Auftrag. Dieser Parameter kann NULL **sein,** wenn die Aufgabe abgeschlossen ist.

</dd> <dt>

*TimeoutPeriod* \[ In\]
</dt> <dd>

Die maximale Zeitdauer, die der Client für den Übergang in den neuen Zustand erwartet. Das Intervallformat muss verwendet werden, um diesen Time out-Zeitraum anzugeben. Der Wert 0 oder **NULL gibt an,** dass der Client keine Zeitanforderungen für den Übergang hat. Wenn diese Eigenschaft nicht 0 oder **NULL** enthält und die Implementierung diesen Parameter nicht unterstützt, wird der Rückgabecode 4098 ("Use Of Timeout Parameter Not Supported") zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

**Unbekannter oder nicht angegebener Fehler** (2)
</dt> <dt>

**Innerhalb des Timeoutzeitraums** (3) kann nicht abgeschlossen werden.
</dt> <dt>

**Fehler** (4)
</dt> <dt>

**Ungültiger Parameter** (5)
</dt> <dt>

**Wird verwendet** (6)
</dt> <dt>

**DMTF Reserved** (..)
</dt> <dt>

**Überprüfte Methodenparameter – Auftrag gestartet** (4096)
</dt> <dt>

**Ungültiger Zustandsübergang** (4097)
</dt> <dt>

**Verwendung des Timeoutparameters nicht unterstützt** (4098)
</dt> <dt>

**Ausgelastet** (4099)
</dt> <dt>

**Reservierte Methode** (4100...32767)
</dt> <dt>

**Herstellerspezifisch** (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm-Tastatur \_**](msvm-keyboard.md)
</dt> </dl>

 

 




