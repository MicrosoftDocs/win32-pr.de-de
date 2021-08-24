---
description: Fügt einer Konfiguration des virtuellen Systems Gastdiensteinstellungen hinzu.
ms.assetid: 2c8c2f2b-332a-470e-af7f-80c82e3e2caf
title: AddGuestServiceSettings-Methode der Msvm_VirtualSystemManagementService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddGuestServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4f011a0bce545bbde57cbcc9c22861f492cbc27e71ddc717a379d82cbd27bc42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681140"
---
# <a name="addguestservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>AddGuestServiceSettings-Methode der Msvm \_ VirtualSystemManagementService-Klasse

Fügt einer Konfiguration des virtuellen Systems Gastdiensteinstellungen hinzu.

Wenn sie auf Teile einer "aktuellen" Konfiguration des virtuellen Systems angewendet wird, können Gastdienste des aktiven virtuellen Systems als Nebeneffekt geändert werden.

## <a name="syntax"></a>Syntax


```mof
uint32 AddGuestServiceSettings(
  [in]  CIM_VirtualSystemSettingData REF AffectedConfiguration,
  [in]  string                           GuestServiceSettings[],
  [out] CIM_SettingData              REF ResultingGuestServiceSettings[],
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AffectedConfiguration* \[ In\]
</dt> <dd>

Verweis auf ein [**CIM \_ VirtualSystemSettingData,**](cim-virtualsystemsettingdata.md) das die betroffene Konfiguration beschreibt.

</dd> <dt>

*GuestServiceSettings* \[ In\]
</dt> <dd>

Ein Array, das die Einstellungen des Gastdiensts enthält.

</dd> <dt>

*ResultingGuestServiceSettings* \[ out\]
</dt> <dd>

Bei Erfolg enthält einen Verweis auf CIM [**\_ SettingData,**](cim-settingdata.md) das die resultierenden Gastdiensteinstellungen beschreibt.

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
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

