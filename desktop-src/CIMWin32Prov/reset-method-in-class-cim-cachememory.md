---
description: Die Reset-Methode der CIM \_ CacheMemory-Klasse fordert eine Zurücksetzung des logischen Geräts an.
ms.assetid: 499426e9-a10f-4d34-a9af-721c2f59d551
ms.tgt_platform: multiple
title: Reset-Methode der CIM_CacheMemory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CacheMemory.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: da5cd756e3f0a56aa51f5de7ef388973d25542853ca29ed4e247ed991ac45698
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119700250"
---
# <a name="reset-method-of-the-cim_cachememory-class"></a>Reset-Methode der CIM \_ CacheMemory-Klasse

Die **Reset-Methode** der CIM \_ CacheMemory-Klasse fordert eine Zurücksetzung des logischen Geräts an. Diese Methode wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

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

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von dmtf veröffentlicht wurden. Möglicherweise hat Microsoft Änderungen vorgenommen, um kleinere Fehler zu korrigieren, den Dokumentationsstandards des Microsoft SDK zu entsprechen oder weitere Informationen bereitzustellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[CIM \_ CacheMemory](reset-method-in-class-cim-cachememory.md)
</dt> <dt>

[**CIM \_ CacheMemory**](cim-cachememory.md)
</dt> </dl>

 

 




