---
description: Löscht einen VHD-Momentaufnahmeeintrag in einer VHD-Set-Datei.
ms.assetid: 37d55a5f-209d-42ce-8f69-8b494055e263
title: DeleteVHDSnapshot-Methode der Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.DeleteVHDSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 45a15b03b3ca26375ef0a563981cb9405c4397f355735c173e105029959d8282
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119522660"
---
# <a name="deletevhdsnapshot-method-of-the-msvm_imagemanagementservice-class"></a>DeleteVHDSnapshot-Methode der Msvm \_ ImageManagementService-Klasse

Löscht einen VHD-Momentaufnahmeeintrag in einer VHD-Set-Datei.

## <a name="syntax"></a>Syntax


```mof
uint32 DeleteVHDSnapshot(
  [in]  string              VHDSetPath,
  [in]  string              SnapshotId,
  [in]  boolean             PersistReferenceSnapshot,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*VHDSetPath* \[ In\]
</dt> <dd>

Eine Zeichenfolge, die den Pfad zur VHD-Set-Datei mit der in Frage gestellten Momentaufnahme enthält.

</dd> <dt>

*SnapshotId* \[ In\]
</dt> <dd>

Eine GUID, die die Momentaufnahme-ID für den zu löschenden VHD-Momentaufnahmeeintrag darstellt.

</dd> <dt>

*PersistReferenceSnapshot* \[ In\]
</dt> <dd>

Gibt an, ob ein Nur-Verweis-Momentaufnahmedatensatz beibehalten werden soll, nachdem die Momentaufnahme gelöscht wurde.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Ein Verweis auf den Auftrag (kann NULL sein, wenn der Task abgeschlossen ist).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück:

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Überprüfte Methodenparameter – Auftrag gestartet** (4096)
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

**Ungültiger** Parameter (32773)
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

[**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




