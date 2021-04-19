---
description: Ruft Informationen zu einer VHD-Momentaufnahme in einer VHD-Datei ab.
ms.assetid: 43745935-9bc3-4a87-8762-54693b2cdef6
title: Getvhdsnapshotinformation-Methode der Msvm_ImageManagementService-Klasse
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
ms.openlocfilehash: 85ea18e2be5329345ba49f4956307c4b29134ed6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347805"
---
# <a name="getvhdsnapshotinformation-method-of-the-msvm_imagemanagementservice-class"></a>Getvhdsnapshotinformation-Methode der MSVM \_ imagemanagementservice-Klasse

Ruft Informationen zu einer VHD-Momentaufnahme in einer VHD-Datei ab.

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

*Vhdsetpath* \[ in\]
</dt> <dd>

Ein voll qualifizierter Pfad, der den Speicherort der VHD-Satz Datei angibt.

</dd> <dt>

*Snapshotids* \[ in\]
</dt> <dd>

Eine Liste von GUIDs, die die Momentaufnahme-IDs der einzelnen Momentaufnahmen darstellen, für die Informationen angefordert werden. Wenn dieser Parameter NULL ist, werden Informationen für alle Momentaufnahmen abgerufen.

</dd> <dt>

*AdditionalInformation* \[ in\]
</dt> <dd>

Ein Array, das angibt, welche zusätzlichen Informationen zu den einzelnen VHD-Momentaufnahmen gesammelt werden sollen. Jeder Eintrag im Array ist ein Typ zusätzlicher Informationen. Wenn dieser Parameter NULL ist, werden keine zusätzlichen Informationen abgerufen.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Parent_Paths"></span><span id="parent_paths"></span><span id="PARENT_PATHS"></span>

Über **geordnete Pfade** (2)


</dt> <dd></dd> </dl> </dd> <dt>

*Snapshotinformation* \[ vorgenommen\]
</dt> <dd>

Bei erfolgreicher Ausführung ein Array von Informationen über die einzelnen angeforderten Momentaufnahmen. Jedes Element ist eine eingebettete Instanz von [**MSVM \_ vhdsnapshotinformation**](msvm-vhdsnapshotinformation.md).

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Ein Verweis auf den Auftrag (kann NULL sein, wenn die Aufgabe abgeschlossen ist).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück:

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)
</dt> <dt>

Fehler **(32768** )
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

Der **Status ist "Unknown** " (32771).
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger Parameter** (32773)
</dt> <dt>

**System wird verwendet** (32774)
</dt> <dt>

**Ungültiger Status für diesen Vorgang** (32775).
</dt> <dt>

**Falscher Datentyp** (32776).
</dt> <dt>

Das **System ist nicht verfügbar** (32777).
</dt> <dt>

**Nicht** genügend Arbeitsspeicher (32778)
</dt> <dt>

Die **Datei wurde nicht gefunden** (32779).
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

[**MSVM \_ imagemanagementservice**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




