---
description: Fügt einem synthetischen Fibre Channel Port auf einem virtuellen Computer dh-CHAP (Diffie Hellman-Challenge Handshake Authentication Protocol)-Parameter hinzu.
ms.assetid: b9799ea4-f948-4b5c-bd18-1faa90213bb3
title: Addfbrechannelchap-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddFibreChannelChap
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 07151a902efa8f8077debc44bd732286c0a96a81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959806"
---
# <a name="addfibrechannelchap-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Addfibrechannelchap-Methode der MSVM \_ virtualsystemmanagementservice-Klasse

Fügt einem synthetischen Fibre Channel Port auf einem virtuellen Computer dh-CHAP (Diffie Hellman-Challenge Handshake Authentication Protocol)-Parameter hinzu. Bei dieser Methode tritt ein Fehler auf, wenn der virtuelle Computer ausgeführt wird.

## <a name="syntax"></a>Syntax


```mof
uint32 AddFibreChannelChap(
  [in] string FcPortSettings[],
  [in] uint8  SecretEncoding,
  [in] uint8  SharedSecret[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Fcportsettings* \[ in\]
</dt> <dd>

Ein Array von Zeichen folgen, die eine eingebettete Instanz der [**MSVM \_ syntheticfcportsettingdata**](msvm-syntheticfcportsettingdata.md) -Klasse enthalten, die Einstellungen für synthetische Fibre Channel Ports für virtuelle Maschinen beschreibt. Die **InstanceId-** Eigenschaft jeder dieser Instanzen identifiziert die Elemente, die geändert werden sollen.

</dd> <dt>

*Secretencoding* \[ in\]
</dt> <dd>

Gibt den Codierungstyp für den gemeinsamen geheimen Schlüssel an.

<dt>

<span id="Printable_ASCII"></span><span id="printable_ascii"></span><span id="PRINTABLE_ASCII"></span>

**Druckbare ASCII** (1)


</dt> <dd></dd> <dt>

<span id="Binary"></span><span id="binary"></span><span id="BINARY"></span>

**Binär** (2)


</dt> <dd></dd> </dl> </dd> <dt>

*Sharedsecret* \[ in\]
</dt> <dd>

Gibt den gemeinsamen geheimen Schlüssel an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

Fehler **(32768** )
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

Der **Status ist "Unknown** " (32771).
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger Parameter** (32773)
</dt> <dt>

**System wird verwendet** (32774)
</dt> <dt>

**Ungültiger Status für diesen Vorgang** (32775).
</dt> <dt>

**Falscher Datentyp** (32776).
</dt> <dt>

Das **System ist nicht verfügbar** (32777).
</dt> <dt>

**Nicht** genügend Arbeitsspeicher (32778)
</dt> </dl>

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

[**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




