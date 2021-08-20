---
description: Konvertieren sie eine vorhandene Momentaufnahme des virtuellen Systems in einen Referenzpunkt. Die Momentaufnahme wird als Nebeneffekt gelöscht. Nur Wiederherstellungsmomentaufnahmen können in Verweispunkte konvertiert werden.
ms.assetid: c634d749-e18f-4a11-a574-2aee705c0722
title: ConvertToReferencePoint-Methode der Msvm_VirtualSystemSnapshotService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.ConvertToReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2ae910dee449af4c47afa80622f0f4d431631e05b5e01fd419241bccd7b12548
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117993886"
---
# <a name="converttoreferencepoint-method-of-the-msvm_virtualsystemsnapshotservice-class"></a>ConvertToReferencePoint-Methode der Msvm \_ VirtualSystemSnapshotService-Klasse

Konvertieren sie eine vorhandene Momentaufnahme des virtuellen Systems in einen Referenzpunkt. Die Momentaufnahme wird als Nebeneffekt gelöscht. Nur Wiederherstellungsmomentaufnahmen können in Verweispunkte konvertiert werden.

## <a name="syntax"></a>Syntax


```mof
uint32 ConvertToReferencePoint(
  [in]      CIM_VirtualSystemSettingData     REF AffectedSnapshot,
  [in]      string                               ReferencePointSettings,
  [in, out] Msvm_VirtualSystemReferencePoint REF ResultingReferencePoint,
  [out]     CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AffectedSnapshot* \[ In\]
</dt> <dd>

Verweis auf die betroffene Momentaufnahme des virtuellen Systems.

</dd> <dt>

*ReferencePointSettings* \[ In\]
</dt> <dd>

Parametereinstellungen.

</dd> <dt>

*ResultingReferencePoint* \[ in, out\]
</dt> <dd>

Resultierender Referenzpunkt des virtuellen Systems

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang lange ausgeführt wird, kann optional ein Auftrag zurückgegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg eine 0 zurück. andernfalls gibt einen der folgenden Werte zurück:

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

[**Msvm \_ VirtualSystemSnapshotService**](msvm-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




