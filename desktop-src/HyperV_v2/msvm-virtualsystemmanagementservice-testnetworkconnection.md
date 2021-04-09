---
description: Testet die Netzwerk Konnektivität eines virtuellen Computers in einer Windows-netzwerkvirtualisierungsumgebung.
ms.assetid: 37d4c34d-406e-4c52-afce-b0eef754eeb3
title: Testnetworkconnection-Methode der Msvm_VirtualSystemManagementService-Klasse
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
ms.openlocfilehash: e8f15faacb1b8ad683b1ea9abfa9b91f5c376dab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128400"
---
# <a name="testnetworkconnection-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Testnetworkconnection-Methode der MSVM \_ virtualsystemmanagementservice-Klasse

Testet die Netzwerk Konnektivität eines virtuellen Computers in einer Windows-netzwerkvirtualisierungsumgebung.

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

*Targetnetworkadapter* \[ in\]
</dt> <dd>

Verweis auf eine [**MSVM- \_ ethernetportbereitungssettingdata**](msvm-ethernetportallocationsettingdata.md) , die den Zielnetzwerk Adapter beschreibt.

</dd> <dt>

*Issender* \[ in\]
</dt> <dd>

Gibt an, ob diese Methode beim Absender oder Empfänger aufgerufen wird.

</dd> <dt>

*Senderip* \[ in\]
</dt> <dd>

Die Absender-IP-Adresse.

</dd> <dt>

*Receiverip* \[ in\]
</dt> <dd>

Die Mac-Adresse des Senders.

</dd> <dt>

*Receivermac* \[ in\]
</dt> <dd>

Die Mac-Adresse des Senders.

</dd> <dt>

*Isolationid* \[ in\]
</dt> <dd>

Die Isolations-ID.

</dd> <dt>

*Sequencennummer* \[ in\]
</dt> <dd>

Die Isolations-ID.

</dd> <dt>

*RoundtripTime* \[ vorgenommen\]
</dt> <dd>

Die Roundtripzeit.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

Fehler **(2** )
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Ungültiger Parameter** (4)
</dt> <dt>

**DMTF reserviert** (..)
</dt> <dt>

Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)
</dt> <dt>

**Reservierte Methode** (4097.32767)
</dt> <dt>

**Hersteller spezifisch** (32768.65535)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

