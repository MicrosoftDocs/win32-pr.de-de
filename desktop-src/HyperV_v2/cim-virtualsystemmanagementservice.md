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
ms.openlocfilehash: 9db9e85e158f546a3a8780f1211ecd7a7dfc3c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360493"
---
# <a name="cim_virtualsystemmanagementservice-class"></a>CIM \_ virtualsystemmanagementservice-Klasse

Stellt einen Dienst dar, der virtuelle Systeme verwaltet.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemManagementService : CIM_Service
{
};
```

## <a name="members"></a>Member

Die **CIM \_ virtualsystemmanagementservice** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **CIM \_ virtualsystemmanagementservice** -Klasse verfügt über diese Methoden.



| Methode                                                                                      | BESCHREIBUNG                                                                           |
|:--------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**Adresssourcesettings**](cim-virtualsystemmanagementservice-addresourcesettings.md)       | Fügt der Konfiguration eines virtuellen Systems Ressourcen hinzu.<br/>                          |
| [**Definesystem**](cim-virtualsystemmanagementservice-definesystem.md)                     | Definiert ein virtuelles System.<br/>                                                  |
| [**Destroysystem**](cim-virtualsystemmanagementservice-destroysystem.md)                   | Löscht ein virtuelles System.<br/>                                                  |
| [**Modifyresourcesettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) | Ändert die Einstellungen der virtuellen Ressource für eine virtuelle Systemkonfiguration.<br/> |
| [**Modifysystemsettings**](cim-virtualsystemmanagementservice-modifysystemsettings.md)     | Ändert die Einstellungen des virtuellen Systems.<br/>                                          |
| [**Removeresourcesettings**](cim-virtualsystemmanagementservice-removeresourcesettings.md) | Entfernt die Einstellungen virtueller Ressourcen aus einer Konfiguration des virtuellen Systems.<br/>     |



 

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

 

 




