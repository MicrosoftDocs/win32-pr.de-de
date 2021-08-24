---
description: Sucht ein Msvm \_ MountedStorageImage-Objekt für einen bestimmten Datenträgerimagepfad.
ms.assetid: 498ed285-2b5b-472b-b0ee-649c97b61274
title: FindMountedStorageImageInstance-Methode der Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.FindMountedStorageImageInstance
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: de205cb729b9ad53674808523cc640b9aaccb2adfaf6fba0b8a06c8a0d8952f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119522630"
---
# <a name="findmountedstorageimageinstance-method-of-the-msvm_imagemanagementservice-class"></a>FindMountedStorageImageInstance-Methode der Msvm \_ ImageManagementService-Klasse

Sucht ein [**Msvm \_ MountedStorageImage-Objekt**](msvm-mountedstorageimage.md) für einen bestimmten Datenträgerimagepfad.

## <a name="syntax"></a>Syntax


```mof
uint32 FindMountedStorageImageInstance(
  [in]  string                       SelectionCriterion,
  [in]  uint16                       CriterionType,
  [out] Msvm_MountedStorageImage REF Image
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SelectionCriterion* \[ In\]
</dt> <dd>

Ein vollqualifiziertes Pfad, der den Speicherort einer Datenträgerimagedatei angibt.

</dd> <dt>

*CriterionType* \[ In\]
</dt> <dd>

Der Typ des Kriteriums, nach dem gesucht werden soll, wenn das Datenträgerimage gefunden wird.

<dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

**unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>

**Pfad** (2)


</dt> <dd></dd> </dl> </dd> <dt>

*Abbildung:* \[ out\]
</dt> <dd>

Ein Verweis auf [**das Msvm \_ MountedStorageImage**](msvm-mountedstorageimage.md) (kann NULL sein, wenn das Image nicht eingebunden ist).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück:

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Fehler** (32768)
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

**Status ist unbekannt** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger Parameter** (32773)
</dt> <dt>

**System wird verwendet** (32774)
</dt> <dt>

**Ungültiger Zustand für diesen Vorgang** (32775)
</dt> <dt>

**Falscher Datentyp** (32776)
</dt> <dt>

**System ist nicht verfügbar** (32777)
</dt> <dt>

**Nicht genügend Arbeitsspeicher** (32778)
</dt> <dt>

**Datei nicht gefunden** (32779)
</dt> <dt>

**Objekt nicht gefunden** (32789)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




