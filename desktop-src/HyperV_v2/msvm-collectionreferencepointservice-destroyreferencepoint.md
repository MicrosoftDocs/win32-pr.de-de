---
description: Zerstört eine vorhandene Verweispunktsammlung. Diese Methode kann als Nebeneffekt andere Referenzpunkte zerstören, die von der betroffenen Verweispunktsammlung abhängig sind.
ms.assetid: 72c116f4-f844-494c-96ea-e97c49a2af7e
title: DestroyReferencePoint-Methode der Msvm_CollectionReferencePointService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.DestroyReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 95745646c410c2752f146fc05042b26215f41ef23d3637701497ad565e06583c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531990"
---
# <a name="destroyreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a>DestroyReferencePoint-Methode der Msvm \_ CollectionReferencePointService-Klasse

Zerstört eine vorhandene Verweispunktsammlung. Diese Methode kann als Nebeneffekt andere Referenzpunkte zerstören, die von der betroffenen Verweispunktsammlung abhängig sind.

## <a name="syntax"></a>Syntax


```mof
uint32 DestroyReferencePoint(
  [in]  CIM_Collection  REF AffectedReferencePointCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AffectedReferencePointCollection* \[ In\]
</dt> <dd>

Verweis auf die betroffene Auflistung des Referenzpunkts des virtuellen Systems.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang lange ausgeführt wird, kann optional ein Auftrag zurückgegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn erfolgreich, wird entweder 0 (kein Fehler) oder 4096 (Auftrag gestartet) zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ CollectionReferencePointService**](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




