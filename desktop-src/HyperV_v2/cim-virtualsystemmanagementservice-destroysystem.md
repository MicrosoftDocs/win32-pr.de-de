---
description: Zerstört ein virtuelles System.
ms.assetid: 8d2504dc-ce23-4257-9dfd-6a35dfd84b2d
title: DestroySystem-Methode der CIM_VirtualSystemManagementService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.DestroySystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fa7bf479e1e861e8425376fa0ebb610cd0b728cc9f02ba80acc9c1faa284fc16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980550"
---
# <a name="destroysystem-method-of-the-cim_virtualsystemmanagementservice-class"></a>DestroySystem-Methode der CIM \_ VirtualSystemManagementService-Klasse

Zerstört ein virtuelles System.

Das virtuelle System, auf das verwiesen wird, wird zerstört, einschließlich aller elemente, auf die es verweist. Virtuelle Ressourcen werden an ihre Ressourcenpools zurückgegeben, was die Zerstörung dieser Ressourcen (implementierungsabhängig) bedeuten kann. Wenn das virtuelle System aktiv ist, wenn der Vorgang aufgerufen wird, wird es zuerst deaktiviert und dann zerstört. Wenn Momentaufnahmen aus dem virtuellen System erstellt wurden, werden diese auch zerstört.

## <a name="syntax"></a>Syntax


```mof
uint32 DestroySystem(
  [in]  CIM_ComputerSystem REF AffectedSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AffectedSystem* \[ In\]
</dt> <dd>

Verweis auf eine Instanz der Klasse [**CIM \_ ComputerSystem,**](cim-computersystem.md) die das zu zerstörende virtuelle Computersystem darstellt.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang lange ausgeführt wird, kann optional ein [**CIM \_ ConcreteJob**](cim-concretejob.md) zurückgegeben werden, der den Auftrag darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg eine 0 zurück. andernfalls gibt einen Fehler zurück.

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

**Überprüfte Methodenparameter – Auftrag gestartet** (4096)
</dt> <dt>

**Reservierte Methode** (4097..32767)
</dt> <dt>

**Herstellerspezifisch** (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




