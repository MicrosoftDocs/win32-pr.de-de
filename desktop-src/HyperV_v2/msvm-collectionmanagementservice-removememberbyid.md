---
description: Entfernt das angegebene verwaltete Element als Member der CIM \_ CollectionOfMSEs mit dem angegebenen Bezeichner. Dies ist auch dann erfolgreich, wenn das Objekt mit diesem Bezeichner nicht vorhanden ist.
ms.assetid: 641535f0-ce71-4f57-a4e1-4775b3bb2374
title: RemoveMemberById-Methode der Msvm_CollectionManagementService-Klasse
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
ms.openlocfilehash: e371962198ea5a27228706a8b8ae7e65a30a9a8af4e5c3faa8276f7946cf4932
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682030"
---
# <a name="removememberbyid-method-of-the-msvm_collectionmanagementservice-class"></a>RemoveMemberById-Methode der Msvm \_ CollectionManagementService-Klasse

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

*Mitglied* \[ In\]
</dt> <dd>

Der zu entfernende Member.

</dd> <dt>

*CollectionId* \[ In\]
</dt> <dd>

Die Sammlungs-ID der Auflistung, aus der der Member entfernt werden soll.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Ein Verweis auf den Auftrag (kann NULL sein, wenn der Task abgeschlossen ist).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 oder 4096 zurück, wenn der Auftrag gestartet wurde. andernfalls wird ein Fehler zurückgegeben.

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

[**Msvm \_ CollectionManagementService**](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




