---
description: Fordert an, dass der Status des Auftrags in den angegebenen Zustand geändert wird.
ms.assetid: 5D7D7D20-4BB9-4375-BBBF-7AA64FEE6D13
title: RequestStateChange-Methode der Msvm_ConcreteJob-Klasse
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
ms.openlocfilehash: 0e7abf5f4bf78ac469e528ab72bb5786130e9cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359006"
---
# <a name="requeststatechange-method-of-the-msvm_concretejob-class"></a>RequestStateChange-Methode der MSVM- \_ Klasse "concretejob"

Fordert an, dass der Status des Auftrags in den angegebenen Zustand geändert wird. Wenn Sie die **requestStateChange** -Methode mehrmals aufrufen, kann dies dazu führen, dass frühere Anforderungen überschrieben werden oder verloren gehen. Wenn 0 zurückgegeben wird, wurde der Task erfolgreich abgeschlossen. Jeder andere Rückgabecode weist auf eine Fehlerbedingung hin.

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

Typ: **UInt16**

Der neue Status eines Auftrags.

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)


</dt> <dd>

Ändert den Zustand in "wird ausgeführt".

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Aussetzen** (3)


</dt> <dd>

Beendet den Auftrag vorübergehend. Die Absicht besteht darin, den Auftrag mit "Start" neu zu starten. Möglicherweise ist es möglich, den Status "Dienst" in den Status "angehalten" einzugeben. (Dies ist Auftrags spezifisch.)

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

Versetzt den Auftrag in einen herstellerspezifischen Dienst Zustand. Möglicherweise ist es möglich, den Auftrag neu zu starten.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert**


</dt> <dd>

Reserviert.

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert**


</dt> <dd>

Reserviert.

</dd> </dl> </dd> <dt>

*Timeoutperiod* \[ in\]
</dt> <dd>

Type: **DateTime**

Ein Timeout Zeitraum, der die maximale Zeitspanne angibt, die der Client für den Übergang in den neuen Zustand erwartet. Das Intervall Format muss zum Angeben des Timeout Zeitraums verwendet werden. Der Wert 0 oder **null** zeigt an, dass der Client keine Zeitanforderungen für den Übergang hat. Wenn diese Eigenschaft nicht 0 oder **null** enthält und die Implementierung diesen Parameter nicht unterstützt, muss der Rückgabecode 4098 (Use of Timeout Parameter not supported) zurückgegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

**Unbekannter/nicht** angegebener Fehler (2)
</dt> <dt>

**Kann nicht innerhalb des Timeout Zeitraums** (3) beendet werden.
</dt> <dt>

Fehler **(4** )
</dt> <dt>

**Ungültiger Parameter** (5)
</dt> <dt>

**In Gebrauch** (6)
</dt> <dt>

**DMTF reserviert** (7 4095)
</dt> <dt>

Über **prüfte Methoden Parameter-der Übergang wurde gestartet** (4096).
</dt> <dt>

**Ungültiger Status Übergang** (4097).
</dt> <dt>

**Verwendung des timeout-Parameters wird nicht unterstützt** (4098)
</dt> <dt>

**Ausgelastet** (4099)
</dt> <dt>

**Reservierte Methode** (4100 32767)
</dt> <dt>

**Hersteller spezifisch** (32768 65535)
</dt> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die [**MSVM-Klasse " \_ concretejob**](msvm-concretejob.md) " kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM- \_ concretejob**](msvm-concretejob.md)
</dt> </dl>

 

