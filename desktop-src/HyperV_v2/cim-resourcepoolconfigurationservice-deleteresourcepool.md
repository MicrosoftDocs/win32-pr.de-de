---
description: Starten Sie einen Auftrag, um einen Ressourcenpool zu löschen.
ms.assetid: af3d9c7c-a825-4568-822d-044b3d92d144
title: Deleteresourcepool-Methode der CIM_ResourcePoolConfigurationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.DeleteResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9cab27df07a6a3a9679cb5e6595b6ba558d8b05e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357371"
---
# <a name="deleteresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Deleteresourcepool-Methode der CIM \_ resourcepoolconfigurationservice-Klasse

Starten Sie einen Auftrag, um einen Ressourcenpool zu löschen. Möglicherweise sind keine Zuordnungen ausstehend, oder der Löschvorgang schlägt fehl mit "in Verwendung". Wenn es sich beim Ressourcenpool um einen Stamm Ressourcenpool handelt, werden alle Host Ressourcen an das zugrunde liegende System zurückgegeben.

## <a name="syntax"></a>Syntax


```mof
uint32 DeleteResourcePool(
  [in]  CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pool* \[ in\]
</dt> <dd>

Ein [**CIM- \_ resourcepool**](cim-resourcepool.md) , der auf den zu löschenden Pool verweist.

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

[**CIM \_ resourcepoolconfigurationservice**](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




