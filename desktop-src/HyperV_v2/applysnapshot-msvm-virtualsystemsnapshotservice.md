---
description: Wendet eine Momentaufnahme des virtuellen Computers auf den virtuellen Computer an, auf dem Sie erstellt wurde.
ms.assetid: 45f1ec8f-aa96-4060-8f8c-0471d0ad4a21
title: Applysnapshot-Methode der Msvm_VirtualSystemSnapshotService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.ApplySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 735e827935689a0f0ede7fbac1d582ea40772ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865223"
---
# <a name="applysnapshot-method-of-the-msvm_virtualsystemsnapshotservice-class"></a>Applysnapshot-Methode der MSVM \_ virtualsystemsnapshotservice-Klasse

Wendet eine Momentaufnahme des virtuellen Computers auf den virtuellen Computer an, auf dem Sie erstellt wurde.

## <a name="syntax"></a>Syntax


```mof
uint32 ApplySnapshot(
  [in]  CIM_VirtualSystemSettingData REF Snapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Momentaufnahme* \[ in\]
</dt> <dd>

Ein Verweis auf eine von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85)) abgeleitete Klasse, die die anzuwendende Momentaufnahme des virtuellen Computers darstellt.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Dieser Vorgang wird immer asynchron ausgeführt. Diese Methode gibt 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.

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

**Zugriff verweigert** (32769)
</dt> <dt>

**Ungültiger Parameter** (32773)
</dt> <dt>

**Ungültiger Status** (32775)
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

[**Applyvirtualsystemsnapshot (v1)**](/previous-versions/windows/desktop/virtual/applyvirtualsystemsnapshot-msvm-virtualsystemmanagementservice)
</dt> <dt>

[**Applyvirtualsystemsnapshotex (v1)**](/previous-versions/windows/desktop/virtual/msvm-virtualsystemmanagementservice-applyvirtualsystemsnapshotex)
</dt> </dl>

 

