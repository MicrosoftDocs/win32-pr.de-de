---
description: Ändert den Status des Auftrags.
ms.assetid: 3B11CE45-63E4-43D1-AAF6-02F83C9CBB85
title: Msvm_CopyFileToGuestJob::RequestStateChange-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 09fdc3a1ee7d0f8942e1e02c5d18f20c42f74db2e65ae065132f164b199ee861
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014338"
---
# <a name="msvm_copyfiletoguestjobrequeststatechange-method"></a>Msvm \_ CopyFileToGuestJob::RequestStateChange-Methode

Ändert den Status des Auftrags.

## <a name="syntax"></a>Syntax


```C++
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*RequestedState* \[ In\]
</dt> <dd>

Der neue Zustand. Dies sind die möglichen Werte:

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)


</dt> <dd>

Ändert den Status in "Wird ausgeführt".

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)


</dt> <dd>

Beendet den Auftrag vorübergehend. Anschließend kann der Client den Auftrag mit "Start" neu starten. Der Client kann möglicherweise den Status "Dienst" eingeben, während er angehalten wird (dies ist auftragsspezifisch).

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

Versetzt den Auftrag in einen anbieterspezifischen Dienststatus. Der Client kann den Auftrag möglicherweise neu starten.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Reservierter Anbieter** (32768..65535)


</dt> <dd></dd> </dl> </dd> <dt>

*TimeoutPeriod* \[ In\]
</dt> <dd>

Ein Timeoutzeitraum, der die maximale Zeitspanne angibt, die der Client für den Übergang in den neuen Zustand erwartet. Das Intervallformat muss verwendet werden, um den Timeoutzeitraum anzugeben. Der Wert 0 oder **NULL gibt an,** dass der Client keine Zeitanforderungen für den Übergang hat. Wenn diese Eigenschaft nicht 0 oder **NULL** enthält und die Implementierung diesen Parameter nicht unterstützt, muss der Rückgabecode 4098 (**Use Of Timeout Parameter Not Supported**) zurückgegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.



| Rückgabecode/-wert                                                                                                                                                               | Beschreibung                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt> </dl>                   | Erfolg.<br/>                                                                |
| <dl> <dt>**Verwendung des Timeoutparameters wird nicht unterstützt**</dt> <dt>4098</dt> </dl> |                                                                                    |
| <dl> <dt>**Fehler**</dt> <dt>32768</dt> </dl>                                |                                                                                    |
| <dl> <dt>**Zugriff verweigert**</dt> <dt>32769</dt> </dl>                         | Zugriff verweigert:<br/>                                                          |
| <dl> <dt>**Nicht unterstützt**</dt> <dt>32770</dt> </dl>                         |                                                                                    |
| <dl> <dt>**Der Status ist unbekannt**</dt> <dt>32771.</dt> </dl>                     |                                                                                    |
| <dl> <dt>**Timeout**</dt> <dt>32772</dt> </dl>                               |                                                                                    |
| <dl> <dt>**Ungültiger Parameter**</dt> <dt>32773</dt> </dl>                     |                                                                                    |
| <dl> <dt>**System wird verwendet**</dt> <dt>32774</dt> </dl>                      |                                                                                    |
| <dl> <dt>**Ungültiger Zustand für diesen Vorgang**</dt> <dt>32775</dt> </dl>      | Der im *RequestedState-Parameter angegebene* Wert wird nicht unterstützt.<br/> |
| <dl> <dt>**Falscher Datentyp**</dt> <dt>32776</dt> </dl>                   |                                                                                    |
| <dl> <dt>**System ist nicht verfügbar**</dt> <dt>32777</dt> </dl>               |                                                                                    |
| <dl> <dt>**Nicht genügend Arbeitsspeicher**</dt> <dt>32778</dt> </dl>                         |                                                                                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\\\Root \\ Virtualization \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ CopyFileToGuestJob**](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

 




