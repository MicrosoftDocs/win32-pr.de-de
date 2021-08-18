---
description: Stellt einen Dienst dar, der virtuelle Systeme verwaltet.
ms.assetid: b2645546-3c04-4d3f-8d53-019a6db08e24
title: CIM_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 903b751b405c103313c0f83c38687e08ee7bb36a33ae803bd175b6ad91c559cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068620"
---
# <a name="cim_virtualsystemmanagementservice-class"></a>CIM \_ VirtualSystemManagementService-Klasse

Stellt einen Dienst dar, der virtuelle Systeme verwaltet.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemManagementService : CIM_Service
{
};
```

## <a name="members"></a>Member

Die **CIM \_ VirtualSystemManagementService-Klasse** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **CIM \_ VirtualSystemManagementService-Klasse** verfügt über diese Methoden.



| Methode                                                                                      | Beschreibung                                                                           |
|:--------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**AddResourceSettings**](cim-virtualsystemmanagementservice-addresourcesettings.md)       | Fügt einer Konfiguration des virtuellen Systems Ressourcen hinzu.<br/>                          |
| [**DefineSystem**](cim-virtualsystemmanagementservice-definesystem.md)                     | Definiert ein virtuelles System.<br/>                                                  |
| [**DestroySystem**](cim-virtualsystemmanagementservice-destroysystem.md)                   | Löscht ein virtuelles System.<br/>                                                  |
| [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) | Ändert die Einstellungen für virtuelle Ressourcen für eine Konfiguration des virtuellen Systems.<br/> |
| [**ModifySystemSettings**](cim-virtualsystemmanagementservice-modifysystemsettings.md)     | Ändert einstellungen des virtuellen Systems.<br/>                                          |
| [**RemoveResourceSettings**](cim-virtualsystemmanagementservice-removeresourcesettings.md) | Entfernt Einstellungen für virtuelle Ressourcen aus einer Konfiguration des virtuellen Systems.<br/>     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_CIM-Dienst**](cim-service.md)
</dt> </dl>

 

 




