---
description: Fügt einer Konfiguration des virtuellen Systems Startquellen hinzu, wenn sie auf eine &\# 0034;Status&\# 0034; virtuelle Systemkonfiguration angewendet wird.
ms.assetid: 2d091554-73d4-47c6-a0c2-97644fc9abe9
title: AddBootSourceSettings-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddBootSourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d52333f3118caa1cf437fabb536bb62f84b99dab01b3115e7f6a65c3f182a17e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148073"
---
# <a name="addbootsourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>AddBootSourceSettings-Methode der Msvm \_ VirtualSystemManagementService-Klasse

Fügt einer Konfiguration des virtuellen Systems Startquellen hinzu, wenn sie auf eine Zustandskonfiguration des virtuellen Systems angewendet wird.

## <a name="syntax"></a>Syntax


```mof
uint32 AddBootSourceSettings(
  [in]  CIM_VirtualSystemSettingData REF AffectedConfiguration,
  [in]  string                           BootSourceSettings[],
  [out] CIM_SettingData              REF ResultingBootSourceSettings[],
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AffectedConfiguration* \[ In\]
</dt> <dd>

Eine [**CIM \_ VirtualSystemSettingData-Datei,**](cim-virtualsystemsettingdata.md) die die betroffene Konfiguration enthält.

</dd> <dt>

*BootSourceSettings* \[ In\]
</dt> <dd>

Ein Array, das die Startquelleinstellungen enthält.

</dd> <dt>

*ResultingBootSourceSettings* \[ out\]
</dt> <dd>

Bei Erfolg wird cim [**\_ settingData**](cim-settingdata.md) mit den resultierenden Startquelleinstellungen zurückgegeben.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein objekt, das von [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))abgeleitet wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 oder 4096 zurück. andernfalls wird ein Fehler zurückgegeben.

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
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

