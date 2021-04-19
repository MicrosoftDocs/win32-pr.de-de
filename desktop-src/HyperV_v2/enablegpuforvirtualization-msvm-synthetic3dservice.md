---
description: Aktiviert eine physische GPU für die Virtualisierung.
ms.assetid: 700cb46b-97f1-40cf-88d2-64242f4bd2c6
title: Enablegpuforvirtualization-Methode der Msvm_Synthetic3DService-Klasse
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
ms.openlocfilehash: 16cf21424e9af8398cd435dce409bccde03543a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353830"
---
# <a name="enablegpuforvirtualization-method-of-the-msvm_synthetic3dservice-class"></a>Enablegpuforvirtualization-Methode der MSVM \_ Synthetic3DService-Klasse

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

*Physicalgpu* \[ in\]
</dt> <dd>

Ein Verweis auf eine Instanz der [**MSVM \_ Physical3dGraphicsProcessor**](msvm-physical3dgraphicsprocessor.md) -Klasse, die die zu aktivierende physische GPU darstellt.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.

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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ Synthetic3DService**](msvm-synthetic3dservice.md)
</dt> </dl>

 

