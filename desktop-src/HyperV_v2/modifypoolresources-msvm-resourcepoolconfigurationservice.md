---
description: Ändert die Ressourceneinstellungen des übergeordneten Pools für Ressourcen, die einem untergeordneten Pool zugewiesen sind.
ms.assetid: 419fca70-5f15-4593-80ac-ef2af2c3dde5
title: ModifyPoolResources-Methode der Msvm_ResourcePoolConfigurationService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.ModifyPoolResources
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2b67b749e1ffa24c26a088b0819f1af11763e671625d3668dd20197122edba32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118149665"
---
# <a name="modifypoolresources-method-of-the-msvm_resourcepoolconfigurationservice-class"></a>ModifyPoolResources-Methode der Msvm \_ ResourcePoolConfigurationService-Klasse

Ändert die Ressourceneinstellungen des übergeordneten Pools für Ressourcen, die einem untergeordneten Pool zugewiesen sind.

## <a name="syntax"></a>Syntax


```mof
uint32 ModifyPoolResources(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  CIM_ResourcePool REF ParentPools[],
  [in]  string               AllocationSettings[],
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ChildPool* \[ In\]
</dt> <dd>

Ein Verweis auf eine Instanz der [**CIM \_ ResourcePool-Klasse,**](cim-resourcepool.md) die den zu ändernden untergeordneten Pool darstellt.

</dd> <dt>

*ParentPools* \[ In\]
</dt> <dd>

Ein Array von [**CIM \_ ResourcePool-Verweisen,**](cim-resourcepool.md) die die neuen übergeordneten Pools darstellen, die dem untergeordneten Pool zugewiesen werden.

</dd> <dt>

*AllocationSettings* \[ In\]
</dt> <dd>

Ein optionales Array von mindestens einer eingebetteten Instanz der [**Msvm \_ ResourceAllocationSettingData-Klasse,**](msvm-resourceallocationsettingdata.md) die zum Angeben der Einstellungen für die Poolzuordnung verwendet werden.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ ConcreteJob abgeleitet wurde.**](/previous-versions//cc136808(v=vs.85))

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Auftrag ohne Fehler** abgeschlossen (0)
</dt> <dt>

**DMTF Reserved** (..)
</dt> <dt>

**Überprüfte Methodenparameter – Auftrag gestartet** (4096)
</dt> <dt>

**Reservierte Methode** (4097..32767)
</dt> <dt>

**Fehler** (32768)
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

**Unbekannt** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger Parameter** (32773)
</dt> <dt>

**Wird verwendet** (32774)
</dt> <dt>

**Ungültiger Zustand** (32775)
</dt> <dt>

**Falscher Ressourcentyp für den Pool** (32776)
</dt> <dt>

**Nicht verfügbar** (32777)
</dt> <dt>

**Nicht genügend Arbeitsspeicher** (32778)
</dt> <dt>

**Reservierter Anbieter** (32779)
</dt> <dt>

**Unzureichende Ressourcen** (32780)
</dt> <dt>

**Objekt nicht gefunden** (32781..32787)
</dt> <dt>

**Objekt vorhanden** (32788)
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

[**Msvm \_ ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

