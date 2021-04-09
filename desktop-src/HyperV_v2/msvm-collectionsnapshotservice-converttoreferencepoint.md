---
description: Konvertiert eine vorhandene Auflistungs Momentaufnahme in eine Verweis Punkt Auflistung. Die Momentaufnahme Auflistung wird als Nebeneffekt gelöscht. Nur Wiederherstellungs Momentaufnahmen können in Verweis Punkte konvertiert werden.
ms.assetid: 6b304782-9e5e-43b1-af7d-08617d65850c
title: Converttoreferencepoint-Methode der Msvm_CollectionSnapshotService-Klasse
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
ms.openlocfilehash: 810761b67303ad33ced6fdaef857c96f65365091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869084"
---
# <a name="converttoreferencepoint-method-of-the-msvm_collectionsnapshotservice-class"></a>Converttoreferencepoint-Methode der MSVM \_ collectionsnapshotservice-Klasse

Konvertiert eine vorhandene Auflistungs Momentaufnahme in eine Verweis Punkt Auflistung. Die Momentaufnahme Auflistung wird als Nebeneffekt gelöscht. Nur Wiederherstellungs Momentaufnahmen können in Verweis Punkte konvertiert werden.

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

*Affectedsnapshotcollection* \[ in\]
</dt> <dd>

Verweis auf eine [**MSVM- \_ snapshotcollection**](msvm-snapshotcollection.md) , die die betroffene Sammlung virtueller System Momentaufnahmen enthält.

</dd> <dt>

*Resultingreferencepointcollection* \[ in, out\]
</dt> <dd>

Verweis auf eine [**MSVM \_ referencepointcollection**](msvm-referencepointcollection.md) , die die resultierende Verweis Punkt Auflistung des virtuellen Systems enthält

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Wenn der Vorgang lange ausgeführt wird, kann optional ein Auftrag zurückgegeben werden.

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

 

 




