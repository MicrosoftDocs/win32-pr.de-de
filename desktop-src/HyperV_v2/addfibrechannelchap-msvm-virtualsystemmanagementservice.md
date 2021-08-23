---
description: Fügt DH-CHAP-Parameter (Diffie Hellman – Challenge Handshake Authentication Protocol) einem synthetischen Fibre Channel Port auf einem virtuellen Computer hinzu.
ms.assetid: b9799ea4-f948-4b5c-bd18-1faa90213bb3
title: AddFibreChannelChap-Methode der Msvm_VirtualSystemManagementService-Klasse
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
ms.openlocfilehash: 26a9f99826e92a35462f0c42e8fce723168799177e96e0ae429aad45c99de928
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562360"
---
# <a name="addfibrechannelchap-method-of-the-msvm_virtualsystemmanagementservice-class"></a>AddFibreChannelChap-Methode der Msvm \_ VirtualSystemManagementService-Klasse

Fügt DH-CHAP-Parameter (Diffie Hellman – Challenge Handshake Authentication Protocol) einem synthetischen Fibre Channel Port auf einem virtuellen Computer hinzu. Diese Methode schlägt fehl, wenn der virtuelle Computer ausgeführt wird.

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

*FcPortSettings* \[ In\]
</dt> <dd>

Ein Array von Zeichenfolgen, die eine eingebettete Instanz der [**Msvm \_ SyntheticFcPortSettingData-Klasse**](msvm-syntheticfcportsettingdata.md) enthalten, die Einstellungen für synthetische Fibre Channel Ports für virtuelle Computer beschreibt. Die **InstanceID-Eigenschaft** jeder dieser Instanzen identifiziert die zu ändernden Elemente.

</dd> <dt>

*SecretEncoding* \[ In\]
</dt> <dd>

Gibt den Typ der Codierung für das gemeinsame Geheimnis an.

<dt>

<span id="Printable_ASCII"></span><span id="printable_ascii"></span><span id="PRINTABLE_ASCII"></span>

**Druckbarer ASCII-Code** (1)


</dt> <dd></dd> <dt>

<span id="Binary"></span><span id="binary"></span><span id="BINARY"></span>

**Binär** (2)


</dt> <dd></dd> </dl> </dd> <dt>

*SharedSecret* \[ In\]
</dt> <dd>

Gibt das gemeinsame Geheimnis an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Fehler** (32768)
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

**Status ist unbekannt** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger Parameter** (32773)
</dt> <dt>

**System wird verwendet** (32774)
</dt> <dt>

**Ungültiger Zustand für diesen Vorgang** (32775)
</dt> <dt>

**Falscher Datentyp** (32776)
</dt> <dt>

**System ist nicht verfügbar** (32777)
</dt> <dt>

**Nicht genügend Arbeitsspeicher** (32778)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




