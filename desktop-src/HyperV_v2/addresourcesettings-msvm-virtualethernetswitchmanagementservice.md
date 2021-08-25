---
description: Fügt einer Konfiguration eines virtuellen Switches Ressourcen hinzu.
ms.assetid: aad5fac1-3884-4a95-abe3-bf192f23ea41
title: AddResourceSettings-Methode der Msvm_VirtualEthernetSwitchManagementService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.AddResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e13b9a9738b830f5b9dfcce5f37efa23c1014c735a5cb0a9cc0e09afa7b0038
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914150"
---
# <a name="addresourcesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a>AddResourceSettings-Methode der Msvm \_ VirtualEthernetSwitchManagementService-Klasse

Fügt einer Konfiguration eines virtuellen Switches Ressourcen hinzu. Wenn sie auf eine Konfiguration des virtuellen Computers "Zustand" angewendet wird, werden dem aktiven virtuellen Computer Nebeneffektressourcen hinzugefügt.

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

Ein Verweis auf ein [**CIM \_ VirtualSystemSettingData-Objekt,**](/previous-versions//cc136954(v=vs.85)) das die betroffene Konfiguration des virtuellen Switches darstellt.

</dd> <dt>

*ResourceSettings* \[ In\]
</dt> <dd>

Ein Array von Zeichenfolgen, das eine eingebettete Instanz der [**\_ CIM-Klasse ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) enthält, die die virtuellen Aspekte einer virtuellen Ressource beschreibt, die dem virtuellen Switch hinzugefügt werden soll.

</dd> <dt>

*ResultingResourceSettings* \[ out\]
</dt> <dd>

Ein Array von Verweisen auf Instanzen der [**\_ CIM-Klasse ResourceAllocationSettingData,**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) die virtuelle Aspekte der hinzugefügten virtuellen Ressourcen darstellt.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[**RemoveResourceSettings**](removeresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[**Msvm \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

