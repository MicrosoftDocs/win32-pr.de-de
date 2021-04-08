---
description: Startet einen Auftrag, um einen Stamm Ressourcenpool zu erstellen. Der Bereich "resourcepool" wird auf dasselbe System wie dieser Dienst beschränkt.
ms.assetid: 357880dc-125a-452c-89f5-44cd17684436
title: Die Methode "kreateresourcepool" der CIM_ResourcePoolConfigurationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.CreateResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ca339eb2e2a4ec0fb441c5ed1a657608d71248bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752248"
---
# <a name="createresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Die Methode "samateresourcepool" der CIM \_ resourcepoolconfigurationservice-Klasse

Startet einen Auftrag, um einen Stamm Ressourcenpool zu erstellen. Der Bereich "resourcepool" wird auf dasselbe System wie dieser Dienst beschränkt.

## <a name="syntax"></a>Syntax


```mof
uint32 CreateResourcePool(
  [in]  string                ElementName,
  [in]  CIM_LogicalDevice REF HostResources[],
  [in]  string                ResourceType,
  [out] CIM_ResourcePool  REF Pool,
  [out] CIM_ConcreteJob   REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ElementName* \[ in\]
</dt> <dd>

Ein Endbenutzer relevanter Name für den Pool, der erstellt wird. Wenn der Wert **null** ist, kann ein vom System bereitgestellter Standardname verwendet werden. Der Wert wird in der **ElementName** -Eigenschaft für den erstellten Pool gespeichert.

</dd> <dt>

" *Hustresources* \[ " in\]
</dt> <dd>

Ein Array von 0 (null) oder mehr [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Geräten, die verwendet werden, um den Pool zu erstellen oder die Quell Blöcke zu ändern. Alle Elemente im Array müssen denselben Typ aufweisen.

</dd> <dt>

*ResourceType* \[in\]
</dt> <dd>

Der Typ der Ressourcen, die vom erstellten Pool verwaltet werden. Wenn " *hustresources* " Elemente enthält, muss diese Eigenschaft den Typ "" haben.

</dd> <dt>

*Pool* \[ vorgenommen\]
</dt> <dd>

Bei Erfolg wird ein Verweis auf den resultierenden [**CIM- \_ resourcepool zurückgegeben**](cim-resourcepool.md). Wenn ein Auftrag zurückgegeben wird, kann dieser **null** sein. in diesem Fall muss der Client den Auftrag verwenden, um den resultierenden resourcepool nach Abschluss des Auftrags zu ermitteln.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Verweis auf einen [**CIM- \_ concretejob**](cim-concretejob.md) , der den Auftrag darstellt (kann NULL sein, wenn der Auftrag abgeschlossen ist).

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

 

 




