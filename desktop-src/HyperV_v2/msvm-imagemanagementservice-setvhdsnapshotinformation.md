---
description: Bearbeitet einen VHD-Momentaufnahmeeintrag in einer VHD-Satzdatei. Wenn die momentaufnahme-ID bereits vorhanden ist, wird der vorhandene Momentaufnahmeeintrag durch den neuen Eintrag überschrieben. Andernfalls wird der neue Eintrag der VHD-Set-Datei hinzugefügt.
ms.assetid: dd14960d-3fb8-4d47-986f-fbbbb08eb37d
title: SetVHDSnapshotInformation-Methode der Msvm_ImageManagementService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetVHDSnapshotInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: af4adddb2b59da303f558cfffac61003e70e5767c77e381b13ba6089228d6643
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119522450"
---
# <a name="setvhdsnapshotinformation-method-of-the-msvm_imagemanagementservice-class"></a>SetVHDSnapshotInformation-Methode der Msvm \_ ImageManagementService-Klasse

Bearbeitet einen VHD-Momentaufnahmeeintrag in einer VHD-Satzdatei. Wenn die momentaufnahme-ID bereits vorhanden ist, wird der vorhandene Momentaufnahmeeintrag durch den neuen Eintrag überschrieben. Andernfalls wird der neue Eintrag der VHD-Set-Datei hinzugefügt.

## <a name="syntax"></a>Syntax


```mof
uint32 SetVHDSnapshotInformation(
  [in]  string              Information,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Informationen* \[ In\]
</dt> <dd>

VHD-Momentaufnahmeinformationen, die geändert oder in der VHD-Set-Datei hinzugefügt werden sollen. Die Zeichenfolge ist eine eingebettete Instanz von [**Msvm \_ VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md).

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

 

 




