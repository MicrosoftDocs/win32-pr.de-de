---
description: Konvertiert eine vorhandene Sammlungsmomentaufnahme in eine Verweispunktsammlung. Die Momentaufnahmesammlung wird als Nebeneffekt gelöscht. Nur Wiederherstellungsmomentaufnahmen können in Verweispunkte konvertiert werden.
ms.assetid: 6b304782-9e5e-43b1-af7d-08617d65850c
title: ConvertToReferencePoint-Methode der Msvm_CollectionSnapshotService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ConvertToReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 97faedea1cdb852e26f6b94211586e5539075c0a225bf98f1a10cf45305d7296
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118148866"
---
# <a name="converttoreferencepoint-method-of-the-msvm_collectionsnapshotservice-class"></a>ConvertToReferencePoint-Methode der Msvm \_ CollectionSnapshotService-Klasse

Konvertiert eine vorhandene Sammlungsmomentaufnahme in eine Verweispunktsammlung. Die Momentaufnahmesammlung wird als Nebeneffekt gelöscht. Nur Wiederherstellungsmomentaufnahmen können in Verweispunkte konvertiert werden.

## <a name="syntax"></a>Syntax


```mof
uint32 ConvertToReferencePoint(
  [in]      Msvm_SnapshotCollection       REF AffectedSnapshotCollection,
  [in, out] Msvm_ReferencePointCollection REF ResultingReferencePointCollection,
  [out]     CIM_ConcreteJob               REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AffectedSnapshotCollection* \[ In\]
</dt> <dd>

Verweis auf eine [**Msvm \_ SnapshotCollection,**](msvm-snapshotcollection.md) die die betroffene Momentaufnahmesammlung des virtuellen Systems enthält.

</dd> <dt>

*ResultingReferencePointCollection* \[ in, out\]
</dt> <dd>

Verweis auf eine [**Msvm \_ ReferencePointCollection, die**](msvm-referencepointcollection.md) die resultierende Auflistung des Referenzpunkts des virtuellen Systems enthält

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang lange ausgeführt wird, kann optional ein Auftrag zurückgegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg wird entweder 0 (Abgeschlossen) oder 4096 (Auftrag gestartet) zurückgegeben. andernfalls gibt einen Fehler zurück.

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

**Ungültiger Typ** (6)
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
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




