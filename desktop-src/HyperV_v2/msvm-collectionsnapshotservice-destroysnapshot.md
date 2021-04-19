---
description: Zerstört eine vorhandene Momentaufnahme der virtuellen System Auflistung. Diese Methode kann als Nebeneffekt andere Momentaufnahmen zerstören, die von der betroffenen Momentaufnahme abhängig sind.
ms.assetid: 79a529d5-35bb-4e63-a1b7-8943de9580e8
title: Destroysnapshot-Methode der Msvm_CollectionSnapshotService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 399737a95db7725718b2e0ec620d2b6b7a7ae93e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345855"
---
# <a name="destroysnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a>Destroysnapshot-Methode der MSVM \_ collectionsnapshotservice-Klasse

Zerstört eine vorhandene Momentaufnahme der virtuellen System Auflistung. Diese Methode kann als Nebeneffekt andere Momentaufnahmen zerstören, die von der betroffenen Momentaufnahme abhängig sind.

## <a name="syntax"></a>Syntax


```mof
uint32 DestroySnapshot(
  [in]  CIM_Collection  REF AffectedSnapshotCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Affectedsnapshotcollection* \[ in\]
</dt> <dd>

Verweis auf eine [**CIM \_**](cim-collection.md) -Auflistung, die die betroffene Sammlung virtueller System Momentaufnahmen beschreibt.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Ein optionaler Verweis, der zurückgegeben wird, wenn der Vorgang asynchron ausgeführt wird. Falls vorhanden, kann der zurückgegebene Verweis auf eine Instanz von [**CIM \_ concretejob**](cim-concretejob.md) verwendet werden, um den Fortschritt zu überwachen und das Ergebnis der Methode abzurufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg wird entweder 0 (abgeschlossen) oder 4096 (Auftrag gestartet) zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.

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

**Ungültiger Status** (5)
</dt> <dt>

**Ungültiger Typ** (6)
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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ collectionsnapshotservice**](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




