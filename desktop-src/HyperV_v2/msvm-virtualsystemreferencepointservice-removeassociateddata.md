---
description: 'RemoveAssociatedData-Methode der Msvm_VirtualSystemReferencePointService-Klasse: Entfernt das dem Verweispunkt zugeordnete Datenprotokoll.'
ms.assetid: b6206bda-c195-4c6f-9b80-508c20b53ce5
title: RemoveAssociatedData-Methode der Msvm_VirtualSystemReferencePointService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.RemoveAssociatedData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3f8cef79e55379df1f91a0e1291144a7f4fdf92378e44cd9ed3588c83b3a3d4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147903"
---
# <a name="removeassociateddata-method-of-the-msvm_virtualsystemreferencepointservice-class"></a>RemoveAssociatedData-Methode der Msvm \_ VirtualSystemReferencePointService-Klasse

Entfernt das dem Verweispunkt zugeordnete Datenprotokoll.

## <a name="syntax"></a>Syntax


```mof
uint32 RemoveAssociatedData(
  [in]  Msvm_VirtualSystemReferencePoint REF AffectedReferencePoint,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AffectedReferencePoint* \[ In\]
</dt> <dd>

Ein Verweis auf die [**Msvm \_ VirtualSystemReferencePoint-Instanz,**](msvm-virtualsystemreferencepoint.md) die den zu entfernenden Verweispunkt darstellt.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Ein optionaler Parameter zum Überwachen des Vorgangsfortschritts, der verwendet wird, wenn die Methode nicht synchron ausgeführt werden konnte. Wenn der Vorgang asynchron ausgeführt wird, lautet der Rückgabewert 4096.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg wird 0 (Ohne Fehler abgeschlossen) oder 4096 (Auftrag gestartet) zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.

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
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




