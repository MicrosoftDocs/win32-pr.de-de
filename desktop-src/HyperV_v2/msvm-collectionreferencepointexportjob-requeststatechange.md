---
description: Fordert eine Statusänderung an.
ms.assetid: 34d70ff2-4545-4ab7-8c84-6532c342768b
title: RequestStateChange-Methode der Msvm_CollectionReferencePointExportJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a3e8b3f3a7249896f023734d049fa3fa772514f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353914"
---
# <a name="requeststatechange-method-of-the-msvm_collectionreferencepointexportjob-class"></a>RequestStateChange-Methode der MSVM \_ collectionreferencepointexportjob-Klasse

Fordert eine Statusänderung an.

## <a name="syntax"></a>Syntax


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Requestedstate* \[ in\]
</dt> <dd>

RequestStateChange ändert den Status eines Auftrags. Die folgenden Werte sind möglich:

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)


</dt> <dd>

Ändert den Zustand in "wird ausgeführt".

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Aussetzen** (3)


</dt> <dd>

Beendet den Auftrag vorübergehend. Die Absicht besteht darin, den Auftrag mit "Start" neu zu starten. Möglicherweise ist es möglich, den Zustand "Dienst" in den Status "angehalten" einzugeben. (Dies ist Auftrags spezifisch.)

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Beenden** (4)


</dt> <dd>

Beendet den Auftrag ordnungsgemäß, speichert Daten, behält den Zustand bei und fährt alle zugrunde liegenden Prozesse ordnungsgemäß herunter.

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)


</dt> <dd>

Beendet den Auftrag sofort, ohne dass es erforderlich ist, Daten zu speichern oder den Zustand beizubehalten.

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Dienst** (6)


</dt> <dd>

Versetzt den Auftrag in einen herstellerspezifischen Dienst Zustand. Möglicherweise ist es möglich, den Auftrag neu zu starten.

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

Gibt bei Erfolg 0 zurück. Andernfalls wird einer der folgenden Fehler zurückgegeben.

<dl> <dt>

  (0)
</dt> <dt>

 (32768)
</dt> <dt>

 (32769)
</dt> <dt>

 (32770)
</dt> <dt>

 (32771)
</dt> <dt>

 (32772)
</dt> <dt>

 (32773)
</dt> <dt>

 (32774)
</dt> <dt>

 (32775)
</dt> <dt>

 (32776)
</dt> <dt>

 (32777)
</dt> <dt>

 (32778)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1703, \[ nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ collectionreferencepointexportjob**](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 




