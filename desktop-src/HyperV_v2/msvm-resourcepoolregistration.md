---
description: Registriert einen Dienst, der globale Ressourcenpoolobjekte zur Verfügung stellt.
ms.assetid: B602F6E1-2889-43CF-AAF1-40F339231DB4
title: Msvm_ResourcePoolRegistration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolRegistration
- Msvm_ResourcePoolRegistration.ResourceType
- Msvm_ResourcePoolRegistration.Component
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bbcb0f2e3d5b0dfad884572c90f889d28e47fcffaf328b39d78f02d4c2baa3a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535470"
---
# <a name="msvm_resourcepoolregistration-class"></a>Msvm \_ ResourcePoolRegistration-Klasse

Registriert einen Dienst, der globale Ressourcenpoolobjekte zur Verfügung stellt.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
class Msvm_ResourcePoolRegistration : Msvm_VirtualizationComponentRegistration
{
  Msvm_ResourceTypeDefinition REF ResourceType;
  Msvm_ResourcePoolComponent  REF Component;
};
```

## <a name="members"></a>Member

Die **Msvm \_ ResourcePoolRegistration-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ ResourcePoolRegistration-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Komponente**
</dt> <dd> <dl> <dt>

Datentyp: **[ **Msvm \_ ResourcePoolComponent**](msvm-resourcepoolcomponent.md)**
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

Ein Verweis auf eine -Instanz, die einen vom Dienst unterstützten Ressourcentyp beschreibt. Diese Eigenschaft wird von [**Msvm \_ VirtualizationComponentRegistration geerbt.**](msvm-virtualizationcomponentregistration.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **Msvm \_ ResourcePoolRegistration-Klasse** kann durch UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ VirtualizationComponentRegistration**](/windows/desktop/HyperV_v2/msvm-virtualizationcomponentregistration)
</dt> <dt>

[**Msvm \_ VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md)
</dt> </dl>

 

