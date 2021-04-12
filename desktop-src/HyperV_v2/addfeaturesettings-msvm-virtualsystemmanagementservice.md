---
description: Fügt der Konfiguration einer Ethernet-Verbindung mit einem virtuellen Computer Ethernet-Funktionseinstellungen hinzu.
ms.assetid: f233bf2f-5201-4b02-8384-bb7e2d1e7dee
title: Addfeaturesettings-Methode der Msvm_VirtualSystemManagementService-Klasse
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
ms.openlocfilehash: 5e9acbaaf6ff1da6439dcb243869e09133e0031e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345559"
---
# <a name="addfeaturesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Addfeaturesettings-Methode der MSVM \_ virtualsystemmanagementservice-Klasse

Fügt der Konfiguration einer Ethernet-Verbindung mit einem virtuellen Computer Ethernet-Funktionseinstellungen hinzu.

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

*Affectedconfiguration* \[ in\]
</dt> <dd>

Verweis auf eine Instanz der [**MSVM-Klasse " \_ ethernetportzuweisung**](msvm-ethernetportallocationsettingdata.md) ", die die betroffene Ethernet-Verbindung darstellt.

</dd> <dt>

*Featuresettings* \[ in\]
</dt> <dd>

Ein Array von Zeichen folgen, das eine eingebettete Instanz der [**MSVM \_ ethertesettingdata**](msvm-ethernetswitchfeaturesettingdata.md) -Klasse enthält, die die Funktionseinstellungen beschreibt, die der Verbindungs Konfiguration hinzugefügt werden sollen.

</dd> <dt>

*Resultingfeaturesettings* \[ vorgenommen\]
</dt> <dd>

Ein Array von Verweisen auf Instanzen der [**MSVM \_ ethertesettingdata**](msvm-ethernetswitchportfeaturesettingdata.md) -Klasse, die die hinzugefügten Funktionseinstellungen darstellt.

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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

