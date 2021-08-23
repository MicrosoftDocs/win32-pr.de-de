---
description: Ändert die Einstellungen eines untergeordneten Pools, die nicht zuordnungsbezogen sind.
ms.assetid: f60068e0-f333-41e2-8f11-78aa48dfa260
title: ModifyPoolSettings-Methode der Msvm_ResourcePoolConfigurationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.ModifyPoolSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e1c8d71f8f380d5049d6bd2743e1f1d48573407431372c53aaeaacf4297ec56e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694040"
---
# <a name="modifypoolsettings-method-of-the-msvm_resourcepoolconfigurationservice-class"></a>ModifyPoolSettings-Methode der Msvm \_ ResourcePoolConfigurationService-Klasse

Ändert die Einstellungen eines untergeordneten Pools, die nicht zuordnungsbezogen sind.

## <a name="syntax"></a>Syntax


```mof
uint32 ModifyPoolSettings(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  string               PoolSettings,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ChildPool* \[ In\]
</dt> <dd>

Ein Verweis auf eine Instanz der [**CIM \_ ResourcePool-Klasse,**](cim-resourcepool.md) die den untergeordneten Pool darstellt, der geändert werden soll.

</dd> <dt>

*PoolSettings* \[ In\]
</dt> <dd>

Eine eingebettete Instanz der [**Msvm \_ ResourcePoolSettingData-Klasse,**](msvm-resourcepoolsettingdata.md) die zum Angeben der neuen Einstellungen für den Pool verwendet wird.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

