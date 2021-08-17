---
description: Definiert ein geplantes virtuelles System.
ms.assetid: f129554b-e43e-4c3a-8418-d5d810f4c4b5
title: DefinePlannedSystem-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DefinePlannedSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 398f0c11f748cb9dc4865cb1ccb94f24409bda104bbcb55ec00ffde62a17188b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117810485"
---
# <a name="defineplannedsystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a>DefinePlannedSystem-Methode der Msvm \_ VirtualSystemManagementService-Klasse

Definiert ein geplantes virtuelles System.

Eingaben, die nicht vollständig angegeben sind, können mit Standardwerten ausgefüllt werden.

## <a name="syntax"></a>Syntax


```mof
uint32 DefinePlannedSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SystemSettings* \[ In\]
</dt> <dd>

Die Systemeinstellungen für das virtuelle System.

</dd> <dt>

*ResourceSettings* \[ In\]
</dt> <dd>

Die Ressourceneinstellungen für das virtuelle System.

</dd> <dt>

*ReferenceConfiguration* \[ In\]
</dt> <dd>

Eine [**CIM \_ VirtualSystemSettingData-Datei,**](cim-virtualsystemsettingdata.md) die die Referenzkonfiguration enthält.

</dd> <dt>

*ResultingSystem* \[ out\]
</dt> <dd>

Ein [**\_ CIM-Computersystem, das**](cim-computersystem.md) das resultierende System enthält.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein objekt, das von [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))abgeleitet wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 oder 4096 zurück. andernfalls wird ein Fehler zurückgegeben.

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

**DMTF Reserved** (..)
</dt> <dt>

**Überprüfte Methodenparameter – Auftragsstart** (4096)
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
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

