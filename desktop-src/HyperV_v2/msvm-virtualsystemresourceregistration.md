---
description: Registriert einen Dienst, der Virtual Machine-spezifische ressourcenbezogene Objekte bereitstellt.
ms.assetid: 85782C4D-E0A3-4EED-9A26-7928862C559B
title: Msvm_VirtualSystemResourceRegistration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemResourceRegistration
- Msvm_VirtualSystemResourceRegistration.ResourceType
- Msvm_VirtualSystemResourceRegistration.Component
- Msvm_VirtualSystemResourceRegistration.IsRootDevice
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7cef3699de973bd22985215a64100c594f223be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525187"
---
# <a name="msvm_virtualsystemresourceregistration-class"></a>MSVM \_ virtualsystemresourceregistration-Klasse

Registriert einen Dienst, der Virtual Machine-spezifische ressourcenbezogene Objekte bereitstellt.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
class Msvm_VirtualSystemResourceRegistration : Msvm_VirtualizationComponentRegistration
{
  Msvm_ResourceTypeDefinition         REF ResourceType;
  Msvm_VirtualSystemResourceComponent REF Component;
  boolean                                 IsRootDevice = False;
};
```

## <a name="members"></a>Member

Die **MSVM \_ virtualsystemresourceregistration** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ virtualsystemresourceregistration** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Komponente**
</dt> <dd> <dl> <dt>

Datentyp: **[ **MSVM \_ virtualsystemresourcecomponent**](msvm-virtualsystemresourcecomponent.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Verweis auf eine-Instanz, die das COM-Objekt beschreibt, das diese Klasse implementiert.

</dd> <dt>

**Isrootdevice**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** , wenn diese Registrierung angibt, ob der angegebene Ressourcentyp das Stamm Gerät (oder das übergeordnete oder übergeordnete) Gerät für diesen Dienst ist. andernfalls **false**. Wenn **isrootdevice** auf **true** festgelegt ist, kann nur eine Registrierung vorhanden sein. Andernfalls stellt diese Registrierung eine Zuordnung zu einem untergeordneten Gerät dar. Diese Eigenschaft ist immer auf " **false**" festgelegt.

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Datentyp: **[ **MSVM \_ resourcetypeer Definition**](msvm-resourcetypedefinition.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Verweis auf eine-Instanz, die einen vom Dienst unterstützten Ressourcentyp beschreibt. Diese Eigenschaft wird von [**MSVM \_ virtualizationcomponentregistration**](msvm-virtualizationcomponentregistration.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **MSVM \_ virtualsystemresourceregistration** -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Ende des Supports (Client)<br/>    | Windows 8.1<br/>                                                                                  |
| Ende des Supports (Server)<br/>    | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ virtualizationcomponentregistration**](/windows/desktop/HyperV_v2/msvm-virtualizationcomponentregistration)
</dt> <dt>

[**MSVM \_ virtualizationcomponentregistration**](msvm-virtualizationcomponentregistration.md)
</dt> </dl>

 

