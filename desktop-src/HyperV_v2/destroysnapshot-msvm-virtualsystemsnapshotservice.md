---
description: Zerstört eine vorhandene Momentaufnahme eines virtuellen Computers.
ms.assetid: 84752bb3-cae1-4a93-89bc-e735c058feda
title: Destroysnapshot-Methode der Msvm_VirtualSystemSnapshotService-Klasse
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
ms.openlocfilehash: 91c2e59baa8bb22f5ea9f128130d7dc440e28ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868231"
---
# <a name="destroysnapshot-method-of-the-msvm_virtualsystemsnapshotservice-class"></a>Destroysnapshot-Methode der MSVM \_ virtualsystemsnapshotservice-Klasse

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

*Affectedsnapshot* \[ in\]
</dt> <dd>

Ein [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85)) -Verweis, der die zu löschender Momentaufnahme des virtuellen Computers darstellt.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

Fehler **(2** )
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Ungültiger Parameter** (4)
</dt> <dt>

**Ungültiger Status** (5)
</dt> <dt>

**Ungültiger Typ** (6)
</dt> <dt>

**DMTF reserviert** (..)
</dt> <dt>

Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)
</dt> <dt>

**Reservierte Methode** (4097.32767)
</dt> <dt>

**Hersteller spezifisch** (32768.65535)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ virtualsystemsnapshotservice**](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[**Removevirtualsystemsnapshot (v1)**](/previous-versions/windows/desktop/virtual/removevirtualsystemsnapshot-msvm-virtualsystemmanagementservice)
</dt> </dl>

 

