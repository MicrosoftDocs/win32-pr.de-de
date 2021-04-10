---
description: Stellt einen Dienst dar, mit dem Momentaufnahmen virtueller Systeme erstellt, angewendet und gelöscht werden können.
ms.assetid: 8d5d54a2-08f1-4f24-bca3-601dc698d018
title: CIM_VirtualSystemSnapshotService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7ae74f85d1af9867b7a95c23aeda670b8f06f413
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869283"
---
# <a name="cim_virtualsystemsnapshotservice-class"></a>CIM \_ virtualsystemsnapshotservice-Klasse

Stellt einen Dienst dar, mit dem Momentaufnahmen virtueller Systeme erstellt, angewendet und gelöscht werden können.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemSnapshotService : CIM_Service
{
};
```

## <a name="members"></a>Member

Die **CIM \_ virtualsystemsnapshotservice** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **CIM \_ virtualsystemsnapshotservice** -Klasse verfügt über diese Methoden.



| Methode                                                                      | BESCHREIBUNG                                                                                      |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**Applysnapshot**](cim-virtualsystemsnapshotservice-applysnapshot.md)     | Wendet dem virtuellen System eine Momentaufnahme des virtuellen Systems auf das virtuelle Quellsystem an.<br/> |
| [**CreateSnapshot**](cim-virtualsystemsnapshotservice-createsnapshot.md)   | Erstellt eine Momentaufnahme eines virtuellen Systems.<br/>                                               |
| [**Destroysnapshot**](cim-virtualsystemsnapshotservice-destroysnapshot.md) | Löscht eine Momentaufnahme eines virtuellen Systems.<br/>                                                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Dienst**](cim-service.md)
</dt> </dl>

 

 




