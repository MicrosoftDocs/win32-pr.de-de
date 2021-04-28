---
description: 'RequestStateChange-Methode der Msvm_CollectionReferencePointExportJob-Klasse: Fordert eine Zustandsänderung an.'
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
ms.openlocfilehash: 84956e206654de022c3151aa5a442651f9c2375a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119238"
---
# <a name="requeststatechange-method-of-the-msvm_collectionreferencepointexportjob-class"></a>RequestStateChange-Methode der Msvm \_ CollectionReferencePointExportJob-Klasse

Fordert eine Zustandsänderung an.

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

RequestStateChange ändert den Status eines Auftrags. Die folgenden Werte sind möglich:

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)


</dt> <dd>

Ändert den Status in "Wird ausgeführt".

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Anhalten** (3)


</dt> <dd>

Beendet den Auftrag vorübergehend. Die Absicht besteht darin, den Auftrag anschließend mit "Start" neu zu starten. Es kann möglich sein, den Status "Dienst" zu erhalten, während er angehalten wird. (Dies ist auftragsspezifisch.)

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)


</dt> <dd>

Beendet den Auftrag ordnungsgemäß, speichert Daten, behält den Zustand bei und fährt alle zugrunde liegenden Prozesse ordnungsgemäß herunter.

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)


</dt> <dd>

Beendet den Auftrag sofort, ohne dass Daten gespeichert oder der Zustand beibehalten werden muss.

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Dienst** (6)


</dt> <dd>

Versetzt den Auftrag in einen anbieterspezifischen Dienststatus. Möglicherweise kann der Auftrag neu gestartet werden.

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

Gibt bei Erfolg 0 zurück. andernfalls gibt einen der folgenden Fehler zurück.

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



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1703 desktop apps only (Nur \[ Desktop-Apps der Version 1703)\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ CollectionReferencePointExportJob**](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 




