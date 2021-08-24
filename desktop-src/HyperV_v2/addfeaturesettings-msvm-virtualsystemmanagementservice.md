---
description: Fügt der Konfiguration einer Ethernet-Verbindung eines virtuellen Computers Ethernet-Featureeinstellungen hinzu.
ms.assetid: f233bf2f-5201-4b02-8384-bb7e2d1e7dee
title: AddFeatureSettings-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d81fb7dd8f7b4c9d3259977c6cdaf1498490c3617699f1d19ccdb47e5eb6b34d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746550"
---
# <a name="addfeaturesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>AddFeatureSettings-Methode der Msvm \_ VirtualSystemManagementService-Klasse

Fügt der Konfiguration einer Ethernet-Verbindung eines virtuellen Computers Ethernet-Featureeinstellungen hinzu.

## <a name="syntax"></a>Syntax


```mof
uint32 AddFeatureSettings(
  [in]  Msvm_EthernetPortAllocationSettingData    REF AffectedConfiguration,
  [in]  string                                        FeatureSettings[],
  [out] Msvm_EthernetSwitchPortFeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob                           REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AffectedConfiguration* \[ In\]
</dt> <dd>

Verweis auf eine Instanz der [**Msvm \_ EthernetPortAllocationSettingData-Klasse,**](msvm-ethernetportallocationsettingdata.md) die die betroffene Ethernet-Verbindung darstellt.

</dd> <dt>

*FeatureSettings* \[ In\]
</dt> <dd>

Ein Array von Zeichenfolgen, das eine eingebettete Instanz der [**Msvm \_ EthernetSwitchFeatureSettingData-Klasse**](msvm-ethernetswitchfeaturesettingdata.md) enthält, die die Featureeinstellungen beschreibt, die der Verbindungskonfiguration hinzugefügt werden sollen.

</dd> <dt>

*ResultingFeatureSettings* \[ out\]
</dt> <dd>

Ein Array von Verweisen auf Instanzen der [**Msvm \_ EthernetSwitchFeatureSettingData-Klasse,**](msvm-ethernetswitchportfeaturesettingdata.md) die die hinzugefügten Featureeinstellungen darstellt.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein objekt, das von [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))abgeleitet wurde.

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

**Überprüfte Methodenparameter – Auftragsstart** (4096)
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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

