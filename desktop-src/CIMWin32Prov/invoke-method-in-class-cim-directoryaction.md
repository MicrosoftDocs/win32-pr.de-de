---
description: Die Invoke-Methode der CIM \_ DirectoryAction-Klasse führt eine bestimmte Aktion aus. Details dazu, wie die -Methode die Aktion ausführt, sind implementierungsspezifisch. Diese Methode wird von CIM \_ Action geerbt.
ms.assetid: e919dfdb-a52d-4bcb-abff-e1273c406226
ms.tgt_platform: multiple
title: Aufrufen der Methode der CIM_DirectoryAction-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectoryAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a622084daaab6a845a2ffce83222dd605eebc888f730736149bbc0bbcbc81c60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760170"
---
# <a name="invoke-method-of-the-cim_directoryaction-class"></a>Aufrufen der Methode der CIM \_ DirectoryAction-Klasse

Die **Invoke-Methode** der [**CIM \_ DirectoryAction-Klasse**](cim-directoryaction.md) führt eine bestimmte Aktion aus. Details dazu, wie die -Methode die Aktion ausführt, sind implementierungsspezifisch. Diese Methode wird von [**CIM \_ Action**](cim-action.md)geerbt.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 Invoke();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Wert 0 (null) zurück, 1 (eins), wenn die Methode nicht unterstützt wird, und eine beliebige andere Zahl, um einen Fehler anzugeben.

## <a name="remarks"></a>Hinweise

WMI implementiert diese Klasse nicht.

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von dmtf veröffentlicht wurden. Möglicherweise hat Microsoft Änderungen vorgenommen, um kleinere Fehler zu korrigieren, den Dokumentationsstandards des Microsoft SDK zu entsprechen oder weitere Informationen bereitzustellen.

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

[CIM \_ DirectoryAction](invoke-method-in-class-cim-directoryaction.md)
</dt> <dt>

[**CIM \_ DirectoryAction**](cim-directoryaction.md)
</dt> </dl>

 

