---
description: Zerstört ein virtuelles System.
ms.assetid: 8d2504dc-ce23-4257-9dfd-6a35dfd84b2d
title: Destroysystem-Methode der CIM_VirtualSystemManagementService-Klasse
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
ms.openlocfilehash: 41355970bb70063b8e90deb8f49b5e6f4b439017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347925"
---
# <a name="destroysystem-method-of-the-cim_virtualsystemmanagementservice-class"></a>Destroysystem-Methode der CIM \_ virtualsystemmanagementservice-Klasse

Zerstört ein virtuelles System.

Das virtuelle System, auf das verwiesen wird, wird zerstört, einschließlich der Elemente, auf die es verweist. Virtuelle Ressourcen werden an Ihre Ressourcenpools zurückgegeben, was möglicherweise die Zerstörung dieser Ressourcen impliziert (implementierungsabhängig). Wenn das virtuelle System aktiv ist, wenn der Vorgang aufgerufen wird, wird es zuerst deaktiviert und anschließend zerstört. Wenn Momentaufnahmen aus dem virtuellen System erstellt wurden, werden diese ebenfalls zerstört.

## <a name="syntax"></a>Syntax


```mof
uint32 DestroySystem(
  [in]  CIM_ComputerSystem REF AffectedSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Affectedsystem* \[ in\]
</dt> <dd>

Verweis auf eine Instanz der Klasse " [**CIM \_ Computersystem**](cim-computersystem.md) ", die das virtuelle Computersystem darstellt, das zerstört werden soll.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Wenn der Vorgang lange ausgeführt wird, kann optional ein [**CIM-" \_ concretejob**](cim-concretejob.md) " zurückgegeben werden, der den Auftrag darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.

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
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ virtualsystemmanagementservice**](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




