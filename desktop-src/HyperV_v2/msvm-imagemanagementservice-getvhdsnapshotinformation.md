---
description: Ruft Informationen zu einer VHD-Momentaufnahme in einer VHD-Set-Datei ab.
ms.assetid: 43745935-9bc3-4a87-8762-54693b2cdef6
title: GetVHDSnapshotInformation-Methode der Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVHDSnapshotInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: faac0c7b52d8e066ffa658a539a18d6423b50c861b772e536abca2aca010ea47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046630"
---
# <a name="getvhdsnapshotinformation-method-of-the-msvm_imagemanagementservice-class"></a>GetVHDSnapshotInformation-Methode der Msvm \_ ImageManagementService-Klasse

Ruft Informationen zu einer VHD-Momentaufnahme in einer VHD-Set-Datei ab.

## <a name="syntax"></a>Syntax


```mof
uint32 GetVHDSnapshotInformation(
  [in]  string              VHDSetPath,
  [in]  string              SnapshotIds[],
  [in]  uint32              AdditionalInformation[],
  [out] string              SnapshotInformation[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*VHDSetPath* \[ In\]
</dt> <dd>

Ein vollqualifizierten Pfad, der den Speicherort der VHD-Set-Datei angibt.

</dd> <dt>

*SnapshotIds* \[ In\]
</dt> <dd>

Eine Liste von GUIDs, die die Momentaufnahme-IDs jeder Momentaufnahme darstellen, für die Informationen angefordert werden. Wenn dieser Parameter NULL ist, werden Informationen für alle Momentaufnahmen abgerufen.

</dd> <dt>

*AdditionalInformation* \[ In\]
</dt> <dd>

Ein Array, das angibt, welche zusätzlichen Informationen zu jeder VHD-Momentaufnahme gesammelt werden sollen. Jeder Eintrag im Array ist ein Typ zusätzlicher Informationen. Wenn dieser Parameter NULL ist, werden keine zusätzlichen Informationen abgerufen.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Andere** (1)


</dt> <dd></dd> <dt>

<span id="Parent_Paths"></span><span id="parent_paths"></span><span id="PARENT_PATHS"></span>

**Übergeordnete Pfade** (2)


</dt> <dd></dd> </dl> </dd> <dt>

*SnapshotInformation* \[ out\]
</dt> <dd>

Bei Erfolg ein Array von Informationen zu jeder angeforderten Momentaufnahme. Jedes Element ist eine eingebettete Instanz von [**Msvm \_ VHDSnapshotInformation.**](msvm-vhdsnapshotinformation.md)

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

**Überprüfte Methodenparameter – Auftragsstart** (4096)
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

 

 




