---
description: Stellt den Sicherheitsdienst dar. Es wird zum Konfigurieren der Sicherheitseinstellungen des virtuellen Systems verwendet.
ms.assetid: 00097d81-9fea-4b84-b5dd-e45af46d6e0a
title: Msvm_SecurityService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 32596a46abaa6d745223ab01f8da734e167909f01621deef85f0b21ddfc0b99e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118146895"
---
# <a name="msvm_securityservice-class"></a>Msvm \_ SecurityService-Klasse

Stellt den Sicherheitsdienst dar. Es wird zum Konfigurieren der Sicherheitseinstellungen des virtuellen Systems verwendet.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecurityService : CIM_Service
{
};
```

## <a name="members"></a>Member

Die **Msvm \_ SecurityService-Klasse** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **Msvm \_ SecurityService-Klasse** verfügt über diese Methoden.



| Methode                                                                                            | Beschreibung                                                             |
|:--------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [**GetKeyProtector**](msvm-securityservice-getkeyprotector.md)                                   | Methode zum Abrufen der Schlüsselschutzvorrichtung für ein virtuelles System.<br/>   |
| [**ModifySecuritySettings**](msvm-securityservice-modifysecuritysettings.md)                     | Ändert die aktuellen Sicherheitseinstellungen eines virtuellen Computers.<br/> |
| [**RestoreLastKnownGoodKeyProtector**](msvm-securityservice-restorelastknowngoodkeyprotector.md) | Methode zum Wiederherstellen der letzten bekannten guten Schlüsselschutzvorrichtung.<br/> |
| [**SetKeyProtector**](msvm-securityservice-setkeyprotector.md)                                   | Methode zum Festlegen der Schlüsselschutzvorrichtung für ein virtuelles System.<br/>        |
| [**SetSecurityPolicy**](msvm-securityservice-setsecuritypolicy.md)                               | Methode zum Festlegen der Schlüsselschutzvorrichtung für ein virtuelles System.<br/>        |
| [**Startservice**](msvm-securityservice-startservice.md)                                         | Startet den Dienst.<br/>                                          |
| [**StopService**](msvm-securityservice-stopservice.md)                                           | Beendet den Dienst.<br/>                                           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur Desktop-Apps der Version 1703 \[\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-Dienst**](cim-service.md)
</dt> </dl>

 

 




