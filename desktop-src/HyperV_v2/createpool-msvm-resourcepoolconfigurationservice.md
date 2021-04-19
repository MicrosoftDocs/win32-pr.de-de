---
description: Erstellt einen untergeordneten Ressourcenpool.
ms.assetid: 30a70231-f1b7-4f0e-ac47-cf5a79ddb8ab
title: Die Methode "kreatepool" der Msvm_ResourcePoolConfigurationService-Klasse
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
ms.openlocfilehash: fb29a4b5a47d88232a6b0df6a828d482030b3f1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360654"
---
# <a name="createpool-method-of-the-msvm_resourcepoolconfigurationservice-class"></a>Die Methode "kreatepool" der Klasse "MSVM \_ resourcepoolconfigurationservice"

Erstellt einen untergeordneten Ressourcenpool. Der Ressourcenpool wird auf dasselbe System wie dieser Dienst beschränkt. Der sich ergebende Pool ist ein untergeordneter Pool.

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

*Poolsettings* \[ in\]
</dt> <dd>

Eine eingebettete Instanz der [**MSVM \_ resourcepoolsettingdata**](msvm-resourcepoolsettingdata.md) -Klasse, die verwendet wird, um die Pool Einstellungen anzugeben, die nicht zugeordnet sind.

</dd> <dt>

"Parser"- *Pools* \[ in\]
</dt> <dd>

Ein Array von [**MSVM- \_ resourcepool**](msvm-resourcepool.md) -verweisen, die den Pool oder die Pools darstellen, aus denen der neue Pool erstellt werden soll.

</dd> <dt>

*Zuordnung von Einstellungen* \[ in\]
</dt> <dd>

Ein Array aus mindestens einer eingebetteten Instanz der [**MSVM \_ resourceallocationsettingdata**](msvm-resourceallocationsettingdata.md) -Klasse, die verwendet wird, um die Einstellungen für die Pool Zuordnung anzugeben. Dieses Array muss entweder ein-Element für jedes Element im *parentpools* -Array oder genau ein Element enthalten. Wenn dieses Array ein Element enthält und *parentpools* mehr als ein Element enthält, gibt *alllocationsettings* eine freigegebene Kapazitäts Zuordnung an, die von einem der übergeordneten Pools erfüllt werden kann.

Hiermit werden die Ressourcen, die vom untergeordneten dem Pool zugewiesen werden können, auf eine niedrigere Grenze beschränkt als die von den übergeordneten Elementen bereitgestellte Aggregat Kapazität. Diese Option wird nicht von allen Ressourcentypen unterstützt. Wenn ein Ressourcentyp keine freigegebene Kapazitäts Zuordnung unterstützt, gibt diese Methode 32770 zurück (wird nicht unterstützt).

</dd> <dt>

*Pool* \[ vorgenommen\]
</dt> <dd>

Ein Verweis auf den resultierenden Pool.

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

 

