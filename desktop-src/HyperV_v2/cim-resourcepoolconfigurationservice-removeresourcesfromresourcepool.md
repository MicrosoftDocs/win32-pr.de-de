---
description: Startet einen Auftrag zum Entfernen von Ressourcen aus einem Ressourcenpool.
ms.assetid: 1689ccbf-a524-45b7-bf95-6341a3b28f6c
title: RemoveResourcesFromResourcePool-Methode der CIM_ResourcePoolConfigurationService Klasse
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
ms.openlocfilehash: 370944c9d8b8307a796b425dd4ff611429f59ccc72473a92528ef19b8c2f5910
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980870"
---
# <a name="removeresourcesfromresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>RemoveResourcesFromResourcePool-Methode der \_ CIM-Klasse "ResourcePoolConfigurationService"

Startet einen Auftrag zum Entfernen von Ressourcen aus einem Ressourcenpool.

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

*HostResources* \[ In\]
</dt> <dd>

Array von [**CIM \_ LogicalDevice-Instanzen,**](cim-logicaldevice.md) die aus dem Pool entfernt werden.

</dd> <dt>

*Pool* \[ In\]
</dt> <dd>

Ein [**\_ CIM-Ressourcenpool,**](cim-resourcepool.md) der den Pool darstellt, aus dem die Ressourcen entfernt werden.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Ein [**CIM \_ ConcreteJob,**](cim-concretejob.md) der auf den Auftrag verweist (kann **NULL sein,** wenn der Auftrag abgeschlossen ist).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg eine 0 zurück. andernfalls gibt einen Fehler zurück.

<dl> <dt>

**Auftrag ohne Fehler** abgeschlossen (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

**Unbekannt** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Fehler** (4)
</dt> <dt>

**Ungültiger Parameter** (5)
</dt> <dt>

**Wird verwendet** (6)
</dt> <dt>

**Falscher ResourceType für den Pool** (7)
</dt> <dt>

**DMTF Reserved** (..)
</dt> <dt>

**Überprüfte Methodenparameter – Auftrag gestartet** (4096)
</dt> <dt>

**Größe nicht unterstützt** (4097)
</dt> <dt>

**Reservierte Methode** (4098..32767)
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

[**CIM \_ ResourcePoolConfigurationService**](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




