---
description: Die WMI-Klasse für die \_ Win32-PnPDevice-Zuordnung verknüpft ein Gerät (bekannt als PNPEntity Konfigurations-Manager) und die funktion, die es ausführt.
ms.assetid: 5163a423-60f2-416d-bf82-89517b499f93
ms.tgt_platform: multiple
title: Win32_PnPDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPDevice
- Win32_PnPDevice.SameElement
- Win32_PnPDevice.SystemElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a136c86c0fd0744c555af2071943d99ca8569a33ce9c59d9d22191c4a78d2a32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972040"
---
# <a name="win32_pnpdevice-class"></a>Win32 \_ PnPDevice-Klasse

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) für **die Win32-PnPDevice-Zuordnung \_** verknüpft ein Gerät (bekannt als PNPEntity Konfigurations-Manager) und die funktion, die es ausführt. Seine Funktion wird durch eine Unterklasse des logischen Geräts dargestellt, die seine Verwendung beschreibt. Beispielsweise eine [**Win32-Tastatur- \_**](win32-keyboard.md) oder [**Win32 \_ DiskDrive-Instanz.**](win32-diskdrive.md) Beide Objekte, auf die verwiesen wird, stellen das gleiche zugrunde liegende Systemgerät dar. Änderungen an der Ressourcenzuordnung aufseiten von PNPEntity wirken sich auf das zugeordnete Gerät aus.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{FE28FD96-C875-11d2-B352-00104BC97924}"), AMENDMENT]
class Win32_PnPDevice
{
  CIM_LogicalDevice REF SameElement;
  Win32_PnPEntity   REF SystemElement;
};
```

## <a name="members"></a>Member

Die **\_ Win32-PnPDevice-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ PnPDevice-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**SameElement**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ LogicalDevice**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")
</dt> </dl>

Reference to the [**CIM\_LogicalDevice**](cim-logicaldevice.md) instance representing the logical device properties associated with the Plug and Play device.

</dd> <dt>

**SystemElement**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ PnPEntity**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PnPEntity")
</dt> </dl>

Reference to the [**Win32\_PnPEntity**](win32-pnpentity.md) instance representing the Plug and Play device associated with the logical device.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Computersystemhardwareklassen](computer-system-hardware-classes.md)
</dt> </dl>

 

 
