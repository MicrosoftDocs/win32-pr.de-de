---
description: Testet die Netzwerkkonnektivität eines virtuellen Computers in Windows Netzwerkvirtualisierungsumgebung.
ms.assetid: 37d4c34d-406e-4c52-afce-b0eef754eeb3
title: TestNetworkConnection-Methode der Msvm_VirtualSystemManagementService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.TestNetworkConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 66988944b6c4f4a97a450f63964d57084fc5886716d109e655921d8744bba721
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119388379"
---
# <a name="testnetworkconnection-method-of-the-msvm_virtualsystemmanagementservice-class"></a>TestNetworkConnection-Methode der Msvm \_ VirtualSystemManagementService-Klasse

Testet die Netzwerkkonnektivität eines virtuellen Computers in Windows Netzwerkvirtualisierungsumgebung.

## <a name="syntax"></a>Syntax


```mof
uint32 TestNetworkConnection(
  [in]  Msvm_EthernetPortAllocationSettingData REF TargetNetworkAdapter,
  [in]  boolean                                    IsSender,
  [in]  string                                     SenderIP,
  [in]  string                                     ReceiverIP,
  [in]  string                                     ReceiverMac,
  [in]  uint32                                     IsolationId,
  [in]  uint32                                     SequenceNumber,
  [out] uint32                                     RoundTripTime,
  [out] CIM_ConcreteJob                        REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*TargetNetworkAdapter* \[ In\]
</dt> <dd>

Verweis auf ein [**Msvm \_ EthernetPortAllocationSettingData-Objekt,**](msvm-ethernetportallocationsettingdata.md) das den Zielnetzwerkadapter beschreibt.

</dd> <dt>

*IsSender* \[ In\]
</dt> <dd>

Gibt an, ob diese Methode beim Absender oder empfänger aufgerufen wird.

</dd> <dt>

*SenderIP* \[ In\]
</dt> <dd>

Die IP-Adresse des Absenders.

</dd> <dt>

*ReceiverIP* \[ In\]
</dt> <dd>

Die Mac-Adresse des Absenders.

</dd> <dt>

*ReceiverMac* \[ In\]
</dt> <dd>

Die Mac-Adresse des Absenders.

</dd> <dt>

*IsolationId* \[ In\]
</dt> <dd>

Die Isolations-ID.

</dd> <dt>

*SequenceNumber* \[ In\]
</dt> <dd>

Die Isolations-ID.

</dd> <dt>

*RoundTripTime* \[ out\]
</dt> <dd>

Die Roundtripzeit.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ ConcreteJob abgeleitet wurde.**](/previous-versions//cc136808(v=vs.85))

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

**Fehler** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Ungültiger Parameter** (4)
</dt> <dt>

**DMTF Reserved** (..)
</dt> <dt>

**Überprüfte Methodenparameter – Auftrag gestartet** (4096)
</dt> <dt>

**Reservierte Methode** (4097..32767)
</dt> <dt>

**Herstellerspezifisch** (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

