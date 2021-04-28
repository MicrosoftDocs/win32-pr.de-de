---
description: 'RemoveResourceSettings-Methode der CIM_VirtualSystemManagementService-Klasse: Entfernt Einstellungen für virtuelle Ressourcen aus einer Konfiguration des virtuellen Systems.'
ms.assetid: 7934a5e4-f54c-43fd-9ec3-d1fc1aad0acd
title: RemoveResourceSettings-Methode der CIM_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.RemoveResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e5c7daabcdcd732c3a5693664e1768ebf66668d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112258"
---
# <a name="removeresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a>RemoveResourceSettings-Methode der CIM \_ VirtualSystemManagementService-Klasse

Entfernt Einstellungen für virtuelle Ressourcen aus einer Konfiguration des virtuellen Systems.

Wenn sie auf Teile einer "aktuellen" Konfiguration des virtuellen Systems angewendet werden, können ressourcen des aktiven virtuellen Systems als Nebeneffekt entfernt werden.

## <a name="syntax"></a>Syntax


```mof
uint32 RemoveResourceSettings(
  [in]  CIM_ResourceAllocationSettingData REF ResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ResourceSettings* \[ In\]
</dt> <dd>

Array von Verweisen auf Instanzen der [**Cim \_ ResourceAllocationSettingData-Klasse,**](cim-resourceallocationsettingdata.md) wobei jede Instanz die Einstellungen einer virtuellen Ressource innerhalb einer konfiguration des virtuellen Systems darstellt, die entfernt werden sollen.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang lange ausgeführt wird, kann optional ein [**CIM \_ ConcreteJob**](cim-concretejob.md) zurückgegeben werden, der den Auftrag darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Wert 0 zurück. andernfalls wird ein Fehler zurückgegeben.

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

**DMTF Reserved** (..)
</dt> <dt>

**Methodenparameter überprüft** – Auftrag gestartet (4096)
</dt> <dt>

**Reservierte Methode** (4097..32767)
</dt> <dt>

**Herstellerspezifisch** (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




