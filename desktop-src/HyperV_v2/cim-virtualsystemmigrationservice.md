---
description: Stellt einen Dienst dar, der die Migration virtueller Systeme zwischen Hostsystemen steuert. Diese Klasse überprüft auch, ob eine ausstehende Migration wahrscheinlich erfolgreich ist.
ms.assetid: 28948a36-3b92-4d52-9a48-aaa155e7fad5
title: CIM_VirtualSystemMigrationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d6343cec0573a97656368d66426ec9b46c7255e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864572"
---
# <a name="cim_virtualsystemmigrationservice-class"></a>CIM \_ virtualsystemmigrationservice-Klasse

Stellt einen Dienst dar, der die Migration virtueller Systeme zwischen Hostsystemen steuert. Diese Klasse überprüft auch, ob eine ausstehende Migration wahrscheinlich erfolgreich ist.

## <a name="syntax"></a>Syntax

``` syntax
[Experimental, Abstract, Version("2.17.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationService : CIM_Service
{
};
```

## <a name="members"></a>Member

Die **CIM- \_ virtualsystemmigrationservice** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **CIM \_ virtualsystemmigrationservice** -Klasse verfügt über diese Methoden.



| Methode                                                                                                                     | BESCHREIBUNG                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**CheckVirtualSystemIsMigratableToHost**](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletohost.md)     | Überprüft, ob eine ausstehende Migration eines virtuellen Systems zu einem Host wahrscheinlich erfolgreich ist.<br/>   |
| [**CheckVirtualSystemIsMigratableToSystem**](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletosystem.md) | Überprüft, ob eine ausstehende Migration eines virtuellen Systems zu einem System wahrscheinlich erfolgreich ist.<br/> |
| [**MigrateVirtualSystemToHost**](cim-virtualsystemmigrationservice-migratevirtualsystemtohost.md)                         | Migriert ein virtuelles System zu einem Zielhost.<br/>                                           |
| [**MigrateVirtualSystemToSystem**](cim-virtualsystemmigrationservice-migratevirtualsystemtosystem.md)                     | Migriert ein virtuelles System zum Zielsystem.<br/>                                           |



 

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

 

 




