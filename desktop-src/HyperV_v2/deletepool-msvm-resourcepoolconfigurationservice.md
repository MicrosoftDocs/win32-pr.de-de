---
description: Löscht einen Ressourcenpool.
ms.assetid: bc3111a4-9687-49ec-890e-190358230c53
title: DeletePool-Methode der Msvm_ResourcePoolConfigurationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.DeletePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 110c380973b500e8c89b399cd688a6624e7059dc14c711dd2b1e356c6fb07c1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118645727"
---
# <a name="deletepool-method-of-the-msvm_resourcepoolconfigurationservice-class"></a>DeletePool-Methode der Msvm \_ ResourcePoolConfigurationService-Klasse

Löscht einen Ressourcenpool. Um einen Ressourcenpool erfolgreich zu löschen, können keine Zuordnungen ausstehen, oder das Löschen schlägt mit 32774 (In Gebrauch) fehl. Wenn der Ressourcenpool ein Stammressourcenpool ist, werden alle Hostressourcen an das zugrunde liegende System zurückgegeben.

## <a name="syntax"></a>Syntax


```mof
uint32 DeletePool(
  [in]  CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pool* \[ In\]
</dt> <dd>

Ein Verweis auf eine Instanz der [**CIM \_ ResourcePool-Klasse,**](cim-resourcepool.md) die den zu löschende Pool darstellt.

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



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**Msvm \_ ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

