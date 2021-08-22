---
description: Erstellt einen Referenzpunkt eines virtuellen Systems.
ms.assetid: 9cc7665a-9562-4267-bcd0-3162e426fbad
title: CreateReferencePoint-Methode der Msvm_VirtualSystemReferencePointService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.CreateReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fdcf4680ff10bdc8135fae4ec3bb9f81d53c26092e7196e73965ee4f4d87991f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014478"
---
# <a name="createreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a>CreateReferencePoint-Methode der Msvm \_ VirtualSystemReferencePointService-Klasse

Erstellt einen Referenzpunkt eines virtuellen Systems.

## <a name="syntax"></a>Syntax


```mof
uint32 CreateReferencePoint(
  [in]      Msvm_ComputerSystem              REF AffectedSystem,
  [in]      string                               ReferencePointSettings,
  [in]      uint16                               ReferencePointType,
  [in, out] Msvm_VirtualSystemReferencePoint REF ResultingReferencePoint,
  [out]     CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AffectedSystem* \[ In\]
</dt> <dd>

Ein [**\_ Msvm-Computersystem,**](msvm-computersystem.md) das auf das betroffene virtuelle System verweist.

</dd> <dt>

*ReferencePointSettings* \[ In\]
</dt> <dd>

Enthält die Parametereinstellungen.

</dd> <dt>

*ReferencePointType* \[ In\]
</dt> <dd>

Angeforderter Referenzpunkttyp:

<dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Protokollbasiertes** Protokoll (0)


</dt> <dd>

Basierend auf der Nachverfolgung von Hyper-V-Replikatprotokollen.

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT-basiert** (1)


</dt> <dd>

Basierend auf resilienten Änderungsnachverfolgung virtuellen Datenträgern.

</dd> </dl> </dd> <dt>

*ResultingReferencePoint* \[ in, out\]
</dt> <dd>

Resultierender Referenzpunkt des virtuellen Systems

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang lange ausgeführt wird, kann optional ein Auftrag zurückgegeben werden. In diesem Fall wird die Instanz der [**Msvm \_ VirtualSystemReferencePoint-Klasse,**](msvm-virtualsystemreferencepoint.md) die den neuen Referenzpunkt des virtuellen Systems darstellt, über die [**CIM \_ AffectedJobElement-Zuordnung**](cim-affectedjobelement.md) mit dem Wert der **AffectedElement-Eigenschaft** dargestellt, die auf die neue Instanz der **Msvm \_ VirtualSystemReferencePoint-Klasse** verweist, die den Referenzpunkt des virtuellen Systems und den Wert der **ElementEffects** darstellt, die auf 5 (Create) festgelegt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg gibt 0 zurück. andernfalls gibt einen Fehler zurück.

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

[**Msvm \_ VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




