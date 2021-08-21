---
description: Stellt die Registrierung eines Diensts auf der Microsoft Hyper-V Plattform dar.
ms.assetid: 706557C2-49D6-453F-9DC0-2C655888EEBE
title: Msvm_VirtualizationComponentRegistration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualizationComponentRegistration
- Msvm_VirtualizationComponentRegistration.Component
- Msvm_VirtualizationComponentRegistration.ResourceType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c7acd111ab95f59146763e874d40c4efb411313938c94b1a4527aa1e2d08490c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118146554"
---
# <a name="msvm_virtualizationcomponentregistration-class"></a>Msvm \_ VirtualizationComponentRegistration-Klasse

Stellt die Registrierung eines Diensts auf der Microsoft Hyper-V Plattform dar.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
class Msvm_VirtualizationComponentRegistration
{
  Msvm_VirtualizationComponent REF Component;
  Msvm_ResourceTypeDefinition  REF ResourceType;
};
```

## <a name="members"></a>Member

Die **Msvm \_ VirtualizationComponentRegistration-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ VirtualizationComponentRegistration-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Komponente**
</dt> <dd> <dl> <dt>

Datentyp: **[ **Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Verweis auf eine -Instanz, die das COM-Objekt beschreibt, das diese Klasse implementiert.

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Datentyp: **[ **Msvm \_ ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Verweis auf eine -Instanz, die einen vom Dienst unterstützten Ressourcentyp beschreibt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **Msvm \_ VirtualizationComponentRegistration-Klasse** kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Ende des Supports (Client)<br/>    | Windows 8.1<br/>                                                                                  |
| Ende des Supports (Server)<br/>    | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

