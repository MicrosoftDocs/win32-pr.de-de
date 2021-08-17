---
description: Die Invoke-Methode der CIM \_ DiskSpaceCheck-Klasse wertet eine bestimmte Überprüfung aus. Die Details dazu, wie die Methode eine bestimmte Überprüfung in einem CIM-Kontext auswertet, werden von der nicht abstrakten CIM \_ Check-Unterklasse beschrieben.
ms.assetid: 1f06b0c4-3f39-4a6f-9205-2aa309fb06bb
ms.tgt_platform: multiple
title: Invoke-Methode der CIM_DiskSpaceCheck Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiskSpaceCheck.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: dbf8e976861c079fc79e70b3b9009b8948624e57e02870ad50c2630cd42aca7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118009896"
---
# <a name="invoke-method-of-the-cim_diskspacecheck-class"></a>Invoke-Methode der CIM \_ DiskSpaceCheck-Klasse

Die **Invoke-Methode** der [**CIM \_ DiskSpaceCheck-Klasse**](cim-diskspacecheck.md) wertet eine bestimmte Überprüfung aus. Die Details dazu, wie die Methode eine bestimmte Überprüfung in einem CIM-Kontext auswertet, werden von der nicht abstrakten [**CIM Check-Unterklasse \_**](cim-check.md) beschrieben.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[CIM \_ DiskSpaceCheck](invoke-method-in-class-cim-diskspacecheck.md)
</dt> <dt>

[**CIM \_ DiskSpaceCheck**](cim-diskspacecheck.md)
</dt> </dl>

 

