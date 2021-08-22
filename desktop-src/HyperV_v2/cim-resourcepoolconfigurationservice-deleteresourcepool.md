---
description: Starten Sie einen Auftrag, um einen Ressourcenpool zu löschen.
ms.assetid: af3d9c7c-a825-4568-822d-044b3d92d144
title: DeleteResourcePool-Methode der CIM_ResourcePoolConfigurationService Klasse
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
ms.openlocfilehash: a5fb895eb76a503d6199bf1057a9f9eaff0c72e4af59460c63551a7c581ff0cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118648089"
---
# <a name="deleteresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>DeleteResourcePool-Methode der \_ CIM-Klasse "ResourcePoolConfigurationService"

Starten Sie einen Auftrag, um einen Ressourcenpool zu löschen. Möglicherweise sind keine Zuordnungen aus, oder beim Löschen wird "Wird verwendet" nicht verwendet. Wenn der Ressourcenpool ein Stammressourcenpool ist, werden alle Hostressourcen an das zugrunde liegende System zurückgegeben.

## <a name="syntax"></a>Syntax


```mof
uint32 DeleteResourcePool(
  [in]  CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pool* \[ In\]
</dt> <dd>

Ein [**\_ CIM-Ressourcenpool,**](cim-resourcepool.md) der auf den zu löschenden Pool verweist.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ ResourcePoolConfigurationService**](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




