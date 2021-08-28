---
description: Fügt der Konfiguration eines Ethernet-Switchports Featureeinstellungen hinzu.
ms.assetid: 628a6546-cc78-4fde-be0c-533a2c3f9483
title: AddFeatureSettings-Methode der Msvm_VirtualEthernetSwitchManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.AddFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 679e4dbba4b8d3e90691955a0642f9a22692d73824059419f5faceacc85abaf1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829660"
---
# <a name="addfeaturesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a>AddFeatureSettings-Methode der Msvm \_ VirtualEthernetSwitchManagementService-Klasse

Fügt der Konfiguration eines Ethernet-Switchports Featureeinstellungen hinzu.

## <a name="syntax"></a>Syntax


```mof
uint32 AddFeatureSettings(
  [in]  CIM_SettingData         REF AffectedConfiguration,
  [in]  string                      FeatureSettings[],
  [out] Msvm_FeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob         REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AffectedConfiguration* \[ In\]
</dt> <dd>

Ein Verweis auf eine [**von CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) abgeleitete Klasse, die den betroffenen Ethernet-Switchport oder die Ethernet-Switchkonfiguration darstellt.

</dd> <dt>

*FeatureSettings* \[ In\]
</dt> <dd>

Ein Array von Zeichenfolgen, das eine eingebettete Instanz einer Von der [**Msvm \_ FeatureSettingData-Klasse**](msvm-featuresettingdata.md) abgeleiteten Klasse enthält, die die Featureeinstellungen beschreibt, die der Switchportkonfiguration hinzugefügt werden sollen.

</dd> <dt>

*ResultingFeatureSettings* \[ out\]
</dt> <dd>

Ein Array von Verweisen auf Instanzen der [**Msvm \_ FeatureSettingData-Klasse,**](msvm-featuresettingdata.md) die die hinzugefügten Featureeinstellungen darstellen.

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
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ModifyFeatureSettings**](modifyfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[**RemoveFeatureSettings**](removefeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[**Msvm \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

