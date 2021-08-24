---
description: Ändert die aktuellen Featureeinstellungen einer Ethernet-Verbindung eines virtuellen Computers.
ms.assetid: 3caa810f-0444-45cf-88a4-e93d04accb46
title: ModifyFeatureSettings-Methode der Msvm_VirtualSystemManagementService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: be963ee0bc57ddc0a9570c3ac9b35b1d8dadaeca48d295b45f0134b6c05f632a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694070"
---
# <a name="modifyfeaturesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>ModifyFeatureSettings-Methode der Msvm \_ VirtualSystemManagementService-Klasse

Ändert die aktuellen Featureeinstellungen einer Ethernet-Verbindung eines virtuellen Computers.

## <a name="syntax"></a>Syntax


```mof
uint32 ModifyFeatureSettings(
  [in]  string                                        FeatureSettings[],
  [out] Msvm_EthernetSwitchPortFeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob                           REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FeatureSettings* \[ In\]
</dt> <dd>

Ein Array von Zeichenfolgen, das eine eingebettete Instanz einer Klasse enthält, die von der [**Msvm \_ EthernetSwitchFeatureSettingData-Klasse**](msvm-ethernetswitchfeaturesettingdata.md) abgeleitet wurde und Änderungen an den aktuellen Featureeinstellungen einer vorhandenen Ethernet-Verbindung beschreibt. Die **InstanceID-Eigenschaft** jeder dieser Instanzen identifiziert die zu ändernden Featureeinstellungen.

</dd> <dt>

*ResultingFeatureSettings* \[ out\]
</dt> <dd>

Ein Array von Verweisen auf Instanzen der [**Msvm \_ EthernetSwitchPortFeatureSettingData-Klasse,**](msvm-ethernetswitchportfeaturesettingdata.md) die die geänderten Featureeinstellungen darstellen.

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

**Ungültiger Zustand** (5)
</dt> <dt>

**Inkompatible** Parameter (6)
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
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

