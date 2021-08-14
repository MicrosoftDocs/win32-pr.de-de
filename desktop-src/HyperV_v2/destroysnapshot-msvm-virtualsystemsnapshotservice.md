---
description: Zerstört eine vorhandene Momentaufnahme eines virtuellen Computers.
ms.assetid: 84752bb3-cae1-4a93-89bc-e735c058feda
title: DestroySnapshot-Methode der Msvm_VirtualSystemSnapshotService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5ed582711b85fa51ceef6f5fb623a50089d80e0fb92e9eb12498efcd50840f56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393381"
---
# <a name="destroysnapshot-method-of-the-msvm_virtualsystemsnapshotservice-class"></a>DestroySnapshot-Methode der Msvm \_ VirtualSystemSnapshotService-Klasse

Zerstört eine vorhandene Momentaufnahme eines virtuellen Computers. Diese Methode kann als Nebeneffekt andere Momentaufnahmen zerstören, die von der betroffenen Momentaufnahme abhängig sind.

## <a name="syntax"></a>Syntax


```mof
uint32 DestroySnapshot(
  [in]  CIM_VirtualSystemSettingData REF AffectedSnapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AffectedSnapshot* \[ In\]
</dt> <dd>

Ein [**CIM \_ VirtualSystemSettingData-Verweis,**](/previous-versions//cc136954(v=vs.85)) der die zu zerstörende Momentaufnahme des virtuellen Computers darstellt.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ ConcreteJob abgeleitet wurde.**](/previous-versions//cc136808(v=vs.85))

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

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
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ VirtualSystemSnapshotService**](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[**RemoveVirtualSystemSnapshot (V1)**](/previous-versions/windows/desktop/virtual/removevirtualsystemsnapshot-msvm-virtualsystemmanagementservice)
</dt> </dl>

 

