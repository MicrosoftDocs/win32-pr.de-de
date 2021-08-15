---
description: Die Reset-Methode der CIM \_ HeatPipe-Klasse fordert eine Zurücksetzung des logischen Geräts an.
ms.assetid: 25153ec2-ecf8-4cf7-a650-03e5c5459445
ms.tgt_platform: multiple
title: Reset-Methode der CIM_HeatPipe Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HeatPipe.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 19bb88066f9422903a139c2641df05cd01a79f0478dbb38775827f9154c13d61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119218060"
---
# <a name="reset-method-of-the-cim_heatpipe-class"></a>Reset-Methode der CIM \_ HeatPipe-Klasse

Die **Reset-Methode** der CIM \_ HeatPipe-Klasse fordert eine Zurücksetzung des logischen Geräts an. Diese Methode wird von [**CIM \_ LogicalDevice geerbt.**](cim-logicaldevice.md)

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

## <a name="syntax"></a>Syntax


```mof
uint32 Reset();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn die Anforderung erfolgreich ausgeführt wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und einen anderen Wert, wenn ein Fehler aufgetreten ist.

## <a name="remarks"></a>Hinweise

Diese Methode wird derzeit nicht von WMI implementiert. Um diese Methode zu verwenden, müssen Sie sie in Ihrem eigenen Anbieter implementieren.

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden. Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[CIM \_ HeatPipe](reset-method-in-class-cim-heatpipe.md)
</dt> <dt>

[**CIM \_ HeatPipe**](cim-heatpipe.md)
</dt> </dl>

 

 




