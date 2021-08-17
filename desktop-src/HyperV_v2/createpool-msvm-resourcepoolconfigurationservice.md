---
description: Erstellt einen untergeordneten Ressourcenpool.
ms.assetid: 30a70231-f1b7-4f0e-ac47-cf5a79ddb8ab
title: CreatePool-Methode der Msvm_ResourcePoolConfigurationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.CreatePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ff1c8a3357a019d9036dd2ac97482a2b106115d06375e96d428ce3d38f6244d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119254350"
---
# <a name="createpool-method-of-the-msvm_resourcepoolconfigurationservice-class"></a>CreatePool-Methode der Msvm \_ ResourcePoolConfigurationService-Klasse

Erstellt einen untergeordneten Ressourcenpool. Der Ressourcenpool wird auf dasselbe System wie dieser Dienst bereichiert. Der resultierende Pool ist ein untergeordneter Pool.

## <a name="syntax"></a>Syntax


```mof
uint32 CreatePool(
  [in]  string               PoolSettings,
  [in]  CIM_ResourcePool REF ParentPools[],
  [in]  string               AllocationSettings[],
  [out] CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PoolSettings* \[ In\]
</dt> <dd>

Eine eingebettete Instanz der [**Msvm \_ ResourcePoolSettingData-Klasse,**](msvm-resourcepoolsettingdata.md) die verwendet wird, um die Pooleinstellungen anzugeben, die nicht zuordnungsbezogen sind.

</dd> <dt>

*ParentPools* \[ In\]
</dt> <dd>

Ein Array von [**Msvm \_ ResourcePool-Verweisen,**](msvm-resourcepool.md) die den Pool oder die Pools darstellen, aus denen der neue Pool erstellt werden soll.

</dd> <dt>

*AllocationSettings* \[ In\]
</dt> <dd>

Ein Array von einer oder mehreren eingebetteten Instanzen der [**Msvm \_ ResourceAllocationSettingData-Klasse,**](msvm-resourceallocationsettingdata.md) die zum Angeben der Einstellungen für die Poolzuordnung verwendet werden. Dieses Array muss entweder ein Element für jedes Element im *ParentPools-Array* oder genau ein Element enthalten. Wenn dieses Array ein Element und *ParentPools* mehrere Elemente enthält, gibt *AlllocationSettings* eine freigegebene Kapazitätszuordnung an, die von einem der übergeordneten Pools erfüllt werden kann.

Dies wird verwendet, um die Ressourcen, die vom untergeordneten Element zum Pool zugeordnet werden können, auf einen niedrigeren Grenzwert als die aggregierte Kapazität zu beschränken, die von den untergeordneten Ressourcen bereitgestellt wird. Diese Option wird nicht von allen Ressourcentypen unterstützt. Wenn ein Ressourcentyp keine freigegebene Kapazitätszuordnung unterstützt, gibt diese Methode 32770 (Nicht unterstützt) zurück.

</dd> <dt>

*Pool* \[ out\]
</dt> <dd>

Ein Verweis auf den resultierenden Pool.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein objekt, das von [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))abgeleitet wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Auftrag ohne Fehler abgeschlossen** (0)
</dt> <dt>

**DMTF Reserved** (..)
</dt> <dt>

**Überprüfte Methodenparameter – Auftragsstart** (4096)
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

**In Verwendung** (32774)
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

**Objekt ist vorhanden** (32788)
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

[**Msvm \_ ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

