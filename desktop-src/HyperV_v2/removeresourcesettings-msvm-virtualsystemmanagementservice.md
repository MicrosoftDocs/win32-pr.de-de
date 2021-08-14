---
description: Entfernt Einstellungen für virtuelle Ressourcen aus der Konfiguration eines virtuellen Computers.
ms.assetid: 74d9a70a-5258-4e4b-8131-b25513d11a4b
title: RemoveResourceSettings-Methode der Msvm_VirtualSystemManagementService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0a55dd7fa6091257fc2bd81e3b8755c9cfb68a4e0830a99c9d0f3727cd0b35c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980030"
---
# <a name="removeresourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>RemoveResourceSettings-Methode der Msvm \_ VirtualSystemManagementService-Klasse

Entfernt Einstellungen für virtuelle Ressourcen aus der Konfiguration eines virtuellen Computers. Wenn sie auf Teile einer aktuellen Konfiguration eines virtuellen Computers angewendet wird, wird der aktive virtuelle Computer möglicherweise entfernt.

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

Ein Array von Verweisen auf Instanzen der [**\_ CIM-Klasse ResourceAllocationSettingData,**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) wobei jede Instanz die Einstellungen einer virtuellen Ressource innerhalb einer Konfiguration des virtuellen Computers darstellt, die entfernt werden sollen.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ ConcreteJob abgeleitet wurde.**](/previous-versions//cc136808(v=vs.85))

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

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

**Überprüfte Methodenparameter – Auftrag gestartet** (4096)
</dt> <dt>

**DMTF Reserved** (..)
</dt> <dt>

**Reservierte Methode** (4097..32767)
</dt> <dt>

**Herstellerspezifisch** (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

