---
description: Erstellt einen Referenzpunkt eines virtuellen Systems.
ms.assetid: 9cc7665a-9562-4267-bcd0-3162e426fbad
title: Die Methode "kreatereferencepoint" der Msvm_VirtualSystemReferencePointService-Klasse
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
ms.openlocfilehash: 08d28970288ba62346894d758ebac5ac156962ff
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106354908"
---
# <a name="createreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a>Methode "kreatereferencepoint" der Klasse "MSVM \_ virtualsystemreferencepointservice"

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

*Affectedsystem* \[ in\]
</dt> <dd>

Ein [**MSVM- \_ Computersystem**](msvm-computersystem.md) , das auf das betroffene virtuelle System verweist.

</dd> <dt>

*Referencepointsettings* \[ in\]
</dt> <dd>

Enthält die Parametereinstellungen.

</dd> <dt>

*Referencepointtype* \[ in\]
</dt> <dd>

Angeforderter Verweis Punkttyp:

<dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Protokoll basiert** (0)


</dt> <dd>

Basierend auf der Protokoll Verfolgung von Hyper-V-Replikaten.

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT basierend** (1)


</dt> <dd>

Basierend auf robusten Änderungsnachverfolgung von virtuellen Datenträgern.

</dd> </dl> </dd> <dt>

*Resultingreferencepoint* \[ in, out\]
</dt> <dd>

Resultierender virtueller System-Referenzpunkt

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Wenn der Vorgang lange ausgeführt wird, kann optional ein Auftrag zurückgegeben werden. In diesem Fall wird die Instanz der " [**MSVM \_ virtualsystemreferencepoint**](msvm-virtualsystemreferencepoint.md) "-Klasse, die den neuen virtuellen System Verweis Punkt darstellt, über die [**CIM- \_ affectedjobelements**](cim-affectedjobelement.md) -Zuordnung mit dem Wert der **affectedelta** -Eigenschaft, die auf die neue Instanz der **MSVM \_ virtualsystemreferencepoint** -Klasse verweist, die den Verweis Punkt des virtuellen Systems und den Wert der **elementeffects** auf 5 (Create) festgelegt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg wird 0 zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.

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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ virtualsystemreferencepointservice**](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




