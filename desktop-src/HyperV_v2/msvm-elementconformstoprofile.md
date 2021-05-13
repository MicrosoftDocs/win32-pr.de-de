---
description: Definiert die registrierten Profile, denen das System entspricht, auf das verwiesen wird.
ms.assetid: F01E79BE-82D9-49E0-AB0C-FD1B48BC4A55
title: Msvm_ElementConformsToProfile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementConformsToProfile
- Msvm_ElementConformsToProfile.ConformantStandard
- Msvm_ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e9b4e257c2ebc0584a8291461439f75238599d35
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843281"
---
# <a name="msvm_elementconformstoprofile-class"></a>Msvm \_ ElementConformsToProfile-Klasse

Definiert die registrierten Profile, denen das System entspricht, auf das verwiesen wird. Diese Zuordnung kann für jedes verwaltete Element gelten. Die typische Verwendung wendet sie auf eine Instanz auf höherer Ebene an, z. B. auf ein System, einen Namespace oder einen Dienst. Bei Anwendung auf eine Instanz auf höherer Ebene müssen sich alle Bestandteile entsprechend verhalten, um die Konformität des verwalteten Elements mit dem benannten registrierten Profil zu unterstützen.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
class Msvm_ElementConformsToProfile : CIM_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a>Member

Die **Msvm \_ ElementConformsToProfile-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ ElementConformsToProfile-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ConformantStandard**
</dt> <dd> <dl> <dt>

Datentyp: **[ **Msvm \_ RegisteredProfile**](msvm-registeredprofile.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Ein Verweis auf eine Instanz der [**Msvm \_ RegisteredProfile-Klasse,**](msvm-registeredprofile.md) die das registrierte Profil darstellt, dem das System entspricht.

</dd> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Datentyp: **[ **Msvm \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Ein Verweis auf eine Instanz der [**Msvm \_ ComputerSystem-Klasse,**](msvm-computersystem.md) die das System darstellt, das dem registrierten Profil entspricht.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 8.1 \[ Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

