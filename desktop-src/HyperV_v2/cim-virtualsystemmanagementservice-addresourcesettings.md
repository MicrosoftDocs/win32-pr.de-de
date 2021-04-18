---
description: Fügt der Konfiguration eines virtuellen Systems Ressourcen hinzu.
ms.assetid: c2541571-74f0-48f8-997c-56c152980eea
title: Adresssourcesettings-Methode der CIM_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.AddResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9563b1e8421dfa6724971450b117780435f6f39e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347100"
---
# <a name="addresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a>Adresssourcesettings-Methode der CIM \_ virtualsystemmanagementservice-Klasse

Fügt der Konfiguration eines virtuellen Systems Ressourcen hinzu.

Wenn Sie auf eine virtuelle Systemkonfiguration vom Typ "State" angewendet werden, werden dem aktiven virtuellen System als Nebeneffekte Ressourcen hinzugefügt.

## <a name="syntax"></a>Syntax


```mof
uint32 AddResourceSettings(
  [in]  CIM_VirtualSystemSettingData      REF AffectedConfiguration,
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Affectedconfiguration* \[ in\]
</dt> <dd>

Ein [**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md) -Verweis auf die betroffene virtuelle Systemkonfiguration.

</dd> <dt>

*Resourcesettings* \[ in\]
</dt> <dd>

Ein Array von Zeichen folgen, die jeweils eine eingebettete Instanz der Klasse [**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md) enthalten, die die virtuellen Aspekte einer virtuellen Ressource beschreibt, die dem virtuellen System hinzugefügt werden soll.

</dd> <dt>

*Resultingresourcesettings* \[ vorgenommen\]
</dt> <dd>

Array von Verweisen auf Instanzen der Klasse [**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md) , die virtuelle Aspekte der hinzugefügten virtuellen Ressourcen darstellen.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Wenn der Vorgang lange ausgeführt wird, kann optional ein Auftrag zurückgegeben werden. In diesem Fall sind die Instanzen der Klasse " [**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md) ", die die hinzugefügten Ressourcen Einstellungen darstellen, über die "Association CIM"- **\_ Komponente** aus der Instanz der Klasse " [**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md) " verfügbar, die die betroffene virtuelle Systemkonfiguration darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.

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

[**CIM \_ virtualsystemmanagementservice**](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




