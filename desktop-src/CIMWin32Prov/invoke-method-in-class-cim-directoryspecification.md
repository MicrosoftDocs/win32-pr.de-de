---
description: Die Invoke-Methode der CIM \_ DirectorySpecification-Klasse wertet eine bestimmte Überprüfung aus.
ms.assetid: 63289f94-f134-4159-898c-404cdd8f2a5c
ms.tgt_platform: multiple
title: Aufrufen der Methode der CIM_DirectorySpecification-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectorySpecification.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b8dd080d2bf28bbddf047b4712d5e5688f16be460749df4f5fc28f023697dbf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118419304"
---
# <a name="invoke-method-of-the-cim_directoryspecification-class"></a>Aufrufen der Methode der CIM \_ DirectorySpecification-Klasse

Die **Invoke-Methode** der [**CIM \_ DirectorySpecification-Klasse**](cim-directoryspecification.md) wertet eine bestimmte Überprüfung aus. Details dazu, wie die Methode eine bestimmte Überprüfung in einem CIM-Kontext auswertet, werden von den nicht abstrakten [**CIM \_ Check-Unterklassen**](cim-check.md) beschrieben. Diese Methode wird von **CIM \_ Check** geerbt.

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

Gibt bei Erfolg 0 zurück, 1, wenn die Methode nicht unterstützt wird, und jeder andere Wert gibt einen Fehler an.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[CIM \_ DirectorySpecification](invoke-method-in-class-cim-directoryspecification.md)
</dt> <dt>

[**CIM \_ DirectorySpecification**](cim-directoryspecification.md)
</dt> </dl>

 

