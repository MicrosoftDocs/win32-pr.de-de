---
description: Ändert die Ressourcen Einstellungen des übergeordneten Pools für Ressourcen, die einem untergeordneten Pool zugewiesen sind.
ms.assetid: 419fca70-5f15-4593-80ac-ef2af2c3dde5
title: Modifypoolresources-Methode der Msvm_ResourcePoolConfigurationService-Klasse
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
ms.openlocfilehash: 2efffdbcc34577f675556874c4153eea2670768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867071"
---
# <a name="modifypoolresources-method-of-the-msvm_resourcepoolconfigurationservice-class"></a>Modifypoolresources-Methode der MSVM \_ resourcepoolconfigurationservice-Klasse

Ändert die Ressourcen Einstellungen des übergeordneten Pools für Ressourcen, die einem untergeordneten Pool zugewiesen sind.

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

*Childpool* \[ in\]
</dt> <dd>

Ein Verweis auf eine Instanz der [**CIM \_ resourcepool**](cim-resourcepool.md) -Klasse, die den zu ändernden untergeordneten Pool darstellt.

</dd> <dt>

"Parser"- *Pools* \[ in\]
</dt> <dd>

Ein Array von [**CIM- \_ resourcepool**](cim-resourcepool.md) -verweisen, die die neuen übergeordneten Pools darstellen, die dem untergeordneten Pool zugewiesen werden sollen.

</dd> <dt>

*Zuordnung von Einstellungen* \[ in\]
</dt> <dd>

Ein optionales Array von mindestens einer eingebetteten Instanz der [**MSVM \_ resourceallocationsettingdata**](msvm-resourceallocationsettingdata.md) -Klasse, die verwendet wird, um die Einstellungen für die Pool Zuordnung anzugeben.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Auftrag ohne Fehler abgeschlossen** (0)
</dt> <dt>

**DMTF reserviert** (..)
</dt> <dt>

Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)
</dt> <dt>

**Reservierte Methode** (4097.32767)
</dt> <dt>

Fehler **(32768** )
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

**Verwendet** (32774)
</dt> <dt>

**Ungültiger Status** (32775)
</dt> <dt>

**Falscher Ressourcentyp für den Pool** (32776).
</dt> <dt>

Nicht **verfügbar** (32777)
</dt> <dt>

**Nicht** genügend Arbeitsspeicher (32778)
</dt> <dt>

**Anbieter reserviert** (32779)
</dt> <dt>

**Unzureichende Ressourcen** (32780)
</dt> <dt>

**Objekt nicht gefunden** (32781.. 32787)
</dt> <dt>

**Objekt vorhanden** (32788)
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

[**MSVM \_ resourcepoolconfigurationservice**](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

