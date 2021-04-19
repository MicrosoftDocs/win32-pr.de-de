---
description: Fordert an, dass der Status der Komponente der Gast Dienst Schnittstelle in den angegebenen Wert geändert wird.
ms.assetid: D9F7CD03-0D86-4005-A600-5CC7082A5047
title: 'Msvm_GuestServiceInterfaceComponent:: requestStateChange-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponent.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: de5689968d44277b01d6cb2256d41ddbbe573cd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362454"
---
# <a name="msvm_guestserviceinterfacecomponentrequeststatechange-method"></a>MSVM \_ guestserviceinterfacecomponent:: requestStateChange-Methode

Fordert an, dass der Status der Komponente der Gast Dienst Schnittstelle in den angegebenen Wert geändert wird.

## <a name="syntax"></a>Syntax


```C++
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Requestedstate* \[ in\]
</dt> <dd>

Typ: **UInt16**

Der neue Zustand. Die Informationen werden in der **requestedstate** -Eigenschaft der-Instanz abgelegt, wenn der Rückgabecode der **requestStateChange** -Methode 0 oder 4096 ist. Weitere Informationen finden Sie in der Beschreibung der Eigenschaften **enabledstate** und **requestedstate** für das-Element. Dabei muss es sich um einen der folgenden Werte handeln:

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Aktiviert** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deaktiviert** (3)


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

**Herunter** fahren (4)


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

**Offline** (6)


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

**Test** (7)


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

Zurück **stellen (8** )


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

Still **legung (9** )


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

**Neustart** (10)


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

**Zurücksetzen** (11)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserviert** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Anbieter reserviert** (32768.65535)


</dt> <dd></dd> </dl> </dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **CIM \_ bettejob**](/previous-versions//cc136808(v=vs.85))**

Ein optionaler Verweis auf ein [**MSVM-" \_ concretejob**](msvm-concretejob.md) "-Objekt, das zurückgegeben wird, wenn der Vorgang asynchron ausgeführt wird. Falls vorhanden, kann der zurückgegebene Verweis zum Überwachen des Fortschritts und zum Abrufen des Ergebnisses der Methode verwendet werden.

</dd> <dt>

*Timeoutperiod* \[ in\]
</dt> <dd>

Type: **DateTime**

Ein Timeout Zeitraum, der die maximale Zeitspanne angibt, die der Client für den Übergang in den neuen Zustand erwartet. Das Intervall Format muss zum Angeben des Timeout Zeitraums verwendet werden. Der Wert 0 oder **null** zeigt an, dass der Client keine Zeitanforderungen für den Übergang hat. Wenn diese Eigenschaft nicht 0 oder **null** enthält und die Implementierung diesen Parameter nicht unterstützt, muss der Rückgabecode 4098 (**use of Timeout Parameter not supported**) zurückgegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Werte zurück.



| Rückgabecode/-wert                                                                                                                                                                       | BESCHREIBUNG         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt> </dl>                           | Erfolg.<br/> |
| <dl> <dt>**Nicht unterstützt**</dt> <dt>1</dt> </dl>                                     |                     |
| <dl> <dt>**Unbekannter/nicht**</dt> angegebener Fehler <dt>2</dt> </dl>                         |                     |
| <dl> <dt>**Kann nicht innerhalb des Timeout Zeitraums**</dt> <dt>3</dt> beendet werden. </dl>            |                     |
| <dl> <dt></dt> Fehler <dt>4</dt> </dl>                                            |                     |
| <dl> <dt>**Ungültiger Parameter**</dt> <dt>5</dt> </dl>                                 |                     |
| <dl> <dt>**In Verwendung**</dt> <dt>6</dt> </dl>                                            |                     |
| <dl> <dt>**DMTF reserviert**</dt> <dt>..</dt> </dl>                                    |                     |
| <dl> Über <dt>**prüfte Methoden Parameter-der Übergang**</dt> wurde <dt>4096</dt> gestartet. </dl> |                     |
| <dl> <dt>**Ungültiger Status Übergang**</dt> <dt>4097</dt> </dl>                       |                     |
| <dl> <dt>**Verwendung des timeout-Parameters wird nicht unterstützt**</dt> <dt>4098</dt> </dl>         |                     |
| <dl> <dt>**Ausgelastet**</dt> <dt>4099</dt> </dl>                                           |                     |
| <dl> <dt>**Methode reserviert**</dt> <dt>4100.32767</dt> </dl>                         |                     |
| <dl> <dt>**Hersteller spezifischer**</dt> <dt>32768.. 65535</dt> </dl>                        |                     |



 

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

[**MSVM \_ guestserviczuterfacecomponent**](msvm-guestserviceinterfacecomponent.md)
</dt> </dl>

 

