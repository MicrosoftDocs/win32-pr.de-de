---
description: Legt die Konfigurationsdaten für die ersten virtuellen Computer fest.
ms.assetid: 0f174d29-ddb2-4a8c-b664-926245573778
title: Setinitialmachineconfigurationdata-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.SetInitialMachineConfigurationData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 08028358d6bb53406abe15c88e0acd02e748d387
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750177"
---
# <a name="setinitialmachineconfigurationdata-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Setinitialmachineconfigurationdata-Methode der MSVM \_ virtualsystemmanagementservice-Klasse

Legt die anfänglichen Computer Konfigurationsdaten eines virtuellen Computers fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetInitialMachineConfigurationData(
  [in]  CIM_ComputerSystem REF TargetSystem,
  [in]  uint8                  ImcData[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*TARGETSYSTEM* \[ in\]
</dt> <dd>

Ein Verweis auf das virtuelle Computersystem, auf dem die IMC-Daten festgelegt werden.

</dd> <dt>

*Imcdata* \[ in\]
</dt> <dd>

Die festzulegenden IMC-Daten. Die ersten vier Bytes müssen die Länge des Arrays in der Big-d-Reihenfolge aufweisen.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Ein optionaler Parameter zum Überwachen des Fortschritts des Vorgangs, der verwendet wird, wenn die Methode nicht synchron ausgeführt werden konnte. Wenn der Vorgang asynchron ausgeführt wird, ist der Rückgabewert 4096.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg wird 0 oder 4096 zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)
</dt> <dt>

Fehler **(32768** )
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

Der **Status ist "Unknown** " (32771).
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger Parameter** (32773)
</dt> <dt>

**System wird verwendet** (32774)
</dt> <dt>

**Ungültiger Status für diesen Vorgang** (32775).
</dt> <dt>

**Falscher Datentyp** (32776).
</dt> <dt>

Das **System ist nicht verfügbar** (32777).
</dt> <dt>

**Nicht** genügend Arbeitsspeicher (32778)
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

[**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




