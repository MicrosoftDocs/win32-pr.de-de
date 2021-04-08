---
description: Stellt den Sicherheitsdienst dar. Sie wird zum Konfigurieren der Sicherheitseinstellungen virtueller Systeme verwendet.
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
ms.openlocfilehash: cc7b15af3d3033487464fe7b29a93dc649ffbd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959877"
---
# <a name="msvm_securityservice-class"></a>MSVM \_ SecurityService-Klasse

Stellt den Sicherheitsdienst dar. Sie wird zum Konfigurieren der Sicherheitseinstellungen virtueller Systeme verwendet.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecurityService : CIM_Service
{
};
```

## <a name="members"></a>Member

Die **MSVM- \_ SecurityService** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **MSVM- \_ SecurityService** -Klasse verfügt über diese Methoden.



| Methode                                                                                            | BESCHREIBUNG                                                             |
|:--------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [**Getkeyprotector**](msvm-securityservice-getkeyprotector.md)                                   | Methode, mit der die Schlüssel Schutzvorrichtung für ein virtuelles System abgerufen wird.<br/>   |
| [**Modifysecuritysettings**](msvm-securityservice-modifysecuritysettings.md)                     | Ändert die aktuellen Sicherheitseinstellungen einer virtuellen Maschine.<br/> |
| [**Restorelastknowngoodkeyprotector**](msvm-securityservice-restorelastknowngoodkeyprotector.md) | Methode für die Wiederherstellung der letzten als funktionierend bekannten Schlüssel Schutzvorrichtung.<br/> |
| [**Setkeyprotector**](msvm-securityservice-setkeyprotector.md)                                   | Methode, mit der die Schlüssel Schutzvorrichtung für ein virtuelles System festgelegt wird.<br/>        |
| [**Setsecuritypolicy**](msvm-securityservice-setsecuritypolicy.md)                               | Methode, mit der die Schlüssel Schutzvorrichtung für ein virtuelles System festgelegt wird.<br/>        |
| [**Start Service**](msvm-securityservice-startservice.md)                                         | Startet den Dienst.<br/>                                          |
| [**Stop Service**](msvm-securityservice-stopservice.md)                                           | Beendet den Dienst.<br/>                                           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1703, \[ nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Dienst**](cim-service.md)
</dt> </dl>

 

 




