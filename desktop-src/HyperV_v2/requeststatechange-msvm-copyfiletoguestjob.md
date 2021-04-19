---
description: Ändert den Status des Auftrags.
ms.assetid: 3B11CE45-63E4-43D1-AAF6-02F83C9CBB85
title: 'Msvm_CopyFileToGuestJob:: requestStateChange-Methode'
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
ms.openlocfilehash: adf5d866989f3b3518cf53b52e073239e023e3c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349947"
---
# <a name="msvm_copyfiletoguestjobrequeststatechange-method"></a>MSVM \_ copyfiletoguestjob:: requestStateChange-Methode

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

*Requestedstate* \[ in\]
</dt> <dd>

Der neue Zustand. Dies sind die möglichen Werte:

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)


</dt> <dd>

Ändert den Zustand in "wird ausgeführt".

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Aussetzen** (3)


</dt> <dd>

Beendet den Auftrag vorübergehend. Anschließend kann der Client den Auftrag mit "Start" neu starten. Der Client kann möglicherweise den Zustand "Dienst" eingeben, während er angehalten wird (Dies ist Auftrags spezifisch).

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Beenden** (4)


</dt> <dd>

Beendet den Auftrag ordnungsgemäß, speichert Daten, behält den Zustand bei und schließt alle zugrunde liegenden Prozesse ordnungsgemäß herunter.

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)


</dt> <dd>

Beendet den Auftrag sofort, ohne dass es erforderlich ist, Daten zu speichern oder den Zustand beizubehalten.

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Dienst** (6)


</dt> <dd>

Versetzt den Auftrag in einen herstellerspezifischen Dienst Zustand. Der Client kann den Auftrag möglicherweise neu starten.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (7.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (32768.65535)


</dt> <dd></dd> </dl> </dd> <dt>

*Timeoutperiod* \[ in\]
</dt> <dd>

Ein Timeout Zeitraum, der die maximale Zeitspanne angibt, die der Client für den Übergang in den neuen Zustand erwartet. Das Intervall Format muss zum Angeben des Timeout Zeitraums verwendet werden. Der Wert 0 oder **null** zeigt an, dass der Client keine Zeitanforderungen für den Übergang hat. Wenn diese Eigenschaft nicht 0 oder **null** enthält und die Implementierung diesen Parameter nicht unterstützt, muss der Rückgabecode 4098 (**use of Timeout Parameter not supported**) zurückgegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.



| Rückgabecode/-wert                                                                                                                                                               | BESCHREIBUNG                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt> </dl>                   | Erfolg.<br/>                                                                |
| <dl> <dt>**Verwendung des timeout-Parameters wird nicht unterstützt**</dt> <dt>4098</dt> </dl> |                                                                                    |
| <dl> <dt></dt> Fehler <dt>32768</dt> </dl>                                |                                                                                    |
| <dl> <dt>**Zugriff verweigert**</dt> <dt>32769</dt> </dl>                         | Zugriff verweigert.<br/>                                                          |
| <dl> <dt>**Nicht unterstützt**</dt> <dt>32770</dt> </dl>                         |                                                                                    |
| <dl> <dt>**Status ist unbekannt**</dt> <dt>32771</dt> </dl>                     |                                                                                    |
| <dl> <dt>**Timeout**</dt> <dt>32772</dt> </dl>                               |                                                                                    |
| <dl> <dt>**Ungültiger Parameter**</dt> <dt>32773</dt> </dl>                     |                                                                                    |
| <dl> <dt>**System wird verwendet**</dt> <dt>32774</dt> </dl>                      |                                                                                    |
| <dl> <dt>**Ungültiger Status für diesen Vorgang**</dt> <dt>32775</dt> </dl>      | Der im *requestedstate* -Parameter angegebene Wert wird nicht unterstützt.<br/> |
| <dl> <dt>**Falscher Datentyp**</dt> <dt>32776</dt> </dl>                   |                                                                                    |
| <dl> <dt>**System ist nicht verfügbar**</dt> <dt>32777</dt> </dl>               |                                                                                    |
| <dl> <dt>**Nicht genügend Arbeitsspeicher**</dt> <dt>32778</dt> </dl>                         |                                                                                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\\\\\Stammvirtualisierung \\ v2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ copyfilein guestjob**](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

 




