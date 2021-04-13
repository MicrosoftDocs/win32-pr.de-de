---
description: Entfernt das angegebene verwaltete Element als Member der CIM \_ CollectionOfMSEs mit dem angegebenen Bezeichner. Dies ist auch dann erfolgreich, wenn das Objekt mit diesem Bezeichner nicht vorhanden ist.
ms.assetid: 641535f0-ce71-4f57-a4e1-4775b3bb2374
title: Removemembership byid-Methode der Msvm_CollectionManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.RemoveMemberById
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 31c30d8698b16ac9bf128aa13ab80a64f09a40c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218699"
---
# <a name="removememberbyid-method-of-the-msvm_collectionmanagementservice-class"></a>Removemembership byid-Methode der MSVM \_ collectionmanagementservice-Klasse

Entfernt das angegebene verwaltete Element als Member der [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) mit dem angegebenen Bezeichner. Dies ist auch dann erfolgreich, wenn das Objekt mit diesem Bezeichner nicht vorhanden ist.

## <a name="syntax"></a>Syntax


```mof
uint32 RemoveMemberById(
  [in]  CIM_ManagedElement REF Member,
  [in]  string                 CollectionId,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Mitglied* \[ in\]
</dt> <dd>

Der zu entfernende Member.

</dd> <dt>

*CollectionId* \[ in\]
</dt> <dd>

Die Sammlungs-ID der Auflistung, aus der das Element entfernt werden soll.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Ein Verweis auf den Auftrag (kann NULL sein, wenn die Aufgabe abgeschlossen ist).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 zurück, wenn erfolgreich, oder 4096, wenn der Auftrag gestartet wurde. Andernfalls wird ein Fehler zurückgegeben.

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

[**MSVM \_ collectionmanagementservice**](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




