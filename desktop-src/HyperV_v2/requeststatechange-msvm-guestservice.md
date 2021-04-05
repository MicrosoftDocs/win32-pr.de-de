---
description: Fordert an, dass der Zustand des Gast Diensts auf den angegebenen Wert geändert wird.
ms.assetid: F2853BB3-4074-431C-9E10-26AA0757FE99
title: 'Msvm_GuestService:: requestStateChange-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1360c36b58c96b7e621e5f339bd503ce4f1390b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757650"
---
# <a name="msvm_guestservicerequeststatechange-method"></a>MSVM \_ guestservice:: requestStateChange-Methode

Fordert an, dass der Zustand des Gast Diensts auf den angegebenen Wert geändert wird.

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

Ein optionaler Verweis auf ein CIM-" [**\_ concretejob**](cim-concretejob.md) "-Objekt, das zurückgegeben wird, wenn der Vorgang asynchron ausgeführt wird. Falls vorhanden, kann der zurückgegebene Verweis zum Überwachen des Fortschritts und zum Abrufen des Ergebnisses der Methode verwendet werden.

</dd> <dt>

*Timeoutperiod* \[ in\]
</dt> <dd>

Ein Timeout Zeitraum, der die maximale Zeitspanne angibt, die der Client für den Übergang in den neuen Zustand erwartet. Das Intervall Format muss zum Angeben des Timeout Zeitraums verwendet werden. Der Wert 0 oder **null** zeigt an, dass der Client keine Zeitanforderungen für den Übergang hat. Wenn diese Eigenschaft nicht 0 oder **null** enthält und die Implementierung diesen Parameter nicht unterstützt, muss der Rückgabecode 4098 (**use of Timeout Parameter not supported**) zurückgegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.



| Rückgabecode/-wert                                                                                                                                                                       | BESCHREIBUNG                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt> </dl>                           | Erfolg.<br/>                                                                |
| <dl> <dt>**Nicht unterstützt**</dt> <dt>1</dt> </dl>                                     |                                                                                    |
| <dl> Über <dt>**prüfte Methoden Parameter-der Übergang**</dt> wurde <dt>4096</dt> gestartet. </dl> | Der Übergang erfolgt asynchron.<br/>                                         |
| <dl> <dt>**Verwendung des timeout-Parameters wird nicht unterstützt**</dt> <dt>4098</dt> </dl>         |                                                                                    |
| <dl> <dt>**Zugriff verweigert**</dt> <dt>32769</dt> </dl>                                 | Zugriff verweigert.<br/>                                                          |
| <dl> <dt>**Ungültiger Status für diesen Vorgang**</dt> <dt>32775</dt> </dl>              | Der im *requestedstate* -Parameter angegebene Wert wird nicht unterstützt.<br/> |



 

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

[**MSVM- \_ guestservice**](msvm-guestservice.md)
</dt> </dl>

 

 




