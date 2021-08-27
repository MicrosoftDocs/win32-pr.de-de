---
description: Die Invoke-Methode der CIM \_ RemoveDirectoryAction-Klasse führt eine bestimmte Aktion aus. Die Details zur Ausführung der Aktion durch die -Methode sind implementierungsspezifisch. Diese Methode wird von CIM \_ Action geerbt.
ms.assetid: c6a7edcd-aac1-4364-8de5-a16fe2bab107
ms.tgt_platform: multiple
title: Invoke-Methode der CIM_RemoveDirectoryAction Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RemoveDirectoryAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: fab386bc41458ae4f4dd4593141af7671240a7f386c3fd9dfbb6c0d511071094
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120064870"
---
# <a name="invoke-method-of-the-cim_removedirectoryaction-class"></a>Invoke-Methode der CIM \_ RemoveDirectoryAction-Klasse

Die **Invoke-Methode** der [**CIM \_ RemoveDirectoryAction-Klasse**](cim-removedirectoryaction.md) führt eine bestimmte Aktion aus. Die Details zur Ausführung der Aktion durch die -Methode sind implementierungsspezifisch. Diese Methode wird von der [**\_ CIM-Aktion geerbt.**](cim-action.md)

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 Invoke();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Wert 0 (null) und eine beliebige andere Zahl zurück, um einen Fehler anzugeben.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[CIM \_ RemoveDirectoryAction](invoke-method-in-class-cim-removedirectoryaction.md)
</dt> <dt>

[**CIM \_ RemoveDirectoryAction**](cim-removedirectoryaction.md)
</dt> </dl>

 

