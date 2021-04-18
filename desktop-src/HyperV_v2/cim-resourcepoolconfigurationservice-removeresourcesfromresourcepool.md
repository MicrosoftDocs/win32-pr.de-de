---
description: Startet einen Auftrag, um Ressourcen aus einem Ressourcenpool zu entfernen.
ms.assetid: 1689ccbf-a524-45b7-bf95-6341a3b28f6c
title: Removeresourcesfromresourcepool-Methode der CIM_ResourcePoolConfigurationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.RemoveResourcesFromResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 41c8a7d1608b9c4d5ea629aa9c053e022d59d9ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526783"
---
# <a name="removeresourcesfromresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Removeresourcesfromresourcepool-Methode der CIM \_ resourcepoolconfigurationservice-Klasse

Startet einen Auftrag, um Ressourcen aus einem Ressourcenpool zu entfernen.

## <a name="syntax"></a>Syntax


```mof
uint32 RemoveResourcesFromResourcePool(
  [in]  CIM_LogicalDevice REF HostResources[],
  [in]  CIM_ResourcePool  REF Pool,
  [out] CIM_ConcreteJob   REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

" *Hustresources* \[ " in\]
</dt> <dd>

Array von [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Instanzen, die aus dem Pool entfernt werden sollen.

</dd> <dt>

*Pool* \[ in\]
</dt> <dd>

Ein [**CIM- \_ resourcepool**](cim-resourcepool.md) , der den Pool darstellt, aus dem die Ressourcen entfernt werden sollen.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Ein [**CIM- \_ bettejob**](cim-concretejob.md) , der auf den Auftrag verweist (kann **null** sein, wenn der Auftrag abgeschlossen ist).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.

<dl> <dt>

**Auftrag ohne Fehler abgeschlossen** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

**Unbekannt** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

Fehler **(4** )
</dt> <dt>

**Ungültiger Parameter** (5)
</dt> <dt>

**In Gebrauch** (6)
</dt> <dt>

**Falscher ResourceType für den Pool** (7).
</dt> <dt>

**DMTF reserviert** (..)
</dt> <dt>

Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)
</dt> <dt>

**Größe nicht unterstützt** (4097)
</dt> <dt>

**Reservierte Methode** (4098.32767)
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

[**CIM \_ resourcepoolconfigurationservice**](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




