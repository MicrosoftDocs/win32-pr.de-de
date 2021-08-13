---
description: Erstellt eine Momentaufnahme einer Sammlung virtueller Systeme.
ms.assetid: 2512d82f-06b9-4613-b920-d3a9be884a75
title: CreateSnapshot-Methode der Msvm_CollectionSnapshotService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 251213d0ff7a98d922a4dec761252479f911e66e2304596a97858fe0b7dc5fbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119426910"
---
# <a name="createsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a>CreateSnapshot-Methode der Msvm \_ CollectionSnapshotService-Klasse

Erstellt eine Momentaufnahme einer Sammlung virtueller Systeme.

## <a name="syntax"></a>Syntax


```mof
uint32 CreateSnapshot(
  [in]      CIM_CollectionOfMSEs REF Collection,
  [in]      string                   SnapshotSettings,
  [in]      uint16                   SnapshotType,
  [in, out] CIM_Collection       REF ResultingSnapshotCollection,
  [out]     CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Sammlung* \[ In\]
</dt> <dd>

Verweis auf eine [**\_ CIM-CollectionOfMSEs,**](cim-collectionofmses.md) die die betroffene Sammlung virtueller Systeme beschreibt.

</dd> <dt>

*SnapshotSettings* \[ In\]
</dt> <dd>

Enthält die Parametereinstellungen.

</dd> <dt>

*SnapshotType* \[ In\]
</dt> <dd>

Angeforderter Momentaufnahmetyp:

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>

<span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>**Standardmomentaufnahme** (1)


</dt> <dd>

Standardmomentaufnahme des virtuellen Systems.

</dd> <dt>

<span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>

<span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>**Wiederherstellungsmomentaufnahme** (2)


</dt> <dd>

Momentaufnahme für Wiederherstellungsszenarien, einschließlich Failoverreplikation und Sicherung.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Herstellerspezifisch** (32768..65535)


</dt> <dd></dd> </dl> </dd> <dt>

*ResultingSnapshotCollection* \[ in, out\]
</dt> <dd>

Bei Erfolg wird ein [**\_ CIM-Sammlungsverweis**](cim-collection.md) zurückgegeben, der die Momentaufnahme des virtuellen Systems enthält.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Ein optionaler Verweis, der zurückgegeben wird, wenn der Vorgang asynchron ausgeführt wird. Falls vorhanden, kann der zurückgegebene Verweis auf eine Instanz von [**CIM \_ ConcreteJob**](cim-concretejob.md) verwendet werden, um den Fortschritt zu überwachen und das Ergebnis der -Methode zu erhalten.

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



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**Msvm \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




