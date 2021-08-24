---
description: 'ModifyResourceSettings-Methode der CIM_VirtualSystemManagementService Klasse: Ändert einstellungen für virtuelle Ressourcen.'
ms.assetid: 4942f167-0e53-4ae2-b973-4a06b636b44a
title: ModifyResourceSettings-Methode der CIM_VirtualSystemManagementService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.ModifyResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bc001d87a95e54682f6b6b4ffdecd3c53d3288b58a6dcb5b6e9a8a4d2dc528e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682730"
---
# <a name="modifyresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a>ModifyResourceSettings-Methode der CIM \_ VirtualSystemManagementService-Klasse

Ändert einstellungen für virtuelle Ressourcen.

Wenn sie auf Teile einer "aktuellen" Konfiguration des virtuellen Systems angewendet wird, können Als Nebeneffekt Ressourcen des aktiven virtuellen Systems geändert werden.

## <a name="syntax"></a>Syntax


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ResourceSettings* \[ In\]
</dt> <dd>

Array von Zeichenfolgen, die jeweils eine eingebettete Instanz der [**Klasse CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) enthalten, die Änderungen an den virtuellen Aspekten einer vorhandenen virtuellen Ressource beschreibt. Alle Instanzen müssen über eine gültige **InstanceID** verfügen, um die zu ändernde Einstellung der virtuellen Ressource zu identifizieren.

</dd> <dt>

*ResultingResourceSettings* \[ out\]
</dt> <dd>

Array von Verweisen auf Instanzen der Klasse [**CIM \_ ResourceAllocationSettingData,**](cim-resourceallocationsettingdata.md) die virtuelle Aspekte der geänderten virtuellen Ressourcen darstellen.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang lange ausgeführt wird, wird optional ein Auftrag zurückgegeben. In diesem Fall sind die Instanzen der [**Klasse CIM \_ ResourceAllocationSettingData,**](cim-resourceallocationsettingdata.md) die die geänderten Ressourceneinstellungen darstellen, über die Zuordnung **CIM \_ ConreteComponent** aus der Instanz der [**Klasse CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) verfügbar, die die betroffene Konfiguration des virtuellen Systems darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg eine 0 zurück. andernfalls gibt einen Fehler zurück.

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
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




