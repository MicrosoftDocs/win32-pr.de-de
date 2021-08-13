---
description: Aktiviert eine physische GPU für die Virtualisierung.
ms.assetid: 700cb46b-97f1-40cf-88d2-64242f4bd2c6
title: EnableGPUForVirtualization-Methode der Msvm_Synthetic3DService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DService.EnableGPUForVirtualization
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f1695583f828f650b6e11025cf9f81242bd9c25ae08a421c93b1a1a7494a58cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118645737"
---
# <a name="enablegpuforvirtualization-method-of-the-msvm_synthetic3dservice-class"></a>EnableGPUForVirtualization-Methode der Msvm \_ Synthetic3DService-Klasse

Aktiviert eine physische GPU für die Virtualisierung.

## <a name="syntax"></a>Syntax


```mof
uint32 EnableGPUForVirtualization(
  [in]  Msvm_Physical3dGraphicsProcessor REF PhysicalGPU,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PhysicalGPU* \[ In\]
</dt> <dd>

Ein Verweis auf eine Instanz der [**Msvm \_ Physical3dGraphicsProcessor-Klasse,**](msvm-physical3dgraphicsprocessor.md) die die zu aktivierende physische GPU darstellt.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein objekt, das von [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))abgeleitet wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**Msvm \_ Synthetic3DService**](msvm-synthetic3dservice.md)
</dt> </dl>

 

