---
description: Fügt einer Konfiguration des virtuellen Systems Ressourcen hinzu.
ms.assetid: c2541571-74f0-48f8-997c-56c152980eea
title: AddResourceSettings-Methode der CIM_VirtualSystemManagementService-Klasse
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
ms.openlocfilehash: 0387d3d46723aede1d0858d647a555db57b3de28e6c1fb5fbb68b6d56342fcb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118646468"
---
# <a name="addresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a>AddResourceSettings-Methode der CIM \_ VirtualSystemManagementService-Klasse

Fügt einer Konfiguration des virtuellen Systems Ressourcen hinzu.

Bei Anwendung auf eine Zustandskonfiguration des virtuellen Systems werden dem aktiven virtuellen System als Nebeneffekt Ressourcen hinzugefügt.

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

*AffectedConfiguration* \[ In\]
</dt> <dd>

Ein [**CIM \_ VirtualSystemSettingData-Verweis**](cim-virtualsystemsettingdata.md) auf die betroffene Konfiguration des virtuellen Systems.

</dd> <dt>

*ResourceSettings* \[ In\]
</dt> <dd>

Array von Zeichenfolgen, die jeweils eine eingebettete Instanz der [**Klasse CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) enthalten, die die virtuellen Aspekte einer virtuellen Ressource beschreibt, die dem virtuellen System hinzugefügt werden soll.

</dd> <dt>

*ResultingResourceSettings* \[ out\]
</dt> <dd>

Array von Verweisen auf Instanzen der [**Klasse CIM \_ ResourceAllocationSettingData,**](cim-resourceallocationsettingdata.md) die virtuelle Aspekte der hinzugefügten virtuellen Ressourcen darstellen.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang lange ausgeführt wird, kann optional ein Auftrag zurückgegeben werden. In diesem Fall sind die Instanzen der [**Klasse CIM \_ ResourceAllocationSettingData,**](cim-resourceallocationsettingdata.md) die die hinzugefügten Ressourceneinstellungen darstellt, über die Zuordnung **CIM \_ ConreteComponent** aus der Instanz der Klasse [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) verfügbar, die die betroffene Konfiguration des virtuellen Systems darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Wert 0 zurück. andernfalls wird ein Fehler zurückgegeben.

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
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**CIM \_ VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




