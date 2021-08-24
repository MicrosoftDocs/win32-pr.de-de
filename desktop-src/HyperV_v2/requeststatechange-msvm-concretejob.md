---
description: Fordert an, dass der Status des Auftrags in den angegebenen Zustand geändert wird.
ms.assetid: 5D7D7D20-4BB9-4375-BBBF-7AA64FEE6D13
title: RequestStateChange-Methode der Msvm_ConcreteJob Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 579ad52bd83bd43dc3071f704914eb7b5f9cae4f0be89f018e56b9608b1c12be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501130"
---
# <a name="requeststatechange-method-of-the-msvm_concretejob-class"></a>RequestStateChange-Methode der Msvm \_ ConcreteJob-Klasse

Fordert an, dass der Status des Auftrags in den angegebenen Zustand geändert wird. Das mehrfache Aufrufen **der RequestStateChange-Methode** kann dazu führen, dass frühere Anforderungen überschrieben oder verloren gehen. Wenn 0 zurückgegeben wird, wurde die Aufgabe erfolgreich abgeschlossen. Jeder andere Rückgabecode gibt einen Fehlerzustand an.

## <a name="syntax"></a>Syntax


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*RequestedState* \[ In\]
</dt> <dd>

Typ: **uint16**

Der neue Zustand eines Auftrags.

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)


</dt> <dd>

Ändert den Status in "Wird ausgeführt".

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)


</dt> <dd>

Beendet den Auftrag vorübergehend. Anschließend soll der Auftrag mit "Start" neu gestartet werden. Es kann möglich sein, den Status "Dienst" zu erhalten, während er angehalten wird. (Dies ist auftragsspezifisch.)

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)


</dt> <dd>

Beendet den Auftrag sauber, wobei Daten gespeichert, der Zustand beibehalten und alle zugrunde liegenden Prozesse in einer geordneten Weise heruntergefahren werden.

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)


</dt> <dd>

Beendet den Auftrag sofort, ohne dass Daten gespeichert oder der Zustand beibehalten werden muss.

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Dienst** (6)


</dt> <dd>

Versetzt den Auftrag in einen anbieterspezifischen Dienststatus. Möglicherweise ist es möglich, den Auftrag neu zu starten.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved**


</dt> <dd>

Reserviert.

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Reservierter Anbieter**


</dt> <dd>

Reserviert.

</dd> </dl> </dd> <dt>

*TimeoutPeriod* \[ In\]
</dt> <dd>

Typ: **datetime**

Ein Timeoutzeitraum, der die maximale Zeitspanne angibt, die der Client für den Übergang in den neuen Zustand erwartet. Das Intervallformat muss verwendet werden, um den Timeoutzeitraum anzugeben. Der Wert 0 oder **NULL gibt an,** dass der Client keine Zeitanforderungen für den Übergang hat. Wenn diese Eigenschaft nicht 0 oder **NULL** enthält und die Implementierung diesen Parameter nicht unterstützt, muss der Rückgabecode 4098 (Use Of Timeout Parameter Not Supported) zurückgegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

**Unbekannter/nicht angegebener Fehler** (2)
</dt> <dt>

**Innerhalb des Timeoutzeitraums** (3) kann nicht abgeschlossen werden.
</dt> <dt>

**Fehler** (4)
</dt> <dt>

**Ungültiger Parameter** (5)
</dt> <dt>

**Wird verwendet** (6)
</dt> <dt>

**DMTF Reserved** (7 4095)
</dt> <dt>

**Überprüfte Methodenparameter – Übergang gestartet** (4096)
</dt> <dt>

**Ungültiger Zustandsübergang** (4097)
</dt> <dt>

**Verwendung des Timeoutparameters nicht unterstützt** (4098)
</dt> <dt>

**Ausgelastet** (4099)
</dt> <dt>

**Reservierte Methode** (4100 32767)
</dt> <dt>

**Herstellerspezifisch** (32768 65535)
</dt> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die [**Msvm \_ ConcreteJob-Klasse**](msvm-concretejob.md) kann durch UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ ConcreteJob**](msvm-concretejob.md)
</dt> </dl>

 

